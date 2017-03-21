---
layout: post
title: "Opciones para montar un entorno local de WordPress"
description: "Como montar un entorno local de WordPress usando virtualización o a través de docker"
category: 
- Hows To
tags: [wordpress, docker, virtualizacion]
---
{% include JB/setup %}

Estos días estoy trabajando en [iCarto](http://icarto.es) en un pequeño proyecto sobre [Wordpress](https://wordpress.org/) y tengo la necesidad de crear un entorno local para hacer pruebas. En un primer momento, para hacerlo de forma rápida probé a través de las máquinas virtuales de Bitnami.

Bitnami es una empresa que ofrece servicios *Cloud* sobre diferentes herramientas de software libre, sobre las que ofrece diversas opciones para poder probarlas fácilmente a través de máquinas virtuales o contenedores. En este caso yo estuve probando su [máquina virtual de WordPress](https://bitnami.com/stack/wordpress/virtual-machine).

Simplemente con descargarla, importarla en mi virtual box y arrancarla, tenía ya un entorno de WordPress funcionando en local con el que poder hacer pruebas. Por defecto al arrancar el WordPress coge una IP de la red local a la que está conectado el equipo anfitrión, así que cuando cambia de ubicación tenía que cambiar esa IP. En la documentación de Bitnami [aparece documentado](https://docs.bitnami.com/virtual-machine/apps/wordpress/#updating-the-ip-address-or-hostname) y dentro de la máquina virtual hay un *script* para ello.

Entre que en mi caso particular el tener que cambiar de ubicación a menudo y tener que hacer este proceso, y que además tenía que tener arrancadas varias máquinas virtuales, al final decidí explorar otras opciones.

### Montar WordPress con Docker Compose

Muchos habréis oído hablar de Docker y sus sistema de contenedores, así que no voy a entrar mucho en ello, [su propia documentación lo explica mejor](https://www.docker.com/what-docker) de lo que yo podría hacerlo aquí.

Por otro lado Docker Compose es una herramienta que permite combinar varios contenedores Docker con lo que puedes con una sola herramienta gestionar varias aplicaciones *dockerizadas*. Esto encaja bien con WordPress ya que como sabréis para montarlo por un lado tendremos la aplicación en sí y por otro la base de datos [MySQL](https://www.mysql.com/). Si queremos tener dos contenedores separados, uno con la base de datos y otro con sólo el WordPress, Docker Compose es lo que necesitamos para gestionarlo todo.

Antes de nada, para poder usarlo, necesitamos tener instalado Docker en nuestro sistema, luego instalaremos el propio Docker Compose y opcionalmente si queremos podemos instalar el soporte de autocompletado para *Bash*, para tener autocompletado cuando queramos ejecutar comandos dentro de los contenedores.

Para hacer todo esto hay muchos tutoriales por Internet, [yo me guié por este](https://openwebinars.net/blog/instalacion-de-wordpress-con-docker-compose/), que es bastante completo y va guiando el proceso paso a paso. Un detalle importante, como se comenta en el post, es darle los permisos adecuados sobre Docker a nuestro usuario, si no lo hacemos tendremos que ser siempre superusuario cada vez que queramos lanzar docker.

El fichero de configuración que estoy usando es exactamente el mismo que en el post y no me dio ningún problema, como es un fichero *yml* tened en cuenta el indentado, si no si que os dará problemas.

```yaml
version: '2'
services:
  db:
    image: mysql:5.7
    volumes:
      - "./.data/db:/var/lib/mysql"
    restart: always
    environment:
      MYSQL_ROOT_PASSWORD: wordpress
      MYSQL_DATABASE: wordpress
      MYSQL_USER: wordpress
      MYSQL_PASSWORD: wordpress

  wordpress:
    depends_on:
      - db
    image: wordpress:latest
    links:
      - db
    ports:
      - "8000:80"
    restart: always
    environment:
      WORDPRESS_DB_HOST: db:3306
      WORDPRESS_DB_PASSWORD: wordpress`
```

Una vez que tenemos todo esto, para arrancar nuestro WordPress simplemente usamos el comando:

`docker-compose up -d`

Y al abrir el navegador en la url: http://localhost:8000 ya tendremos nuestro WordPress levantado y funcionando.

Una cosa que no cubre el post anterior es como acceder al sistema de archivos donde está nuestro WordPress. Antes de nada, como en realidad lo que tenemos son dos contenedores distintos, tenemos que averiguar el ID que le corresponde. Para eso ejecutamos el comando:

`docker ps`

que nos dará como salida, los contenedores que se están ejecutando. Nos fijamos en la columna con el CONTAINER ID y anotamos el valor para ejecutar el siguiente comando:

`docker exec -it <CONTAINER ID> bash`

Con esto ya podemos ejecutar comandos dentro de nuestro contenedor con WordPress.



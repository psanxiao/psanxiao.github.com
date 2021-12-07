---
layout: post
title: "Sirviendo Vector tiles con Geoserver"
description: "Pequeño tutorial de como servir Vector tiles con Geoserver"
category:
  - Hows To
tags: [Vector tiles, Geoserver, Docker]
---

{% include JB/setup %}

Versión escrita y resumida de un webminar que preparé para el módulo de SIG Distribuido del Máster Profesional en SIG de [UNIGIS](https://unigis.es). En él obtenemos un contenedor de Geoserver preparado para _docker_, instalamos un plugin para servir _Vector tiles_ y configuramos todo lo necesario para servir una capa de ejemplo.

## **Paso a Paso**

### Instalamos Docker

El primer paso será tener instalado Docker en nuestro equipo. En la web oficial tendremos la [documentación para instalarlo](https://docs.docker.com/get-docker/) según el sistema operativo que utilicemos.

### Obtenemos la extensión para GeoServer

Descargamos la extensión oficial de Vector tiles para GeoServer, desde la [web de descargas](https://docs.geoserver.org/stable/en/user/extensions/vectortiles/index.html). Vamos al enlace _Installing the Vector Tiles Extension_, en el primer párrafo pulsamos en el enlace _GeoServer download_, que nos llevará a la página de descargas de GeoServer. Ahí escogemos la versión estable y en el apartado de Extensiones, buscamos en la sección _Output Formats_ la extensión _Vector Tiles_, hacemos click y se descargará la extensión en nuestro equipo. Una vez descarga, renombramos la carpeta general y la llamamos _vectortiles_.

Para poder utilizarla después con nuestro contenedor de Docker, crearemos en el directorio que queramos una carpeta llamada **geoserver-exts** y copiaremos nuestra carpeta vectortiles ahí dentro. De esta forma, los ficheros de la extensión que descargamos deberían quedar en una ruta del tipo:

```bash
[Directorio]/geoserver-exts/vectortiles
```

### Descargamos la imagen de GeoServer para Docker

Usaremos una imagen Docker preparada para desplegar un GeoServer, usando Tomcat como servidor de aplicaciones. Esta imagen fue creada y es mantenida por Oscar Fonts. Tenemos toda la información sobre la misma en su [repositorio de GitHub](https://github.com/oscarfonts/docker-geoserver).

Para descargarla usaremos uno de los comandos que nos ofrece Docker. Abriremos un terminal de línea de comandos y ejecutamos:

```bash
docker pull oscarfonts/geoserver
```

Una vez descargada la imagen, para arrancar nuestro GeoServer ejecutaremos el siguiente comando:

```bash
docker run —name geoserver -d -p 8080:8080 oscarfonts/geoserver
```

Con la etiqueta -name le indicamos el nombre que le queremos dar al contenedor, en este caso lo llamamos simplemente geoserver. Después le indicamos el puerto en el que queremos que se ejecute, en este caso en el 8080, y finalmente le indicamos que use la imagen que acabamos de descargar.

**Nota**: _Este comando lo ejecutaremos sólo la primera vez, ya que lo que estamos haciendo es crear un contenedor a partir de la imagen. A partir de ese momento podremos detener y arrancar ese mismo contenedor siempre que queramos. Con esa misma imagen podemos crear otros contenedores, usando el comando anterior, pero poniéndole otro nombre y si vamos a querer ejecutarlos a la vez, cambiando también el puerto_.

Docker nos ofrece algunos comandos para ver los contenedores que tenemos y los que están ejecutándose.

```bash
docker ps (contenedores ejecutándose)
docker ps -a (todos los contenedores disponibles)
```

Si queremos parar nuestro contenedor de geoserver que hemos arrancado hacemos:

```bash
docker stop geoserver
```

Y para arrancarlo de nuevo:

```bash
docker start geoserver
```

Otros comandos interesantes:

```bash
docker rm geoserver
docker images (listar imágenes)
docker rmi imagen (eliminar imagen)
```

### Instalar la extensión Vector tiles en nuestro GeoServer

Para instalar cualquier extensión en GeoServer basta con copiar la carpeta con los ficheros al directorio de extensiones que está en la ruta **/var/local/geoserver-exts**. En nuestro caso, al usar un contenedor de Docker, en el momento de crearlo tenemos que decirle que use como directorio de extensiones una ruta de nuestro equipo, donde tendremos la extensión preparada. Esa ruta será la que creamos en el primer punto, cuando descargamos los ficheros de extensión.

En el comando de creación de nuestro contenedor, le diremos que use ese directorio como directorio de extensiones de GeoServer:

```bash
docker run —name geoserver -d -p 8080:8080 -v [Directorio_local]/geoserver-exts:/var/local/geoserver-exts oscarfonts/geoserver
```

De la misma manera, si queremos cargar algunos datos en nuestro GeoServer _dockerizado_, haremos lo mismo con el directorio de datos de GeoServer:

```bash
docker run —name geoserver -d -p 8080:8080 -v [Directorio_local]/geoserver:/var/local/geoserver oscarfonts/geoserver
```

Y por supuesto podemos combinar ambos:

```bash
docker run —name geoserver -d -p 8080:8080 -v [Directorio_local]/geoserver:/var/local/geoserver -v [Directorio_local]/geoserver-exts:/var/local/geoserver-exts oscarfonts/geoserver
```

### Servir capa como Vector Tile en GeoServer

Simplemente tenemos que publicar una capa de la manera habitual, y en la pestaña de Cacheado de Teselas, seleccionamos uno de los nuevos formatos que nos ofrece la extensión.

![Geoserver](/assets/images/posts/geoserver-vectorTiles.png)

El formato recomendado para servidores en producción es el **mapbox-vector-tile** (MVT). Es un formato binario muy eficiente y soportado por casi todas las aplicaciones que permiten consumir Vector tiles.

El formato **geojson** es un formato de texto, más legible, y aunque la mayoría de aplicaciones que permiten consumir información geográfica aceptan el formato estándar de geojson, en el caso de Vector tiles servidas en este formato, el soporte es aún limitado.

El formato **topojson** es más complejo, su uso se aconseja sólo en determinadas situaciones y es todavía poco soportado por las aplicaciones que pueden consumir Vector tiles.

En la documentación de GeoServer tenemos un [ejemplo de como consumir una capa en Vector tiles](https://docs.geoserver.org/stable/en/user/extensions/vectortiles/tutorial.html), desde un pequeño visor creado con OpenLayers.

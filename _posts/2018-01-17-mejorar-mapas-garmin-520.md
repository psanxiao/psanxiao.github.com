---
layout: post
title: "Mejorar los mapas de un Garmin 520"
description: "Como mejorar los mapas de un garmin 520 gracias a Openstreetmap"
category: 
- Hows To
tags: [mapa, map, openstreetmap, garmin, gps]
---
{% include JB/setup %}

Estas pasadas navidades me regalaron un [Garmin 520](https://buy.garmin.com/es-ES/ES/p/166370#overview), un dispositivo con GPS para llevar en la bicicleta con el que se registra un montón de parámetros, se pueden programar entrenamientos y gracias a sus capacidades GPS almacenar las rutas realizadas o incluso recibir instrucciones para seguir una.

Las capacidades en este último caso son limitadas, ya que no funcionan como un navegador GPS de los que estamos acostumbrados a llevar en el coche, hoy en día ya más sustituidos por los propios móviles, ya que no tiene capacidad de hacer enrutado, es decir, no le puedes decir estoy en el punto A, quiero ir al punto B, calculame el recorrido. Este trabajo hay que hacerlo previamente y cargar la ruta a seguir en el dispositivo previamente. 

Existen muchos sitios en Internet donde poder descargar rutas en formatos de ficheros compatibles con este dispositivo, [wikiloc](https://es.wikiloc.com/) por ejemplo es uno de los más conocidos, la propia [aplicación web de garmin](https://connect.garmin.com/es-ES/) permite compartir rutas entre usuarios, y por supuesto el famoso [Strava](https://www.strava.com/), [del que ya he hablado varias veces en este blog](http://psanxiao.com/cuando-el-producto-es-muy-bueno-y-es-gratis-tu-eres-el-producto). Una vez cargadas en el dispositivo éste es capaz de guiarte por ellas, a través de instrucciones en la pantalla y mostrándote la ruta en un mapa. Y aquí es donde entra este post, en esos mapas.

Una de las características de este dispositivo es que no tiene mucha capacidad de memoria interna, y a diferencia de otros modelos superiores no se puede incrementar mediante tarjetas externas. Supongo que en gran parte por este motivo los mapas base que trae son bastante escuetos. La cartografía que incluye cubre una parte muy grande de territorio pero a costa de no ser muy detallada, no esperes por ejemplo que te muestre carreteras o caminos, se limita simplemente a mostrar algunos puntos de referencia simplemente.

![mapa-strava](/assets/images/posts/garmin-520-osm.jpg)

### Openstreetmap al rescate

Por suerte esto es *hackeable* y gracias a [Opentreetmap](http://psanxiao.com/un-mapa-hecho-entre-todos) podemos mejorar y mucho la cartografía base de nuestro mapa. Vamos a ello:

Lo primero de todo es conseguir la cartografía base adaptada a nuestro dispositivo, para ello contamos con la ayuda de [una web específica](http://garmin.openstreetmap.nl/) donde podemos encontrar datos de Openstreetmap adaptados para nuestro dispositivo. Al contar con poca memoria y querer tener mapas muy detallados lógicamente debemos de sacrificar algo y en este caso no es otra cosa que disponer de menos territorio. Esto tampoco debería ser mayor problema, ya que normalmente saldremos en bici por una zona acotada cercana a donde vivimos y en el caso de que nos vayamos de viaje a otras zonas siempre podemos cambiar el mapa y adaptarlo.

En esta web vemos una serie de opciones y un mapa. Aquí tenemos que tener en cuenta fundamentalmente tres cosas: Por un lado el tipo de mapa que queremos y que podemos elegir en la primera opción. Básicamente en todos hay los mismos datos pero cambia la simbología según lo vayamos a usar para una cosa u otra. En el caso de la bicicleta yo elijo la opción **Routable Bicycle (Openstreetmap Lite)**.

El segundo punto es elegir el trozo de mapa que queremos. Para ello en las opciones bajo la etiqueta **Choose a predefined country** podemos ir seleccionando nuestro país y así el mapa de abajo se nos irá centrando. Después tendremos que elegir una o varias de las cuadrículas en las que está dividido el mapa. Esas cuadrículas representan el trozo de mapa que nos estamos descargando para nuestro dispositivo. 

Al elegir un país en el mapa, por defecto están seleccionadas todas las cuadrículas que lo cubren. Como esto suele ser demasiada información para la memoria de nuestro dispositivo, yo lo que hago es en el apartado que pone **Perhaps you'd like to add some additional tiles?** pulsar el botón *Reset Selection*, lo que hace que se elimine toda la selección, así puedo controlar yo que cuadrículas me interesan manualmente. Para ello marco la opción *Enable manual tile selection* y entonces ahora al pinchar con el ratón sobre una o varias cuadrículas se seleccionan, se rellenan en azul, y esas serán las que me descargue.

Después de todo esto sólo nos queda rellenar nuestra dirección de correo en **Request your map or download it directly** y hacer click sobre el botón *Build my map*. La página procesará nuestra petición y nos enviará dos correos electrónicos, uno diciéndonos que todo está en orden y que en breve nuestro mapa estará listo para descargar, con un enlace que nos dirá el tiempo que falta aproximadamente para estar listo, y posteriormente cuando terminé el proceso nos enviará otro correo con el enlace para descargarlo.

El enlace de descarga nos proporciona varios tipos de formatos. Yo suelo coger el que tiene el icono de MicroSD, un zip que se llama *openfietsmap_lite_gmapsupp.zip*. Al descomprimirlo nos quedará un fichero que se llama *gmapsupp.img*, que es el que contienen nuestro mapa. Este fichero deberemos pasarlo al garmin, pero antes tenemos que renombrarlo a *gmapbmap.img* que es el nombre del fichero que tiene el mapa en nuestro garmin.

### Pasar el mapa a nuestro dispositivo

Para pasar el mapa a nuestro garmin simplemente tenemos que conectar este a nuestro ordenador con el cable. Aparecerá como un disco duro o una memoria usb y veremos los archivos que hay dentro. En la raíz es donde tendremos el fichero llamado *gmapbmap.img* que tenemos que cambiar por el que nos acabamos de descargar.

**Importante!** Antes de hacer el cambio guardar una copia del que viene por defecto en nuestro ordenador para poder recuperarlo y dejar el dispositivo como estaba, por si hay algún problema o simplemente queremos usar los mapas que traía por defecto.  


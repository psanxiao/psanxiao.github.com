---
layout: post
title: "Un mapa hecho entre todos"
description: "Introducción a la cartografía colaborativa"
category: 
    - 12meses12mapas
tags: [openstreetmap, mapa, map, cartografía, colaborativa]
---
{% include JB/setup %}

No podía faltar en esta serie de [#12meses#12mapas](http://psanxiao.com/12meses12mapas) el hablar de la cartografía colaborativa y su máximo estandarte como es el proyecto [Openstreetmap](http://osm.org). Este proyecto tiene como objetivo crear un mapa de todo el mundo de forma colaborativa, permitiendo a cualquier persona incluir nuevas cosas en él, modificar las que ya están para corregir errores o mejorar la información.

Normalmente en los talleres o charlas sobre Openstreetmap se suele empezar con un pequeño ejercicio, se les pide a las personas asistentes que dibujen un pequeño mapa. Yo suelo pedirles que dibujen un mapa de una misma zona que todas conozcan, así después les pregunto si creen que cualquiera de esos mapas será lo suficientemente completo para que alguien que no conozca nada de esa zona, tenga toda la información que necesita. Normalmente la respuesta es que no, así que les pregunto que pasaría si pudiésemos juntar todos esos mapas en uno sólo, si pudiésemos juntar en un único punto todo el conocimiento que cada uno de los asistentes tiene sobre esa zona. De esa forma entonces seguramente sí tendríamos un mapa lo suficientemente bueno y completo.

Otra de las reflexiones que suelo hacer en las charlas sobre Openstreetmap es que pasaría si cada uno de nosotros dedicásemos un poco de tiempo, no mucho, a mantener actualizada la información de donde vivimos, tan sólo nuestra calle, nuestro barrio o un pedacito de nuestro pueblo. Con ese pequeño esfuerzo por parte de mucha gente, tendríamos la mejor cartografía posible, actualizada prácticamente a tiempo real.

Los antiguos cartógrafos que hacían los mapas en realidad usaban algo parecido a la cartografía colaborativa. Cuando el mundo no estaba cubierto por satélites y la idea de poder ver cualquier punto del mismo desde un ordenador quedaba todavía muy lejos de las más imaginativas mentes, la única manera de hacer mapas era usar el conocimiento de la gente, preguntar a viajeros, marineros, comerciantes, para hacerse una idea de como era el mundo en el que vivían.

![mapa-osm](/assets/images/posts/map-osm.png)

### OpenStreetMap

El proyecto Openstreetmap es el principal valuarte de la cartografía colaborativa, un proyecto que nació en el año 2006 y que intenta crear un mapa del mundo a través de colaboraciones voluntarias, al estilo Wikipedia. Suele, por error, muchas veces verse el nombre en plural, Openstreetmaps, pero es importante recordar que la idea es crear un único mapa de todo el mundo, llevándolo al ejemplo del principio sería como dibujar todos juntos en un mismo papel. 

Si nos ponemos estrictos, en realidad Openstreetmap, no es ni siquiera un mapa como tal, sino una base de datos. Aunque todo lo que aportamos al proyecto dibujando lo hacemos sobre un mapa, en realidad lo que estamos alimentando es una gran base de datos, donde las líneas, puntos y áreas que dibujamos se transforman en coordenadas geográficas y donde además guardamos más información relacionada con ellas. Cuando dibujamos un cuadrado por ejemplo que representa un edificio, también podemos decir para que sirve, si es una vivienda o si tiene algún uso diferente, cuantas plantas tiene, si tiene un nombre, cual es su dirección postal, su número, podemos incluso añadir información sobre si es accesible para personas con movilidad reducida, etc, etc, etc...

Toda esta información que añadimos al proyecto se puede consultar y lo más importante, se puede usar para lo que se quiera, porque es libre. Esto significa que podemos usar esta gran base de datos para lo que nosotros queramos, crear nuestro mapa del mundo, o muchos mapas de zonas más pequeñas, podemos destacar puntos, podemos destacar carreteras, vías ciclistas o simplemente podemos darle unos colores bonitos e imprimir un cuadro, todo es posible. El único requisito es citar la fuente, reconocer todo el esfuerzo, dedicación y trabajo voluntario de todas las personas que colaboran para crear este mapa global o base de datos.

### La calidad de la información

Una de las preguntas más habituales sobre Openstreetmap y en general sobre la cartografía colaborativa, es cómo de buena es la información que se genera. Esta pregunta en realidad no tiene una respuesta fácil. Para llegar si cabe a plantearnos una posible respuesta a esta pregunta, tenemos que empezar por reflexionar que entendemos por buena información. Tratándose de un mapa lo que uno espera es que la información que contiene sea fiel a la realidad, y que donde pone que hay una calle, pues que esa calle exista, por ejemplo. Desde un punto de vista más técnico, un cartógrafo podría tener una interpretación diferente de lo que a su juicio se le debería pedir a un mapa en términos de calidad. 

Si se compara con otras soluciones más conocidas como puede ser Google Maps por ejemplo, cabe preguntarse cómo podemos saber que lo que éste nos muestra es real si los datos sólo los manejan ellos. Es sabido que [Google Maps muestra cosas diferentes según desde que país se consulte](https://www.elconfidencial.com/tecnologia/2015-05-25/google-y-las-fronteras-de-sus-mapas-entre-la-diplomacia-la-polemica-y-el-escandalo_852397/) por ejemplo. En realidad este tipo de problemas se podrían dar de forma parecida en OSM, dependiendo de la nacionalidad del autor de un cambio las cosas podrían estar dibujadas de una o de otra manera. Desde ese punto de vista es difícil poder decir si un mapa hecho mediante cartografía colaborativa u otro hecho por una persona, una entidad o una empresa es más o menos fiable o tiene más o menos calidad.

Otro aspecto es la precisión. Aquí pueden entrar en juego diversos factores, desde las herramientas que se usan hasta la pericia de la persona que lo hace. La reflexión en este punto tiene que venir por la necesidad de la cartografía, no es necesaria la misma precisión cuando sólo se quieren mostrar cosas a gran escala o cuando se quiere ir al detalle, igual que no es la misma la precisión necesaria para mostrar algo sobre una cartografía base, que cuando queremos usarla para navegar entre dos puntos siguiendo unas indicaciones, en este caso necesitaremos mucha precisión, que las calles estén correctamente conectadas entre sí, los sentidos de circulación, etc.

En la cartografía colaborativa es fácil entender que la calidad y la precisión de los datos, independientemente de como la interpretemos, va a variar mucho entre unas zonas y otras. Con algo más de 3 millones de colaboradores actualmente es complicado poder hablar de homogeneidad en estos aspectos, pero al mismo tiempo este "problema" se transforma también en una ventaja. La cantidad de voluntarios hace que en realidad los posibles errores o bajas calidades y precisiones puedan ser corregidos con más facilidad. Es fácil sin ir más lejos hacer una prueba uno mismo, modificando o creando algo mal y ver cuanto tiempo pasa hasta que alguien lo corrige.

### El conocimiento local

Cuando comparamos la información de Openstreetmap con otras fuentes de datos cartográficos suele haber sorpresas. Uno puede esperar a priori, sin conocer a lo mejor demasiado sobre el proyecto, que en general haya menos cantidad de información en OSM, sin embargo en muchos casos no es así, y no sólo es así porque la información de OSM sea al menos tanta como en otros casos si no porque muchas veces es incluso mayor.

En todos estos casos el motivo suele estar relacionado con el mayor conocimiento local que los voluntarios que cartografían en OSM poseen. Ese conocimiento local aporta una gran diferencia a la hora de cartografiar muchos detalles que en otros casos pasan inadvertidos. Cuando alguien añade información en OSM de una zona que conoce bien puede añadir una infinidad de detalles a la cartografía, desde una papelera, un pequeño camino peatonal en un parque o una fuente de agua. 

Los procesos de generación de cartografía que siguen las grandes empresas que se dedican a ello pasan por automatizar al máximo las tareas, creando cartografía a partir de imágenes por satélite, vehículos que recogen información con cámaras y sensores, etc... y eso hace que muchos de los pequeños detalles pasen desapercibidos.

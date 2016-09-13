---
layout: post
title: "Popular Races: Una web de carreras geolocalizadas Low Cost"
description: "Popular Races es un mini proyecto para crear una web de carreras populares que se visualizan en un mapa"
category: 
- Development
tags: [carreras, cartodb, carto, geocoding, ]
---
{% include JB/setup %}

Llevo tiempo en el mundo de las carreras y competiciones populares como [atleta y triatleta amateur](http://psanxiao.com/athlete), y desde siempre me ha llamado la atención que las webs donde se recoge información sobre las mismas las muestren en un listado, ordenado por fechas, o en forma de calendario. Que está bien y es práctico pero siempre pensé que un mapa sería una mejor forma de mostrarlo. 

### El objetivo: Mostrar carreras en un mapa
Por lo menos en Galicia últimamente hay una cantidad enorme de carreras populares, que se celebran no sólo en ciudades sino también en pueblos y aldeas pequeños. Consultando los listados o los calendarios siempre acabo mirando en un mapa la localización para saber donde están, si quedan más o menos cerca o si suponen un desplazamiento importante, que suele implicar madrugón.

Cómo llevaba tiempo queriendo jugar con una tecnología para hacer mapas en web, llamada *CartoDB* por aquel entonces, hoy [CARTO](http://carto.com), cree un pequeño proyecto para poder mostrar carreras populares en un mapa. [El resultado es una pequeña web](https://popular-races.github.io/popular-races), muy rudimentaria, en la que además de ver las carreras en un mapa, y poder dar de alta nuevas, se pueden hacer algunos filtros para buscar las carreras más próximas tanto en el tiempo como en el espacio (a partir de la ǵeolocalización del usuario), además de lógicamente filtrar por tipos básicos, dependiendo si buscamos carreras, triatlones o trails.

### El proceso: Jugando con CARTO
Desde el punto de vista tecnológico, me interesaba, además de jugar un poco con la tecnología de CARTO, montar este pequeño proyecto sin necesidad de infraestructura propia, montando algo así como un prototipo de software de "inventario low-cost", en el que ahora se muestran carreras, pero en realidad valdría para otras muchas cosas. El almacenamiento de la información se hace en CARTO, y el código fuente se almacena en [GitHub](https://github.com/psanxiao/popular-races), desde donde se sirve la propia aplicación. Se usa también la [API de Geocoding](https://carto.com/location-data-services/geocoding/) del propio CARTO para asignar la posición geográfica de las carreras de forma automática. 

Usar CARTO permite tener una base de datos online, con una API a través de la cual es muy fácil hacer consultas, básicamente es como están implementados los filtros. La visualización del mapa se hace directamente desde el propio editor web, sin necesidad de programación por lo que se puede separar totalmente y lo podría haber hecho alguien que supiese hacer mapas, por ejemplo. El API de geolocalización me ha dado algún resultado extraño, como comenté en la [lista de correo](https://groups.google.com/forum/#!topic/cartodb/K-Vwjo33NCQ), pero en general funciona bien. 

Para que la geolocalización funcione por ejemplo en Chrome, la página tiene que servirse bajo *https*, lo cual me ha generado algún problema. Las *gh-pages* de GitHub se pueden servir bajo *https* pero no si se usa un dominio propio, por eso he creado una organización dentro de GitHub, ya que mi cuenta está asociada a este dominio [al servirse también este blog desde GitHub](http://psanxiao.com/new-psanxiao-dot-com).

### El resultado: Popular Races
El resultado, como comentaba, [es una pequeña web](https://popular-races.github.io/popular-races), más o menos funcional a día de hoy, muy mejorable en cuanto a diseño gráfico y de interacción.

![popularraces](/assets/images/posts/popular-races.png)

La geolocalización a través del navegador parece que está dando algo de problemas últimamente en algunas versiones de algunos navegadores. Ahora mismo está funcionando bien en Chrome, pero a veces da problemas con Firefox. A nivel dispositivos móviles no está optimizada, aunque es funcional. Los filtros deberían aparecer en formato menú, pero se colocan debajo del mapa, que a su vez coge todo el ancho de la pantalla cuando se ve en una tablet o móvil.

Si quieres probarla y subir carreras adelante. Si quieres comentarme que te parece la idea, posibles mejoras o incluso mejorar el código actual, adelante.
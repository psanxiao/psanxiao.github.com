---
layout: post
title: "El mapa del cólera de John Snow"
description: "Artículo sobre el mapa de John Snow que ayudo a frenar la epidemia de cólera en Londres"
category: 
- 12meses12mapas
tags: [Jonh Snow, mapa, cólera, londres]
---
{% include JB/setup %}

Me resistía a iniciar esta [serie de 12 posts](http://psanxiao.com/12-meses-12-mapas) con el famoso mapa del cólera de John Snow. No porque no sea un mapa interesante para un artículo, ni mucho menos, sino porque me han hablado y he hablado tantas veces sobre él que estoy un poco saturado. Sin embargo, pensándolo un poco, si en realidad hablo tanto de él es porque en realidad representa muy bien una idea que me fascina y es la utilización de los mapas como herramientas para analizar y comunicar información.

### La historia detrás del mapa

La historia de este mapa se encuadra en el Londres de 1854, una época en la que las ciudades en general y Londres en particular eran muy diferentes a las actuales. Con algo más de 2,5 millones de personas, Londres era una de las mayores ciudades del mundo en aquellos tiempos. Gestionar una ciudad de estas características en esa época no era tarea fácil. Los servicios que hoy en día calificamos como básicos en aquellos tiempos eran muchas veces una utopía. La gestión de los residuos urbanos era complicada y el alcantarillado un sistema muy deficiente, en su mayor parte conformado por pozos negros en los sótanos de los edificios.

Esta situación era un caldo de cultivo para enfermedades de todo tipo. En concreto durante ese año se vivió uno de los brotes de cólera más virulentos de la historia en Londres. En el pequeño barrio del Soho, este brote se cebó especialmente provocando cerca de mil muertes en un área de sólo medio kilómetro cuadrado. Esta no era la primera epidemia de cólera que se daba en Londres y en Gran Bretaña, dos anteriores se habían cobrado más de 50.000 vidas cada una. En aquellos tiempos se creía, avalado así por las personalidades médicas más importantes, que el cólera se transmitía por el aire. Sin embargo, algunos epidemiólogos, entre los que se encontraba el doctor John Snow, empezaban a sospechar lo contrario. En 1849 el doctor Snow había escrito sobre esto y su tesis era que el cólera se transmitía por el consumo de agua o comida contaminada.

Cuando la epidemia del cólera llego al Soho, el doctor Snow que vivía en la zona pensó que su conocimiento de la misma y el contacto con los residentes le permitiría encontrar una causa. Convencido de que el cólera no se transmitía por el aire, empezó a visitar las casas de los enfermos y preguntar sobre sus hábitos. Al tercer día creyó dar con la causa, una bomba de agua en la calle *Broad Street*, en el cruce con *Cambridge Street*. La mayoría de personas que vivían por la zona se abastecían de esa bomba, además de locales cercanos, donde habían muerto varios de sus clientes. Snow analizó el agua pero no encontró nada concluyente, aunque algunos vecinos le dijeron que el agua sabía de forma diferente. Convencido de tener razón pero sin poder probarlo todavía pidió un listado de todos los fallecidos al Registro de Defunciones. Gracias a este listado detectó que la mayoría de fallecidos vivían cerca de la bomba. Además también pudo comprobar que el cólera no se transmitía por el aire, ya que en un asilo cercano a la misma no había ningún caso de cólera, ya que contaba con su propia bomba.

Gracias a estos hallazgos, las autoridades clausuraron la bomba y el brote de cólera comenzó a remitir.

### EL mapa

![snowMap](/assets/images/posts/snow_map.png)

El famoso [mapa del doctor Snow](https://www1.udel.edu/johnmack/frec682/cholera/snow_map.png) se empezó a confeccionar a partir de aquí, ya que en realidad no fue un mapa de la causa sino una manera de ilustrar sus hallazgos.

El mapa de base que utilizó ya estaba disponible, era un mapa elaborado por [Charles Cheffins](https://en.wikipedia.org/wiki/Charles_Cheffins), cartógrafo conocido sobre todo por haber realizado algunos de los primeros mapas del ferrocarril. El plano tenía una escala de 30 pulgadas: 1 milla.

El doctor Snow añadió tres elementos sobre este mapa, como si fueran capas de lo que hoy conocemos como un [Sistema de Información Geográfica](http://volaya.github.io/libro-sig/chapters/Introduccion_fundamentos.html). Primero dibujó las 13 bombas de agua repartidas por el barrio del Soho. Después delimitó mediante una línea de puntos la zona en la que la bomba de *Broad Street* estaba más cerca de los residentes que cualquier otra, lo que hoy conocemos como [diagrama de Voronoi](https://es.wikipedia.org/wiki/Pol%C3%ADgonos_de_Thiessen). Finalmente añadió una serie de rayas negras que identificaban personas fallecidas colocándolas donde vivían estas, resultando una gran acumulación en torno a *Broad Street*. Este mapa fue mostrado por el doctor Snow como parte de sus hallazgos sobre el cólera en la conferencia que dio en la Sociedad Epidemiológica de Londres en diciembre de 1854.

Aunque estos hallazgos mostrados por el doctor Snow parecían irrefutables, faltaba aún la causa de la contaminación de la bomba de agua. Aquí entra la figura del reverendo Henry Whitehead, un párroco local que también investigó por su cuenta sobre el brote en el Soho. Fruto de sus investigaciones habló con un policía local que vivía en el número 40 de *Broad Street*, que le contó que su hija había muerto después de enfermar el 2 de septiembre, justo antes del brote. La esposa del policía le contó al reverendo Whitehead que vaciaba el agua con las "deyecciones" de su hija en el sumidero del sótano. El reverendo comprobó entonces que el contenido de ese pozo se estaba filtrando a la tierra y por lo tanto en el suministro de agua. El caso de esta víctima no figuraba en el mapa del doctor Snow, que recogía 4 muertes en lugar de 5 en el número 40 de *Broad Street*.

Hoy en día en el actual barrio del Soho se conservan varias referencias al doctor John Snow, en la famosa *Broad Street* renombrada hoy como *Broadwick Street*, desde un pub con su nombre donde se reune la *The John Snow Society*, [una escultura de la famosa bomba de agua](https://en.wikipedia.org/wiki/John_Snow#/media/File:John_Snow_memorial_and_pub.jpg), o incluso [una pequeña placa](https://www.flickr.com/photos/psanxiao/17431573782/in/album-72157652448973666/) en el edificio donde estaba dicha bomba.

Lo que hoy son técnicas habituales en el análisis de información o el uso de mapas como vehículo para mostrar los resultados de dicho análisis, eran en aquella época una innovación. Sin embargo, aunque este mapa es probablemente el más famoso y el que más repercusión ha tenido, en parte también por la figura del doctor Snow, existen casos anteriores de análisis de este tipo basados en mapas. Uno famoso [es el de Valentine Seaman](https://brianaltonenmph.com/gis/historical-disease-maps/valentine-seaman-1804-the-black-plague-or-yellow-fever-in-new-york-city/), funcionario de salud pública de Nueva York, que en 1798 dibujó un mapa de la distribución de la fiebre amarilla en el puerto de esa ciudad.

En realidad, volviendo ahora al inicio del post, creo que sí o sí tenía que empezar esta serie con este mapa. No se me ocurre mejor ejemplo para ilustrar dos ideas básicas: Cualquier dato se puede poner en un mapa y cuando la información se pone en un mapa, su análisis alcanza una nueva perspectiva.


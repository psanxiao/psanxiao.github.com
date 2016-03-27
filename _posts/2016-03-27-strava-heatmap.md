---
layout: post
title: "Heatmap de mis actividades en Strava"
description: "" 
category: 
- Spanish
- Running
tags: []
---
{% include JB/setup %}

Inspirado por este [post](http://brunosan.eu//2012/07/20/a-heatmap-for-all-your-runs-in-runkeeper/) hice dos [heatmaps](https://en.wikipedia.org/wiki/Heat_map) con mis actividades de los últimos dos años que tengo subidas en [Strava](https://www.strava.com/athletes/psanxiao).

Desde Strava es posible bajarse todas las actividades que se tienen registrada en un sólo archivo comprimido, que en realidad contiene dentro todas y cada una de ellas en ficheros GPX, así que el primer paso fui unirlos todos con la ayuda de [ogr2ogr](http://www.gdal.org/ogr2ogr.html) y un pequeño script, para obtener en mi caso dos ficheros, uno con las actividades de running y otro con las de ciclismo.

Una vez creados los dos ficheros, en mi caso cree los mapas subiéndolos a mi cuenta de [CartoDB](https://psanxiao.cartodb.com). Aquí están los resultados:

### Running

<iframe width="100%" height="520" frameborder="0" src="https://psanxiao.cartodb.com/viz/94e2802a-f439-11e5-b2d6-0ecfd53eb7d3/embed_map" allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen></iframe>

### Ciclismo

<iframe width="100%" height="520" frameborder="0" src="https://psanxiao.cartodb.com/viz/3bf14554-f43a-11e5-a35b-0ea31932ec1d/embed_map" allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen></iframe>

Por cierto, el propio Strava tiene [su propio heatmap](http://labs.strava.com/heatmap) global con todas las actividades que sube la gente.
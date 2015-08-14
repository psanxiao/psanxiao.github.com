---
layout: post
title: "Migrar el plugin de traducción en Wordpress"
description: ""
category: 
- Free Software
- Hows To
- Spanish
tags: []
---
{% include JB/setup %}

Hace poco he tenido que enfrentarme a la migración del plugin
de traducción de un [Wordpress](http://wordpress.org) en
producción. Aunque parece una tarea sencilla a priori, una vez
metido en faena la verdad es que no lo fue tanto. A continuación
dejo un resumen de los pasos que seguí.

### El motivo

Esta instalación de Wordpress estaba usando el plugin [WPML](https://wpml.org/es/), uno de los que se utilizan normalmente para esta tarea.
El problema, es que desde hace un tiempo, a partir de una determinada
versión este plugin ya no es gratuito y requiere la compra de
una licencia. La versión instalada en este caso era muy
antigua, y con la actualización a las últimas versiones de
wordpress empezaron a surgir los problemas. Como no se quería
pagar por la versión comercial de WPML, se optó por migrar a
[qTranslate X](https://wordpress.org/plugins/qtranslate-x/).

### El proceso

Antes de empezar con la migración, el primer paso fue crear
una copia exacta del Wordpress en producción para trabajar en
local y asegurarse que todo el proceso funcionaba correctamente.
Para ello podemos usar otro plugin, [Duplicator](https://wordpress.org/plugins/duplicator/) que crea un "instalable" de una instancia de Wordpress
que podemos instalar en cualquier otro servidor. El proceso es
sencillo y funciona muy bien. Hay muchos tutoriales en Internet
que nos dicen como usarlo, yo usé [este](http://ayudawp.com/como-migrar-tu-wordpress-de-hosting-usando-duplicator/).

Una vez que tenemos nuestra réplica, podemos trabajar tranquilos
en la migración. Para ello, tenemos que instalar tres plugins:

* El propio qTranslate X
* [qTranslate Slug](https://wordpress.org/plugins/w2q-wpml-to-qtranslate/)
que nos permitirá gestionar las url de las diferentes traducciones
* [WPML to qTranslate](https://wordpress.org/plugins/w2q-wpml-to-qtranslate/) 
que se encarga de migrar las entradas y páginas traducidas con WPML
al formato de qTranslate X

Una vez que tenemos todos los plugins instalados, debemos 
desactivar WPML y activar los tres que acabamos de instalar. Ahora
seguimos las opciones de WPML to qTranslate para migrar las
entradas y páginas. En mi caso la migración fue bastante bien, y
tan sólo fue necesario hacer algún pequeño ajuste manual en un
par de entradas. Una vez hecho esto es necesario ir a Ajustes ->
Idioma -> Import/Export y marcar las entradas como escritas en
el idioma por defecto. Este paso es necesario para que qTranslate X
carque la traducción correspondiente de cada entrada según el idioma
de la página.

### Otros

Llegados al punto anterior deberíamos tener la migración del contenido 
lista, sin embargo, dependiendo de la configuración y personalización
de la instalación de Wordpress, será necesario hacer algunos
ajustes a mayores. En mi caso, por ejemplo, tuve que volver a
crear los menús de la página, o cambiar el código que  
se usaba para detectar el idioma en algunos widgets personalizados.
En este caso, para ejecutar alguna línea de código específica cuan
el idioma es el Inglés, se haría así:

    $GLOBALS['q_config']['language']=="en"
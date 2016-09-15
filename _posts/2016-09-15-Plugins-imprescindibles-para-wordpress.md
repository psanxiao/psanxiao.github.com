---
layout: post
title: "Plugins imprescindibles para WordPress"
description: "Plugins imprescindibles para una instalación estándar de Wordpress"
category:
- Hows To 
tags: [wordpress, plugins]
---
{% include JB/setup %}

Aunque hace tiempo que dejé de usar WordPress en este blog, [para usar una solución más sencilla de mantener](http://psanxiao.com/new-psanxiao-dot-com), sigo pensando wordpress es una execelente herramienta para montar un blog personal o una página web, incluso si se quieren hacer cosas complejas. Sus opciones de personalización y la cantidade de temas y plugins disponibles hacen que se puedan hacer incluso portales web complejos.

He montado unas cuantas páginas web con wordpress y a día de hoy sigo mantiendo todía algunas. En este post quería comentar algunos plugins que considero imprescindbles en una instalación estándar, independientemente del uso que se le vaya a dar. Son plugins que cubren aspectos básicos como el rendimiento de la página, la seguridad o los backups. Para cada uso concreto hay cientos de listados de plugins que se pueden utilizar.

* [UpdraftPlus](https://es.wordpress.org/plugins/updraftplus/): Este es un plugin para hacer copias de seguridad de tu wordpress. Permite automatizar los backups tanto de los ficheros como de la base de datos y guardarlos tanto en el propio servidor (mala idea) como en servicios externos. Puedes guardar las copias de seguridad en tu cuenta de Dropbox, Google Drive, etc...

* [Wordfence Security](https://es.wordpress.org/plugins/wordfence/): Como su nombre da a entender se trata de un plugin de seguridad. Permite proteger y monitorizar tú instalación de wordpress de ataques externos. Permite bloquear IPs y detecta insercciones de código maligno en los ficheros. Aunque tiene una versión de pago con muchas opciones, la versión gratuita es más que suficiente en la mayoría de los casos.

* [Sucuri Security](https://es.wordpress.org/plugins/wordfence/): Este es otro plugin de seguridad, que se puede utilizar en lugar del anterior o como suelo hacer yo, combinándolos. Personalmente como plugin de seguridad me gusta más Wordfence, pero Sucuri facilita mucho la configuración inicial de una instalación nueva, automatizando tareas como la de ocultar la versión de wordpress por ejemplo. También es algo más efectivo en caso de *hackeo* limpiando archivos afectados.

* [P3(Plugin Performance Profiler)](https://es.wordpress.org/plugins/p3-profiler/): Entramos en el apartado de la optimización de rendimiento. Este plugin nos hace una auditoría del rendimiento de nuestra página, viendo cuanto tarde en cargar por ejemplo y diciéndonos que plugins la están relantizando. Importantísimo cuando instalamos plugins nuevos, para ver si lo que nos ofrecen en cuanto a funcionalidad no nos lo quitan en rendimiento.

* [WP Smush](https://es.wordpress.org/plugins/wp-smushit/): Las imágenes es uno de los puntos que más suele perjudicar el rendimiento de una página. Si eres de los que suben directamente imágenes que sacadas con una mega ultra cámara último modelo de millones de megapíxeles, sin editarla previamente este plugin se encarga de hacerlo por ti. Es capaz de ajustar el tamaño de las imágenes automáticamente para que se muestren sin pérdida de calidad pero con un rendimiento óptimo.

* [WP Optimize](https://es.wordpress.org/plugins/wp-optimize/): Este plugin se encarga de optimizar la base de datos de tu wordpress y hacer que vaya más rápido, punto. Instálalo! Básicamente se encarga de eliminar toda la *morralla* que se va acumulando en la base de datos como revisiones de entradas y páginas, comentarios spam, etc...

En el caso de un [wordpress multisite](https://codex.wordpress.org/Create_A_Network), sí wordpress puede hacer eso, hay un par de plugins que incluiría en la lista.

* [BackWPup](https://es.wordpress.org/plugins/backwpup/): Este más que incluírlo sería cambiarlo por el UpdraftPlus, ya que este permite hacer backups de todos los sitios directamente, sin tener que ir configurando los backups de forma independiente en cada uno de ellos.

* [Duplicate Theme](https://es.wordpress.org/plugins/duplicate-theme/): En un wordpress multisite cuando se instala un tema, esto se hace en el *site* principal y se activa para el resto. Esto hace que si lo personalizamos, las personalizaciones se replican en todos los *sites* que lo estén utilizando. Para conseguir una independencia entre ellos hay que duplicarlo y crear temas hijos, que es justo lo que hace este plugin, fácil no?

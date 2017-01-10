---
layout: post
title: "Sincronizar Suunto Ambit desde Ubuntu"
description: "Cómo sincronizar las actividades desde un reloj deportivo Suunto con Linux"
category: 
- Hows To
tags: [suunto, ubuntu, openambit]
---
{% include JB/setup %}

He tenido varios relojes deportivos con los que registro mis actividades de varias marcas, actualmente un [Suunto Ambit 2](http://www.suunto.com/es-ES/Productos/Relojes-deportivos/Suunto-Ambit2/Suunto-Ambit2-Silver/), y siempre me ha pasado lo mismo.

Si bien para ver las actividades todas las marcas tienen una aplicación web desde la que además puedes incluso hacer ajustes en el reloj o en el caso particular de Suunto instalar aplicaciones que va desarrollando la gente o crear rutas para ir las siguiendo después con el reloj. En principio sólo necesitas un navegador web por lo que puedes hacer todo esto desde un ordenador cualquiera o un dispositivo móvil, hasta aquí todo estupendo.

El problema viene con el paso intermedio, ¿cómo sincronizar los datos entre el reloj y la aplicación web? Para esto tanto Suunto como otras marcas ofrecen aplicaciones que se encargan de esto, y aquí es donde está el problema. Los usuarios de linux somos los grandes olvidados ya que las aplicaciones suelen estar disponibles sólo para Windows y macOS. Es una aplicación sencilla que lo único que hace es sincronizar los datos, todo lo demás se hace en la aplicación web, pero aún así no tienen una versión para linux.

Por suerte, al menos en el caso de Suunto, existe un proyecto de software libre que se llama [Openambit](http://openambit.org/) que nos ofrece a los usuarios de este sistema operativo lo que la marca nos niega, una pequeña aplicación nativa que sincroniza los datos del reloj y los sube a la plataforma de Suunto, [movescount](http://www.movescount.cn/es).

Para instalarla en Ubuntu sólo es necesario añadir un ppa e instalarla con APT:

    $ sudo apt-add-repository ppa:openambit/ppa
    $ sudo apt-get update
    $ sudo apt-get install openambit  

Llevo unos días probándola y la verdad es que funciona muy bien, reconoce el reloj sin problemas, sincroniza los datos y los envía a la plataforma de Suunto. Para esto último hay que introducir la cuenta de usuario en las preferencias de la aplicación, en un apartado específico llamado Movescount, eso nos llevará a la plataforma para que autoricemos la aplicación y listo.
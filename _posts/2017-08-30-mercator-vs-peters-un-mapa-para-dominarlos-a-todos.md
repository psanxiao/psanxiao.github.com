---
layout: post
title: "Mercator vs Peters: Un mapa para dominarlos a todos"
description: "Sobre proyecciones cartográficas y en particular los famosos mapas de Mercator y Peters"
category: 
- 12meses12mapas
tags: [mercator, peters, proyecciones, mapa, map]
---
{% include JB/setup %}

Descubrir que la Tierra no es exactamente como se ve en los mapas suele ser un pequeño shock. Una vez recuperado de la impresión inicial, se empieza a analizar y digerir el por qué, y es entonces cuando aparece el nombre de Mercator y las proyecciones.

Posteriormente, una vez [asimilado el tema de las proyecciones](http://www.educ.ar/sitios/educar/recursos/ver?id=20029), o bien dejado por imposible, suele llegar la fase en la que se indaga en los motivos sobre el por qué de usar la proyección de Mercator, y entonces inevitablemente surge la idea de la hegemonía de Europa, de la visión centralista, del Norte sobre el Sur, etc... e inevitablemente también aparece a colación el mapa de Peters, como supuestamente el "mapa de verdad". 

Sin embargo, ningún mapa es real en realidad, no hay un mapa que sea verdad y otros que sean mentira, todos son igual de verdad e igual de mentira a la vez. 

### Las proyecciones

Pero empecemos por el principio. El gran problema con el que se enfrentan los cartógrafos al hacer mapas es como presentar en una superficie plana de dos dimensiones un elemento, la Tierra, que tiene tres dimensiones. Esto de partida es un problema imposible de resolver, así que hay que ir dando pasos para simplificarlo. El primero de ellos es asimilar la tierra a una esfera, sí sabemos que la tierra es redonda, pero no es una esfera perfecta ni mucho menos. La visión esférica de las imágenes desde el espacio es simplemente fruto de la perspectiva, [pero en realidad nuestro planeta se parece más a una patata que a una esfera](http://www.esa.int/esl/ESA_in_your_country/Spain/GOCE_muestra_el_campo_gravitatorio_terrestre_con_un_nivel_de_detalle_sin_precedentes).

Esa primera simplificación hace que se puedan buscar formas geométricas sobre las que es posible proyectar el contenido de una esfera y luego trasladarlo a un plano, en función de la forma geométrica elegida la representación en el plano variará, cilíndrica, circular, cuneiforme... y la deformación será distinta, más acusada en los tamaños o en las formas, dependiendo de la transformación elegida, pero desde luego nunca reflejará exactamente la realidad.

¿De dónde viene entonces la "polémica"?

### El mapa (proyección) de Mercator

La controversia con la proyección de Mercator viene motivada por la relación de tamaño entre países y continentes, ya que mientras Europa se mantiene en sus proporciones más o menos reales, Sudamérica y sobre todo África aparecen mucho más pequeñas de lo que en realidad son. También llama la atención sobre todo Groenlandia o la Antártida que aparecen como pedazos de tierra enormes, sobre todo la primera que casi parece igual de grande que África.

![mapa-mercator](/assets/images/posts/mercator-map.jpg)

El motivo técnico de todo esto es que se trata de una proyección cilíndrica y por tanto las zonas cercanas al Ecuador son las que conservan mejor su proporciones reales, si creas un cilindro con una cartulina y rodeas un globo terráqueo es fácil ver que las partes del ecuador que tocan la cartulina quedarán mejor plasmadas al proyectarse, mientras que las partes más alejadas sufrirán más distorsión. Esto es precisamente lo que pasa con Groenlandia, África o Sudamérica.

Esta proyección nación en el año 1549, en pleno apogeo de viajes comerciales entre Europa y América, y precisamente este mapa lo que permite es crear fácilmente rumbos de navegación y fundamentalmente para eso empezó a usarse, si bien es cierto que Mercator la usaba también para otros mapas que no eran de navegación, pero quien lo culpa, si inventas algo ¿no serías el primero en usarlo para todo?.

Por los motivos que sea esa proyección se convirtió en la más popular hasta nuestros días, y la gran mayoría de mapas que vemos están hechos con esa proyección, incluso si abrimos *Google Maps* u otro servicio de mapas online nos encontramos con una pequeña variante de la proyección de Mercator. Algunos desarrolladores de estos servicios justifican el uso de esta proyección por motivos técnicos, ya que en cualquier punto del planeta las direcciones norte-sur son siempre verticales y las este-oeste horizontales, además es una proyección *conforme* lo que hace que no se distorsionen por ejemplo las formas de los edificios.

Otro de los puntos de controversia es lo que se ha llamado la versión eurocentrista del mundo. Se supone que en el mapa de Mercator Europa aparece justo en el centro, como si estuviese en el ecuador de la Tierra, cuando en realidad sabemos que está mucho más al norte. Esto en realidad es un error, ya que como se ve en la imagen, Europa no aparece en el centro de la proyección de Mercator, lo que pasa es que esta versión completa no se suele utilizar mucho sino que la que se usa es una versión simplificada que queda digamos más bonita al comprimir la parte de océanos y parte de la Antártida.

### El mapa (proyección) de (Gall) Peters

Como respuesta a esta supuesta versión interesada del mundo eurocentrista o de supremacía del norte sobre el sur, en 1970 aparece el mapa de Peters. Arno Peters era historiador, aficionado a la cartografía, y cuando presentó su proyección dejó claro que lo que buscaba era terminar con eso, ya que así veía él el mapa de Mercator, como una visión de la supremacía de Europa frente a sus colonias.

![mapa-facebook](/assets/images/posts/peters-map.jpg)

Desde el punto de vista cartográfico, su proyección fue más que discutida, primero porque no había sido el primero en inventarla, ya que en 1855 un reverendo escocés llamado James Gall ya había presentado una proyección a efectos prácticos idéntica a la de Peters, por eso hoy en día se debe hablar de la proyección de Gall-Peters y no sólo de Peters. Pero además de eso, desde el punto de vista más técnico muchos análisis de expertos en la materia revelaron muchos defectos en su proyección, la supuesta afirmación de que en esta proyección la escala y la distancia están correctamente representadas es falsa ya que matemáticamente es imposible. Mirando con detalle hay aberraciones, considerándolas así con la misma vara de medir que en el caso de Mercator, así por ejemplo Nigeria o Chad aparecen el doble de largos de lo que son en realidad. 

Sin embargo, el conjunto del mapa y la visión que proyecta junto con el discurso de Peters invita cuanto menos a la reflexión o a la duda. Su proyección en realidad no tienen ninguna utilidad técnica, como sí la tenía la de Mercator, no se pueden calcular distancias y tampoco sirve para navegar, por ejemplo, sin embargo sirve para invitar a pensar. Peters era historiador y se había especializado en la utilización propagandística de los mapas en las guerras, sobre todo durante la segunda guerra mundial, y seguramente en parte esto lo marcó y le ayudó para presentar su mapa como lo hizo y lograr un enorme impacto. Durante los años siguientes a su presentación se distribuyeron millones de copias, promocionado sobre todo por ONGs y diferentes organizaciones. La UNESCO lo adoptó como propio y Unicef publicó más de 60 millones de copias con el eslogan "Nuevas dimensiones, condiciones justas". Para todas estas organizaciones fue una herramienta sin duda, no en lo técnico sino en lo político y propagandístico, para reforzar su labor y despertar pensamientos en la gente sobre un mundo más justo.

### Una proyección para dominarlas a todas

Seguramente desde este último punto de vista la proyección de Gall-Peters se pueda considerar como algo positivo pero hay que aislar esto de todo lo demás. Las proyecciones cartográficas, sea cual sea, no son una representación real del mundo, no pueden serlo porque matemáticamente es imposible. Incluso la proyección de [Winkel-Tripel](https://es.wikipedia.org/wiki/Proyecci%C3%B3n_de_Winkel-Tripel) considera técnicamente como una de las que mejor representa el mundo y avalada por la *National Geographic Society* es incapaz de mostrar exactamente el mundo tal y como es en la realidad.

Las proyecciones cartográficas son instrumentos que nos ayudan a crear mapas, con los que resolvemos problemas, navegar, orientarnos, medir distancias, etc... incluso nos permiten crear mapas con los que presentar ideas, contar historias, mostrar datos o cualquier otro uso que se nos ocurra.

Si el mapa de Mercator tenía una intención de demostrar cierta hegemonía o no, es algo que no sabemos, fuera esa intención u otra lo cierto es que somos nosotros los que le damos la interpretación que queremos a los mapas. Pero lo cierto es que la proyección de Mercator no es ni mejor ni peor que la de Gall-Peters, sino que es diferente, igual que ambas lo son con respecto a las demás, lo único que tienen todas en común es que **ninguna representa la realidad tal y como es**.







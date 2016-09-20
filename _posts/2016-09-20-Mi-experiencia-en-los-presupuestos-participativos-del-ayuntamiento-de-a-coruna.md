---
layout: post
title: "Mi experiencia en los presupuestos participativos del ayuntamiento de A Coruña"
description: "Resumen y reflexiones de la participación en los presupuestos del ayuntamiento de A Coruña"
category: 
- Free Software
tags: [participación, software libre, migración]
---
{% include JB/setup %}

Desde el pasado lunes 19 y hasta el próximo día 30 de Septiembre está abierta la votación para la fase final de propuestas en los [presupuestos participativos](https://aportaaberta.coruna.es/) del ayuntamiento de A Coruña. [La propuesta que yo había hecho](http://psanxiao.com/Propuesta-migracion_software-libre-ayuntamiento-corunha) en su día sobre [un piloto de migración a Software Libre de la administración](https://aportaaberta.coruna.es/participatory_budget/investment_projects/156), es una de las que está incluida en esta fase final. Aunque quedan unos cuantos días aún para saber los resultados definitivos, creo que es un buen momento para revisar el proceso en sí.

### Abrir los presupuestos a la ciudadanía

Sin duda esta tarea en sí no es fácil, aunque creo que muy necesaria y por eso tengo que empezar con un reconocimiento a este gobierno por llevarla a cabo. Es una oportunidad de poder opinar directamente sobre en que se debería gastar el dinero público, con todo lo que ello conlleva, y desde luego gestionarlo no debe ser tarea sencilla. No sabría decir si la participación ha sido alta o no, mi sensación es que no, pero como siempre esto es relativo. [Al parecer la primera fase, en la que se registraron 362 ideas, tuvieron en total 13.000 votos, habiéndose registrado en la plataforma 1.200 personas](http://www.laopinioncoruna.es/coruna/2016/07/19/participacion-13000-votos/1089886.html).
Comparando con la iniciativa original [Decide Madrid](http://decide.madrid.es), ésta [tuvo 100.000 personas inscritas y un millón de visitas en los seis primeros meses de vida](http://www.lainformacion.com/politica/elecciones/participacion-ciudadana-Decide-Madrid-registradas_0_897810657.html). A priori no parecen números emocionantes, sobre el 2,5% de la población en Madrid y casi el 0,5% en A Coruña no parecen grandes datos, aunque se tratan de iniciativas novedosas y quizás los números los hay que ver a más largo plazo.

### La plataforma

La plataforma web, [A Porta Aberta](https://aportaaberta.coruna.es/), es la misma que se desarrolló para Decide Madrid, [Consul](https://github.com/consul/consul), que es software libre y ha sido reutilizada en este caso adaptándola al caso de A Coruña. Como ya les comenté en su día a los responsables, hay un pequeño problema de cumplimiento de licencia. Consul es AGPL y esta licencia tiene la particularidad de obligar a que si la herramienta se usa en una red de ordenadores, tiene que ponerse a disposición de cualquier usuario potencial el código fuente. En el pie de página aparece el *link* al código fuente de Consul, pero como ha habido pequeñas adaptaciones, éstas deberían estar compartidas también y aunque están disponibles en un [repositorio público](https://github.com/ConcelloCoruna/aportaaberta), no están enlazadas desde la plataforma como deberían. 

Problemas de licencias a parte, la plataforma es sencilla de usar y cumple su función, sobre todo en la primera fase, en la que simplemente se dan de alta propuestas y se le dan "apoyos", que vienen a ser un "me gusta" para entendernos. Para dar de alta una propuesta sólo hay que escribir una pequeña descripción, no es necesaria una valoración económica por ejemplo, de eso se encargará el equipo municipal en la siguiente fase. Se pueden hacer comentarios dentro de las propuestas y se puede enlazar información adicional incluyendo un *link* de Internet, no se pueden subir documentos ni ficheros.

### Análisis de las propuestas y votación final

Una vez que terminó la fase de crear propuestas y apoyarlas, éstas se analizaron por parte de los técnicos municipales para estudiar su viabilidad y cuantificarlas económicamente. Justo antes de empezar la fase final de votación, recibo un correo en el que me dicen que va a empezar la fase final de votación. Miro y la propuesta estaba incluida, pero no me lo comunicaron ni me enviaron el informe técnico de la misma donde entiendo se incluirá la valoración económica. En la propuesta sólo hay un párrafo nuevo que hace mención a ese informe técnico y dice que es una propuesta viable y como se va a llevar a cabo, además se incluye el importe total que han estimado para la misma.

Sobre esto varias cosas. Lo primero es que yo esperaba un contacto previo, y si han elaborado un informe técnico para cada propuesta esperaba que lo enviasen antes de empezar la fase de votación, por ejemplo en mi caso, como explicaré luego, el informe técnico cambia totalmente la propuesta y lo que dicen que van a hacer no es lo que yo había propuesto. En el apartado económico sólo hay un número, pero tampoco sé en base a qué ni que aspectos cubre ese presupuesto.

Además, a través de otra propuesta que había hecho y que en este caso se rechazó por no alcanzar el número mínimo de apoyos, me entero que este número mínimo es de 26, pero no hay ninguna explicación de donde sale, entiendo que no será aleatorio y que saldrá de alguna fórmula, pero no he encontrado en ningún sitio ninguna información al respecto.

La forma de votar las propuestas sí me ha gustado. La parte del presupuesto que se va a confeccionar con estos presupuestos participativo es 1 millón de euros, así que para votar debes imaginarte que tienes 1 millón de euros y elegir propuestas hasta alcanzar esa cantidad. Me gusta porque te obliga a priorizar y a ponerse en la piel de alguien que tiene que gestionar lo público, que a veces pensamos que desde esa posición se puede hacer cualquier cosa y al final detrás de todo siempre está el dinero, que es finito.

### Mi propuesta de migración a Software Libre

Como decía, según el informe técnico, la manera de ejecutar mi propuesta la cambia totalmente y ya no es mi propuesta en realidad. Yo proponía llevar a cabo un piloto de migración del puesto de funcionario, empezando por un subconjunto. Revisando documentación sobre procesos similares, en todos me encontré con algo así. La idea del piloto es identificar roles de usuario, problemas que puedan surgir, necesidades, elegir un conjunto de aplicaciones que cubran esas necesidades... todo esto con un grupo acotado y manejable, que hace más fácil el proceso para que cuando se expanda a toda la administración todo sea más sencillo.

Sin embargo, lo que proponen los técnicos municipales es realizar el piloto en los puestos de uso público de una biblioteca o centro cívico!. Esto no tiene sentido, los puestos de uso público de una biblioteca no son puestos de funcionario, no se pueden analizar necesidades ni identificar roles de usuario, no se puede en definitiva aplicar nada de esa migración al proceso de migración de la administración. Si bien tiene lógica que los puestos de uso público estén también en software libre, no era para nada esto la idea de la propuesta.

Me he puesto en contacto con el ayuntamiento para comentarlo, pero me da la sensación de que esto va a quedar así, ya que estamos en fase de votación.Espero que al menos todo esto sirva para que el proceso mejore, porque si bien esta iniciativa es ilusionante, tengo la duda de si realmente todos, ciudadanos y administración estábamos preparados para llevarla a cabo.


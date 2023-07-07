# __METODO DE THOMPSON__
---

|El algoritmo Thompson (también conocido como método de Thompson) fue creado por Ken Thompson y Dennis Ritchie, se utiliza para obtener autómatas finitos no deterministas(AFND)a partir de expresiones regulares (ER).|![](imagenes/td.jpg)|
|:--:|:--:|

## __ALGORITMO__
El algoritmo está orientado a la sintaxis, ya que recorre en forma recursiva hacia arriba el árbo sintáctico para la expresión regular. Para cada subexpresión, el algoritmo construye un AFN con _un solo estado aceptante_.

## __a__
>![](imagenes/ta.svg)
## __ε__
>![](imagenes/tb.svg)
## __a.b__
>![](imagenes/tc.svg)
## __a|b|c__
>![](imagenes/td.svg)
## __a+__
>![](imagenes/te.svg)
## __a*__
>![](imagenes/tf.svg)
## __a?__
>![](imagenes/tg.svg)

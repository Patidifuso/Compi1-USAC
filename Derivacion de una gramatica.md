# __PARCIAL 2__
---
## __ENTRADA__
```sh
( id + id * id ) + ( id + id * id )
```
## __GRAMATICA__
```sh
E -> E + T 
E -> T 
T -> T * F
T -> F
F -> ( E )
F -> id
```
## __DERIVACION POR LA IZQUIERDA__
```sh
E -> E + T
E -> T + T
E -> F + T
E -> ( E ) + T
E -> ( E + T ) + T
E -> ( T + T ) + T
E -> ( F + T ) + T
E -> ( id + T ) + T
E -> ( id + T * F ) + T
E -> ( id + F * F ) + T
E -> ( id + id * F ) + T
E -> ( id + id * id ) + T
E -> ( id + id * id ) + F
E -> ( id + id * id ) + ( E )
E -> ( id + id * id ) + ( E + T )
E -> ( id + id * id ) + ( T + T )
E -> ( id + id * id ) + ( F + T )
E -> ( id + id * id ) + ( id + T )
E -> ( id + id * id ) + ( id + T * F )
E -> ( id + id * id ) + ( id + id * F )
E -> ( id + id * id ) + ( id + id * id )
```
## __DERIVACION POR LA DERECHA__
```sh
E -> E + T
E -> E + F
E -> E + ( E )
E -> E + ( E + T )
E -> E + ( E + T * F )
E -> E + ( E + T * id )
E -> E + ( E + F * id )
E -> E + ( E + id * id )
E -> E + ( T + id * id )
E -> E + ( F + id * id )
E -> E + ( id + id * id )
E -> T + ( id + id * id )
E -> F + ( id + id * id )
E -> ( E ) + ( id + id * id )
E -> ( E + T ) + ( id + id * id )
E -> ( T + T ) + ( id + id * id )
E -> ( T + T * F ) + ( id + id * id )
E -> ( T + T * id ) + ( id + id * id )
E -> ( T + F * id ) + ( id + id * id )
E -> ( T + id * id ) + ( id + id * id )
E -> ( F + id * id ) + ( id + id * id )
E -> ( id + id * id ) + ( id + id * id )
```


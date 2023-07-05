# __SEGUNDO PARCIAL COMPI 1__
## __Gramatica__
```sh
G -> G P
G -> prod flecha L 
P -> prod flecha L
P -> pipe L
L -> L , id
L -> firstid 
```

## __Quitar recursividad__
```sh
S -> G
G -> prod flecha L G'
G' -> P G'
G' -> ''
P -> prod flecha L
P -> pipe L
L -> firstid L'
L' -> id , L'
L' -> ''
```

## __Calculo de primeros y siguientes__

| Gramatica             | Primeros | Siguientes |
| S -> G                | P(S)  = P(G)     = { prod          } | S(S) = |
| G -> prod flecha L G' | P(G)  =            { prod          } | S(G) = |
| G' -> P G'            | P(G') = P(P) U ε = { prod, pipe, ε } | S(G') =  |
| G' -> ε               |                                      |  |
| P -> prod flecha L    | P(P)  =            { prod, pipe    } | S(P) = P(G') = { prod, pipe } |
| P -> pipe L           |                                      |  |
| L -> firstid L'       | P(L)  =            { firstid       } | S(L) = |
| L' -> id , L'         | P(L') =            { id, ε         } | S(L') = |
| L' -> ε               |                                      |  |













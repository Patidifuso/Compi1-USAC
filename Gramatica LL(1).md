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

| Gramatica             | Primeros                             | Siguientes                                           |
|-----------------------|--------------------------------------|------------------------------------------------------|
| S -> G                | P(S)  = P(G)=      { prod          } | S(S)  =                                        { $ } |
| G -> prod flecha L G' | P(G)  =            { prod          } | S(G)  = S(G) =                                 { $ } |
| G' -> P G'            | P(G') = P(P) U ε = { prod, pipe, ε } | S(G') = S(G) U S(G') =                         { $ } |
| G' -> ε               |                                      |                                                      |
| P -> prod flecha L    | P(P)  =            { prod, pipe    } | S(P) = (P(G') - ε) U S(G') =       { prod, pipe, $ } |
| P -> pipe L           |                                      |                                                      |
| L -> firstid L'       | P(L)  =            { firstid       } | S(L) = (P(G') - ε) U S(G) U S(P) = { prod, pipe. $ } |
| L' -> id , L'         | P(L') =            { id, ε         } | S(L') = S(L) U S(L') =             { prod, pipe. $ } |
| L' -> ε               |                                      |                                                      |

## __Tabla de analisis predictivos__
| No terminales | produccion            | flecha | pipe        | firstid         | id            | , | $       |
|---------------|-----------------------|--------|-------------|-----------------|---------------|---|---------|
| S	            | S -> G                |        |             |                 |               |   |         |
| G	            | G -> prod flecha L G' |        |             |                 |               |   |         |
| G'            | G' -> P G'            |        | G' -> P G'  |                 |               |   | G' -> ε |
| P	            | P -> prod flecha L    |        | P -> pipe L |                 |               |   |         |
| L	            |                       |        |             | L -> firstid L' |               |   |         |
| L'            | L' -> ε               |        | L' -> ε     |                 | L' -> id , L' |   | L' -> ε |
















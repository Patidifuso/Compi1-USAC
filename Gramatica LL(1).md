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
| --------------------- | -------- | ---------- |
| S -> G                |||
| G -> prod flecha L G' |||
| G' -> P G'            |||
| G' -> ε               |||
| P -> prod flecha L    |||
| P -> pipe L           |||
| L -> firstid L'       |||
| L' -> id , L'         |||
| L' -> ε               |||













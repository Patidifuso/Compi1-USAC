# __Tercer Parcial__
## __Gramatica__
```sh
S -> X
X -> W W
W -> ( X )
W -> 34 W
W -> 25
```


## __LR(1)__
```sh
(R0) S -> X
(R1) X -> W W
(R2) W -> ( X )
(R3) W -> 34 W
(R4) W -> 25
```

## __E0__
```sh
(d0) S -> .X        [ $ ]
(d1) X -> .W W      [ $ ]
(d2) W -> .( X )    [ ( | 3 | 2 ] 
(d3) W -> .34 W     [ ( | 3 | 2 ]
(d4) W -> .25       [ ( | 3 | 2 ]
```

## __E1( 0, X )__
```sh
(R0) S -> X.        [ $ ]
```

## __E2( 0, W )__
```sh
(d6) W -> W. E      [ $ ]

```

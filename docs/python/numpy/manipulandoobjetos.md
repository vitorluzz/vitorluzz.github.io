

### Manipulando objetos 3D e 4D em NumPy

#### 3 Dimensões

Criando um array de 3 dimensões:
```python title='python'

arr_3d = np.array([
    [
        [1, 2, 3, 4],
        [5, 6, 7, 8],
        [9, 10, 11, 12]
    ],
    [
        [13, 14, 15, 16],
        [17, 18, 19, 20],
        [21, 22, 23, 24]
    ]
])

print(arr_3d)
```
```python title='out:'
     [[[ 1  2  3  4]
       [ 5  6  7  8]
       [ 9 10 11 12]]
   
      [[13 14 15 16]
       [17 18 19 20]
       [21 22 23 24]]]
```

***
ㅤ

Vamos saber o número de dimensões de um objeto:
```python title='python'

arr_3d.ndim
```
```python title='out:'
3
```

***
ㅤ

Sabendo a forma (shape) da array:
```python title='python'

print(arr_3d.shape)
```
```python title='out:'
(2, 3, 4)
```
>2 elementos, com 3 linhas e 4 elementos em cada linha.

ㅤ
***


#### 4 Dimensões
Criando um array de 4 dimensões:
```python title='python'

arr_4d = np.array([
    [
        [
            [1, 2, 3, 4, 5],
            [6, 7, 8, 9, 10],
            [11, 12, 13, 14, 15],
            [16, 17, 18, 19, 20]
        ],
        [
            [21, 22, 23, 24, 25],
            [26, 27, 28, 29, 30],
            [31, 32, 33, 34, 35],
            [36, 37, 38, 39, 40]
        ],
          [
            [1, 2, 3, 4, 5],
            [6, 7, 8, 9, 10],
            [11, 12, 13, 14, 15],
            [16, 17, 18, 19, 20]
        ]
    ],
    [
        [
            [41, 42, 43, 44, 45],
            [46, 47, 48, 49, 50],
            [51, 52, 53, 54, 55],
            [56, 57, 58, 59, 60]
        ],
        [
            [61, 62, 63, 64, 65],
            [66, 67, 68, 69, 70],
            [71, 72, 73, 74, 75],
            [76, 77, 78, 79, 80]
        ],
          [
            [1, 2, 3, 4, 5],
            [6, 7, 8, 9, 10],
            [11, 12, 13, 14, 15],
            [16, 17, 18, 19, 20]
        ]
    ]
])

print(arr_4d)
```
```python title='out:'
     [[[[ 1  2  3  4  5]
        [ 6  7  8  9 10]
        [11 12 13 14 15]
        [16 17 18 19 20]]
     
       [[21 22 23 24 25]
        [26 27 28 29 30]
        [31 32 33 34 35]
        [36 37 38 39 40]]
     
       [[ 1  2  3  4  5]
        [ 6  7  8  9 10]
        [11 12 13 14 15]
        [16 17 18 19 20]]]
     
     
      [[[41 42 43 44 45]
        [46 47 48 49 50]
        [51 52 53 54 55]
        [56 57 58 59 60]]
     
       [[61 62 63 64 65]
        [66 67 68 69 70]
        [71 72 73 74 75]
        [76 77 78 79 80]]
     
       [[ 1  2  3  4  5]
        [ 6  7  8  9 10]
        [11 12 13 14 15]
        [16 17 18 19 20]]]]
```

***
ㅤ

Sabendo o número de dimensões do array:
```python title='python'

arr_4d.ndim
```
```python title='out:'
4
```

***
ㅤ

Sabendo a forma (shape) da array
```python title='python'

print(arr_4d.shape)
```
```python title='out:'
(2, 3, 4, 5)
```
>Ele está nos dizendo que é:
>      
>     2 blocos:
>         com 3 estruturas cada um:
>             com 4 linhas em cada estrutura:
>                  com 5 elementos em cada linha.
>


***
ㅤ


##### Fatiamento de um Array de 4 Dimensões (SLICING)

> Como estamos manipulando um elemento de 4 dimensões, precisamos defiir qual bloco, qual estrutura, qual linha e qual elemento

*[bloco, estrutura, linha, elemento]*


***



Retornando o elemento, do bloco de índice 0, na estrutura de índice 2, na linha de índice 1, todos os elementos (Como não foi específicado o elemento, ele retorna a linha inteira!)
```python title='python'

arr_4d[0,2,1]
```
```python title='out:'
arr_4d[0,2,1,4]
```

***


Retornando o elemento de bloco de índice 0, na estrutura de índice 2, na linha de índice 1, o elemento de índice 4
```python title='python'

arr_4d[0,2,1,4]
```
```python title='out:'
10
```

ㅤ

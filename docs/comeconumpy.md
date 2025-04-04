# Numpy - Python

>O NumPy (Numerical Python) é uma biblioteca fundamental para computação numérica em Python. Ele fornece suporte para arrays multidimensionais de alta performance e funções matemáticas otimizadas para operações nesses arrays. Extremamente utilizado em análise de dados!

Primeiros passos
Importando o numpy

```
python


import numpy as np
```
***


Criando uma Array NumPy a partir de uma lista python!
```
python

arr1 = np.array([10,21,32,43,48,15,76,57,89])
```
***

O tipo dele será array numpy
```
python

type(arr1)
```
```
out: numpy.ndarray
```
***


A função shape, nos retorna as dimensões do objeto,
Ela irá me retornar que ele é um array comum, unilateral 
```
python

arr1.shape
```
```
out: (9,)
```

>O array numpy nos permite criar um array de múltiplas dimensões, diferente das listas comum, ele nos deixa ter um objeto n-dimensional. São muito mais eficientes que as listas de dados para armazenar e manipular grandes quantidades de dados. Eles são implementados em linguagem C e nos permitem muitas otimizações de desempenho. 
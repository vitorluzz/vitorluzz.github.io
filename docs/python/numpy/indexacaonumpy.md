

## Indexação em Arrays NumPy

>**LEMBRETE: A INDEXAÇÃO EM PYTHON COMEÇA POR 0**
ㅤ

Printando os elementos da array
```python title='python'

print(arr1)
```
```python title='out:'
[10, 21, 32, 43, 48, 15, 76, 57, 89]
```
ㅤ

***


Para indexar um array numpy utilizamos os colchetes:
```python title='python'

arr1[4]
```
```python title='out:'
48
```
ㅤ
***



Podemos retornar uma lista com os elementos desejados:
No exemplo abaixo, o índice 4 não entra pois ele é EXCLUSIVO!
```python title='python'

arr1[1:4]
```
```python title='out:'
array([21, 32, 43])
```

***

Caso queira que o índice 4 entre podemos fazer dessa forma:
```python title='python'

arr1[1:4+1]
```
```python title='out:'
array([21, 32, 43, 48])
```
***
ㅤ

Podemos procurar os índices de uma array através de uma lista de índices!
```python title='python'

# Criando uma lista de índices:
indices = [1,2,5,6]

# Procurando os índices do array a partir de uma lista de índices!
arr1[indices]
```
```python title='out:'
array([21, 32, 15, 76])
```

***
ㅤ

Podemos fazer uma máscara para verificar se os elementos de um array são pares
```python title='python'

mask = (arr1 % 2 == 0)
print(mask)

```
```python title='out:'
array([ True, False,  True, False,  True, False,  True, False, False])
```

***
ㅤ

Ou então, passar a máscara como parâmentro do índice!
```python title='python'

arr1[mask]
```
```python title='out:'
array([10, 32, 48, 76])
```

***
ㅤ

Podemos alterar o valor de um elemento por um índice específico
```python title='python'

arr1[0] = 100
arr1
```
```python title='out:'
array([100,  21,  32,  43,  48,  15,  76,  57,  89])
```

***

ㅤ

Diferente das listas python, um array numpy não aceita valores diferentes, não tendo a dinâmicidade das listas python uma vez que, uma array é de inteiros, não irá aceitar valores diferente de inteiros!

```python title='python'

try:
    arr1[0] = 'batatinha'
except:
    print('Erro! Operação não permitida!')
```
```python title='out:'
Erro! Operação não permitida!
```

***

ㅤ

Diferente das listas python, o range não pode ser utilizado nas arrays, no lugar deles, usamos o arange, semelhante ao range, criamos uma progressão aritmética a partir de um intervalo (start, stop, step)
```python title='python'

arr2 = np.arange(0,50,5)
```
```python title='out:'
0, 5, 10, 15, 20, 25, 30, 35, 40, 45
```

***

ㅤ

Podemos criar um array preenchido com zeros, chamamos a função zeros e definimos quantos elementos vamos querer:
```python title='python'

arr3 = np.zeros(10)
print(arr3)
```
```python title='out:'
[0. 0. 0. 0. 0. 0. 0. 0. 0. 0.]
```

ㅤ
***


**As arrays tem posições horizontais e verticais.**
 Com a função eye, podemos definir que queremos uma array, de tamanho vertical a ser determinado, contendo 0 e 1 nas diagonais dele:
```python

arr5 = np.eye(3)
print(arr5)
```
```python title='out:'
    [[1. 0. 0.]
     [0. 1. 0.]
     [0. 0. 1.]]
```

***
ㅤ

Podemos definir um array como argumento da função diagonal, e então falar que iremos preencher as diagonais com valores específicos de outro array numpy
```python title='python'

arr6 = np.diag(np.array([1,2,3,4]))
print(arr6)
```
```python title='out:'
    [[1 0 0 0]
     [0 2 0 0]
     [0 0 3 0]
     [0 0 0 4]]
```

***
ㅤ

Arrays Numpy aceitam diversos valores, como inteiros, floats, strings, booleanos...
```python title='python'

arr7 = np.array([True, False, False, True])
print(arr7)
```
```python title='out:'
[ True, False, False, True]
```


***
ㅤ


```python title='python'

arr8 = np.array(['Linguagem Python', 'Linguagem R', 'Linguagem Julia'])
print(arr8)
```
```python title='out:'
['Linguagem Python', 'Linguagem R', 'Linguagem Julia']
```


ㅤ

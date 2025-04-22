
## Manipulação de Arrays
Criando um array
```python title='python'

arr23 = np.arange(10)
arr23
```

***


<br>

Buscando o elemento de menor valor em um array:
```python title='python'

arr23.min()
```
```python title='out:' 
0
```


***


<br>


Buscando o elemento de maior valor em um array:
```python title='python'

arr23.max()
```
```python title='out:' 
9
```

***


<br>


Atribuindo um valor em cada um dos elementos do array
```python title='python'

np.array([1,2,3]) + 1.5
```
```python title='out:' 
array([2.5, 3.5, 4.5])
```

***


<br>


Criando um array com valores decimais
```python title='python'

arr24 = np.array([1.2,1.5,1.6,2.5,3.5,4.5])
```

Arredondando os valores (Acima de 0.5, o arredondamento será para cima!)
```python title='python'

arr25 = np.around(arr24)
print(arr25)
```
```python title='out:' 
array([1., 2., 2., 2., 4., 4.])
```

***


<br>



**Flatten**

>Usado para criar uma cópia unidimensional (achatada) de um array multidimensional. Basicamente: ele cria uma cópia do array multidimensional em um novo unidimensional, contendo todos os valores do array original porém em uma linha só, seguindo a mesma ordem de elementos.

Criando um array com 2 dimensões:
```python title='python'

arr26 = np.array(([1,2,3,4], [5,6,7,8]))
```

Deixando o array achatado:
```python title='python'

arr27 = arr26.flatten()
arr27
```
```python title='out:' 
array([1, 2, 3, 4, 5, 6, 7, 8])
```

***


<br>


Criando um array com 3 elementos
```python title='python'

arr28 = np.array([1,2,3])
```

***


<br>





Repetindo os elementos de um array determinadas vezes
```python title='python'

np.repeat(arr28, 3)
```
```python title='out:' 
array([1, 1, 1, 2, 2, 2, 3, 3, 3])
```

***


<br>





Criando um array:
```python title='python'

arr29 = np.array([5,6])
```


***




Fazendo a cópia de um array:
```python title='python'

arr30 = np.copy(arr29)`
print(arr30)
```
```python title='out:' 
array([5,6])
```

***


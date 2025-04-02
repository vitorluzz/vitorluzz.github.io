
## Manipulação de Arrays
Criando um array
```
python

arr23 = np.arange(10)
arr23
```
<br>
Buscando o elemento de menor valor em um array:
```
python

arr23.min()
```
```
out: 0
```

<br>

Buscando o elemento de maior valor em um array:
```
python

arr23.max()
```
```
out: 9
```
<br>

Atribuindo um valor em cada um dos elementos do array
```
python

np.array([1,2,3]) + 1.5
```
```
out: array([2.5, 3.5, 4.5])
```
<br>

Criando um array com valores decimais
```
python

arr24 = np.array([1.2,1.5,1.6,2.5,3.5,4.5])
```

Arredondando os valores (Acima de 0.5, o arredondamento será para cima!)
```
python

arr25 = np.around(arr24)
print(arr25)
```
```
out: array([1., 2., 2., 2., 4., 4.])
```
<br>


**Flatten**

>Usado para criar uma cópia unidimensional (achatada) de um array multidimensional. Basicamente: ele cria uma cópia do array multidimensional em um novo unidimensional, contendo todos os valores do array original porém em uma linha só, seguindo a mesma ordem de elementos.

Criando um array com 2 dimensões:
```
python

arr26 = np.array(([1,2,3,4], [5,6,7,8]))
```

Deixando o array achatado:
```
python

arr27 = arr26.flatten()
arr27
```
```
out: array([1, 2, 3, 4, 5, 6, 7, 8])
```
<br>

Criando um array com 3 elementos
```
python

arr28 = np.array([1,2,3])
```
<br>

Repetindo os elementos de um array determinadas vezes
```
python

np.repeat(arr28, 3)
```
```
out: array([1, 1, 1, 2, 2, 2, 3, 3, 3])
```
<br>

Criando um array:
```
python

arr29 = np.array([5,6])
```

Fazendo a cópia de um array:
```
python

arr30 = np.copy(arr29)`
print(arr30)
```
```
out: array([5,6])
```

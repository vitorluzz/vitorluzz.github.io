
## Manipulando Matrizes

Uma **matriz NumPy** (ou numpy.ndarray) é uma **estrutura de dados multidimensional** otimizada **para armazenar e operar com grandes quantidades de dados numéricos de maneira eficiente.** Ela pertence à biblioteca NumPy, que é amplamente utilizada em computação científica, aprendizado de máquina, análise de dados e muitas outras áreas.


ㅤ

ㅤ
Criando uma Matriz com 2 dimensões:
```
python

arr9 = np.array([ [1,2,3], [4,5,6] ])
print(arr9)
```
```
out: [[1 2 3]
     [4 5 6]]
```


ㅤ

Verificando a forma (shape) desse array criado:
```
python

print(arr9.shape)
```
```
out: (2, 3)
```
Ele nos retorna, que é, uma matriz, com 2 dimensões e 3 valores em cada dimensão!


ㅤ

ㅤ



Dessa forma, eu crio uma matriz, com 2 dimensões preenchida com o número 1:

```
python

arr10 = np.ones((2,3))
print(arr10)
```
```
out: [[1. 1. 1.]
     [1. 1. 1.]]
```

ㅤㅤ


Vamos criar uma listas de listas:
```
python

lista = [[10,20,30], [90,80,100], [1,2,3]]
```

Criando uma array numpy a partir de uma lista de listas:
```
python

arr11 = np.matrix(lista)
```

Verificando a forma (shape) desse array criado:
```
python

arr11.shape
```
```
out: (3, 3)
```
Nos retornando que ele tem 3 dimensões, com 3 elementos em cada



ㅤㅤ


ㅤㅤ
### Manipulando os elementos das matrizes

#### Fatiando uma matriz (SLICING)
> antes de tudo: **INDEXAÇÃO EM PYHTON COMEÇA POR ZERO!**

A indexação por matrizes é um pouco diferente, como vamos manipular uma matriz que tem 3 dimensões, precisamos especificar, qual a dimensão e depois qual elemento:


 *[dimensão, elemento]*
ㅤㅤ

ㅤㅤ

Vendo os valores da array a ser manipulada:
```
python

print(arr11)
```
```
out: [[ 10,  20,  30]
     [ 90,  80, 100]
     [  1,   2,   3]]
```


ㅤㅤ


Retornando o elemento de indice 1 da linha de indice 2:
```
python

arr11[2,1]
```
```
out: 2
```


ㅤㅤ

Vamos retornar das linhas de índice 0, até 1 (Porque o índice 2 é EXCLUSIVO), apenas os elementos de índice 2
```
python

arr11[0:2, 2]
```
```
out: matrix([[ 30],
            [100]])
```


ㅤㅤ

Retornando da linha de índice 1, qualquer valor (todos valores)
```
python

arr11[1, ]
```
```
out: matrix([[ 90,  80, 100]])
```


ㅤ

#### Manipulando os elementos

Alterando um elemento pelo índice:
```python

arr11[1,0] = 100 
```



ㅤ

Se não definirmos o tipo do dado, o numpy define ele, porém, pode acabar cometendo erros, é um bom ponto de atenção:
```
python

x = np.array([1,2]) # o Numpy decide o tipo do dado
y = np.array([1.0,2.0]) # o Numpy decide o tipo do dado
z = np.array([1,2], dtype = np.float64) # Aqui foi definido o tipo de dado em particular

print(x.dtype, y.dtype, z.dtype)
```
```
out: print(x.dtype, y.dtype, z.dtype)
```

ㅤ

Podemos definir o tipo de um array já na criação:
```
python

arr12 = np.array([[24, 76, 92, 14], [47, 36, 89, 2]], dtype = float)
print(arr12)
```
```
out: [[24. 76. 92. 14.]
     [47. 36. 89.  2.]]
```

ㅤ

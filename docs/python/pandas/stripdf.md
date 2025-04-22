
## Strip em DF do Pandas

>Diferente do Split, o Strip remove alguns caracteres da string

Retornando os 3 elementos da coluna 'Data_Pedido'
```python title='python'

df3['Data_Pedido'].head(3)
```
```python title='out:'

    0    2016-11-08
    1    2016-11-08
    2    2016-06-12
    Name: Data_Pedido, dtype: object
```
A coluna Data pedido tem o formato YYYY-MM-DD. Imagine que seja necessário deixar o ano apenas com 2 dígitos sem alterar o tipo da variável.

Podemos fazer isso com a função lstrit(), ou seja, left strip, (à esquerda).

<br><br>
***
Vamos remover os dígitos 2 e 0 à esquerda do valor da variável 'Data_Pedido'
```python title='python'

df3['Data_Pedido'].str.lstrip('20')
```
```python title='out:'

    0       16-11-08
    1       16-11-08
    2       16-06-12
    3       15-10-11
    4       15-10-11
              ...   
    9989    14-01-21
    9990    17-02-26
    9991    17-02-26
    9992    17-02-26
    9993    17-05-04
    Name: Data_Pedido, Length: 9994, dtype: object
```
Como não usamos o inplace=True, a mudança é feita apenas na memória, não afetando diretamente o DF. 

Podemos ainda usar as funções rstrip() (Á direita) ou strip().

<br>
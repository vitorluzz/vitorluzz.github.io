
## Manipulando Dados em DataFrames do Pandas

Criando um dicionário em python:
```
python

dados = {
    'Estado': ['Santa Catarina', 'Rio de Janeiro', 'Tocantins', 'Bahia', 'Minas Gerais'],
    'Ano': [2004, 2005, 2006, 2007, 2008],
    'Taxa Desemprego': [1.5, 1.7, 1.6, 2.4, 2.7]
}
```
<br>

Importando a classe DataFrame de dentro do pandas!
```
python

from pandas import DataFrame
```
<br>

Convertendo o dicionário python para um DataFrame do Pandas!
```
python

df = DataFrame(dados)
```
<br>

Fazendo a visualização dos dados, criando um cabeçalho e mostrando as primeiras 5 primeiras linhas
```
python

df.head()
```

out:
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Estado</th>
      <th>Ano</th>
      <th>Taxa Desemprego</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Santa Catarina</td>
      <td>2004</td>
      <td>1.5</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Rio de Janeiro</td>
      <td>2005</td>
      <td>1.7</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Tocantins</td>
      <td>2006</td>
      <td>1.6</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Bahia</td>
      <td>2007</td>
      <td>2.4</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Minas Gerais</td>
      <td>2008</td>
      <td>2.7</td>
    </tr>
  </tbody>
</table>
</div>
Isso é um formato tabular, uma tabela que podemos encontrar em um BD relacional.

<br>


Verificando o tipo do df
```
python

type(df)
```
```
out: pandas.core.frame.DataFrame
```
Ele nos diz que é um objeto Dataframe do pandas.
<br>

Reorganizando a ordem das colunas de forma fácil!
```
python

DataFrame(dados, columns = ['Estado', 'Taxa Desemprego', 'Ano'])
```
out:
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Estado</th>
      <th>Taxa Desemprego</th>
      <th>Ano</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Santa Catarina</td>
      <td>1.5</td>
      <td>2004</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Rio de Janeiro</td>
      <td>1.7</td>
      <td>2005</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Tocantins</td>
      <td>1.6</td>
      <td>2006</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Bahia</td>
      <td>2.4</td>
      <td>2007</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Minas Gerais</td>
      <td>2.7</td>
      <td>2008</td>
    </tr>
  </tbody>
</table>
</div>

<br>

Alterando o nome das palavras do índice!
```
python

df2 = DataFrame(dados,
               columns = ['Estado', 'Taxa Desemprego', 'Taxa Crescimento', 'Ano'],
               index = ['estado1', 'estado2', 'estado3', 'estado4', 'estado5'])
```

Mostando o DataFrame modificado
```
python

print(df2)
```
```
out:
                     Estado  Taxa Desemprego Taxa Crescimento   Ano
    estado1  Santa Catarina              1.5              NaN  2004
    estado2  Rio de Janeiro              1.7              NaN  2005
    estado3       Tocantins              1.6              NaN  2006
    estado4           Bahia              2.4              NaN  2007
    estado5    Minas Gerais              2.7              NaN  2008

```
 Como a taxa Crescimento não existia no meu dicionário, ele preenche com NaN.

<br>

Retornando os valores do DataFrame
```
python
 
df.values
```
```
out:

array([['Santa Catarina', 2004, 1.5],
           ['Rio de Janeiro', 2005, 1.7],
           ['Tocantins', 2006, 1.6],
           ['Bahia', 2007, 2.4],
           ['Minas Gerais', 2008, 2.7]], dtype=object)
```
<br>

Retornando o tipo de cada coluna
```
python

df2.dtypes
```
```
out:

    Estado               object
    Taxa Desemprego     float64
    Taxa Crescimento     object
    Ano                   int64
    dtype: object
```
Quando o pandas não reconhece o conteúdo, ele classifica o mesmo como String

<br>

Retornando as colunas do DF
```
python

df2.columns
```
```
out: Index(['Estado', 'Taxa Desemprego', 'Taxa Crescimento', 'Ano'], dtype='object')
```
<br>

Imprimindo apenas uma coluna do DataFrame
```
python

df2['Estado']
```
```
out:

    estado1    Santa Catarina
    estado2    Rio de Janeiro
    estado3         Tocantins
    estado4             Bahia
    estado5      Minas Gerais
    Name: Estado, dtype: object
```

<br>

Imprimindo duas colunas do DF
```
python


df2[['Taxa Desemprego', 'Ano']]
```
out:
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Taxa Desemprego</th>
      <th>Ano</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>estado1</th>
      <td>1.5</td>
      <td>2004</td>
    </tr>
    <tr>
      <th>estado2</th>
      <td>1.7</td>
      <td>2005</td>
    </tr>
    <tr>
      <th>estado3</th>
      <td>1.6</td>
      <td>2006</td>
    </tr>
    <tr>
      <th>estado4</th>
      <td>2.4</td>
      <td>2007</td>
    </tr>
    <tr>
      <th>estado5</th>
      <td>2.7</td>
      <td>2008</td>
    </tr>
  </tbody>
</table>
</div>
Quando eu estou imprimindo apenas 1 coluna, eu utilizo 1 colchete e o nome da coluna.

Já quando eu imprimir mais de 1 coluna, preciso passar uma lista de colunas para conseguir fazer essa operação.
<br>

Filtrando uma linha específica do meu DF
```
python

df2.filter(items = ['estado3'], axis = 0)
```
out:
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Estado</th>
      <th>Taxa Desemprego</th>
      <th>Taxa Crescimento</th>
      <th>Ano</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>estado3</th>
      <td>Tocantins</td>
      <td>1.6</td>
      <td>NaN</td>
      <td>2006</td>
    </tr>
  </tbody>
</table>
</div>

<br>

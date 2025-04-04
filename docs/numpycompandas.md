
## Usando NumPy e Pandas para Manipulação de Dados!

Imprimindo o DataFrame que será manipulado
```
python

df2.head()
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
      <th>estado1</th>
      <td>Santa Catarina</td>
      <td>1.5</td>
      <td>NaN</td>
      <td>2004</td>
    </tr>
    <tr>
      <th>estado2</th>
      <td>Rio de Janeiro</td>
      <td>1.7</td>
      <td>NaN</td>
      <td>2005</td>
    </tr>
    <tr>
      <th>estado3</th>
      <td>Tocantins</td>
      <td>1.6</td>
      <td>NaN</td>
      <td>2006</td>
    </tr>
    <tr>
      <th>estado4</th>
      <td>Bahia</td>
      <td>2.4</td>
      <td>NaN</td>
      <td>2007</td>
    </tr>
    <tr>
      <th>estado5</th>
      <td>Minas Gerais</td>
      <td>2.7</td>
      <td>NaN</td>
      <td>2008</td>
    </tr>
  </tbody>
</table>
</div>

<br>
***


Imprimindo um resumo estatístico do meu DF das colunas do tipo numérico!
```
python

df2.describe()
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
      <th>count</th>
      <td>5.000000</td>
      <td>5.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>1.980000</td>
      <td>2006.000000</td>
    </tr>
    <tr>
      <th>std</th>
      <td>0.535724</td>
      <td>1.581139</td>
    </tr>
    <tr>
      <th>min</th>
      <td>1.500000</td>
      <td>2004.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>1.600000</td>
      <td>2005.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>1.700000</td>
      <td>2006.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>2.400000</td>
      <td>2007.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>2.700000</td>
      <td>2008.000000</td>
    </tr>
  </tbody>
</table>
</div>

<br>
***


Retornando True para as colunas com valor ausente!
```
python

df2.isna()
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
      <th>estado1</th>
      <td>False</td>
      <td>False</td>
      <td>True</td>
      <td>False</td>
    </tr>
    <tr>
      <th>estado2</th>
      <td>False</td>
      <td>False</td>
      <td>True</td>
      <td>False</td>
    </tr>
    <tr>
      <th>estado3</th>
      <td>False</td>
      <td>False</td>
      <td>True</td>
      <td>False</td>
    </tr>
    <tr>
      <th>estado4</th>
      <td>False</td>
      <td>False</td>
      <td>True</td>
      <td>False</td>
    </tr>
    <tr>
      <th>estado5</th>
      <td>False</td>
      <td>False</td>
      <td>True</td>
      <td>False</td>
    </tr>
  </tbody>
</table>
</div>

<br>
***


Olhando uma coluna específica para verificar se há valores ausentes.
```
python

df2['Taxa Crescimento'].isna()
```
```
out:

    estado1    True
    estado2    True
    estado3    True
    estado4    True
    estado5    True
    Name: Taxa Crescimento, dtype: bool
```
<br>
***


Importando o NumPy para nos auxiliar na manipulação
```
python

import numpy as np
```
<br>
***


Usando o numpy para preencher uma das colunas do df!
```
python

df2['Taxa Crescimento'] = np.arange(5.)
df2
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
      <th>estado1</th>
      <td>Santa Catarina</td>
      <td>1.5</td>
      <td>0.0</td>
      <td>2004</td>
    </tr>
    <tr>
      <th>estado2</th>
      <td>Rio de Janeiro</td>
      <td>1.7</td>
      <td>1.0</td>
      <td>2005</td>
    </tr>
    <tr>
      <th>estado3</th>
      <td>Tocantins</td>
      <td>1.6</td>
      <td>2.0</td>
      <td>2006</td>
    </tr>
    <tr>
      <th>estado4</th>
      <td>Bahia</td>
      <td>2.4</td>
      <td>3.0</td>
      <td>2007</td>
    </tr>
    <tr>
      <th>estado5</th>
      <td>Minas Gerais</td>
      <td>2.7</td>
      <td>4.0</td>
      <td>2008</td>
    </tr>
  </tbody>
</table>
</div>

<br>
***


Agora, verificando se ainda há valores ausentes no DF
```
python

df2['Taxa Crescimento'].isna()
```
```
out:

    estado1    False
    estado2    False
    estado3    False
    estado4    False
    estado5    False
    Name: Taxa Crescimento, dtype: bool
```
<br>
***



## Fatiamento do DataFrame do Pandas (Slicing)

Retornando as linhas da coluna de índice = estado2 e estado4
```
python

df2['estado2':'estado4']
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
  </tbody>
</table>
</div>
Nesse caso, o estado4 não se classifica como exclusivo, então, o estado4 entra!
<br>
***

Retornando os valores das colunas onde a taxa desemprego for menor que 2
```
python

df2[ df2['Taxa Desemprego'] < 2 ]
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
  </tbody>
</table>
</div>
Quando queremos aplicar uma regra de fatiamento, precisamos abrir colchetes 2 vezes!

<br>
***

Retornando os valores de 2 ou mais colunas!
```
python

df2[ ['Estado', 'Taxa Crescimento'] ]
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
      <th>Taxa Crescimento</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>estado1</th>
      <td>Santa Catarina</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>estado2</th>
      <td>Rio de Janeiro</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>estado3</th>
      <td>Tocantins</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>estado4</th>
      <td>Bahia</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>estado5</th>
      <td>Minas Gerais</td>
      <td>4.0</td>
    </tr>
  </tbody>
</table>
</div>
Preciso abrir dois colchetes quando eu quiser aplicar uma rera de fatiamento!!

<br>

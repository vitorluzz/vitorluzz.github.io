
## Split de Strings em DFs

Filtrando uma coluna específica do DF
```
python

df3['ID_Pedido'].head()
```
```
out:

    0    CA-2016-152156
    1    CA-2016-152156
    2    CA-2016-138688
    3    US-2015-108966
    4    US-2015-108966
    Name: ID_Pedido, dtype: object
```
Essa coluna de Id, nos retorna: o País, o ano e o ID do pedido, vamos extrair esses dados e gravar em uma nova coluna!

<br>

Separando os dados dos ID com base no '-'
```
python

df3['ID_Pedido'].str.split('-')
```
```
out:

    0       [CA, 2016, 152156]
    1       [CA, 2016, 152156]
    2       [CA, 2016, 138688]
    3       [US, 2015, 108966]
    4       [US, 2015, 108966]
                   ...        
    9989    [CA, 2014, 110422]
    9990    [CA, 2017, 121258]
    9991    [CA, 2017, 121258]
    9992    [CA, 2017, 121258]
    9993    [CA, 2017, 119914]
    Name: ID_Pedido, Length: 9994, dtype: object
```
Ele está nos retornando uma lista em cada ID

<br>

>*O Split ele divide os valores e nos retorna eles em uma lista por cada ID separadamente*

<br>

Separando os dados, porém, retornando apenas o valor de índice 1, ou seja, o ano
```
python

df3['ID_Pedido'].str.split('-').str[1].head
```
```
out:

    <bound method NDFrame.head of 0       2016
    1       2016
    2       2016
    3       2015
    4       2015
            ... 
    9989    2014
    9990    2017
    9991    2017
    9992    2017
    9993    2017
    Name: ID_Pedido, Length: 9994, dtype: object>
```
<br>

Agora, estamos fazendo o split, separando os valores e armazenando em uma coluna específica
```
python

df3['Ano'] = df3['ID_Pedido'].str.split('-').str[1]
```

Visualizando as alterações!
```
python

df3.head()
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
      <th>ID_Pedido</th>
      <th>Data_Pedido</th>
      <th>ID_Cliente</th>
      <th>Segmento</th>
      <th>Pais</th>
      <th>Regiao</th>
      <th>ID_Produto</th>
      <th>Categoria</th>
      <th>Nome_Produto</th>
      <th>Valor_Venda</th>
      <th>Quantidade</th>
      <th>Ano</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>CA-2016-152156</td>
      <td>2016-11-08</td>
      <td>CG-12520</td>
      <td>Consumer</td>
      <td>United States</td>
      <td>South</td>
      <td>FUR-BO-10001798</td>
      <td>Furniture</td>
      <td>Bush Somerset Collection Bookcase</td>
      <td>261.9600</td>
      <td>3.0</td>
      <td>2016</td>
    </tr>
    <tr>
      <th>1</th>
      <td>CA-2016-152156</td>
      <td>2016-11-08</td>
      <td>CG-12520</td>
      <td>Consumer</td>
      <td>United States</td>
      <td>South</td>
      <td>FUR-CH-10000454</td>
      <td>Furniture</td>
      <td>Hon Deluxe Fabric Upholstered Stacking Chairs,...</td>
      <td>731.9400</td>
      <td>3.0</td>
      <td>2016</td>
    </tr>
    <tr>
      <th>2</th>
      <td>CA-2016-138688</td>
      <td>2016-06-12</td>
      <td>DV-13045</td>
      <td>Corporate</td>
      <td>United States</td>
      <td>West</td>
      <td>OFF-LA-10000240</td>
      <td>Office Supplies</td>
      <td>Self-Adhesive Address Labels for Typewriters b...</td>
      <td>14.6200</td>
      <td>2.0</td>
      <td>2016</td>
    </tr>
    <tr>
      <th>3</th>
      <td>US-2015-108966</td>
      <td>2015-10-11</td>
      <td>SO-20335</td>
      <td>Consumer</td>
      <td>United States</td>
      <td>South</td>
      <td>FUR-TA-10000577</td>
      <td>Furniture</td>
      <td>Bretford CR4500 Series Slim Rectangular Table</td>
      <td>957.5775</td>
      <td>5.0</td>
      <td>2015</td>
    </tr>
    <tr>
      <th>4</th>
      <td>US-2015-108966</td>
      <td>2015-10-11</td>
      <td>SO-20335</td>
      <td>Consumer</td>
      <td>United States</td>
      <td>South</td>
      <td>OFF-ST-10000760</td>
      <td>Office Supplies</td>
      <td>Eldon Fold 'N Roll Cart System</td>
      <td>22.3680</td>
      <td>2.0</td>
      <td>2015</td>
    </tr>
  </tbody>
</table>
</div>

<br>

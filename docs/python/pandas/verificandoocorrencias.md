

## Verificando a ocorrência de diversos valores em uma coluna

Verificando a forma (shape) do DF
```python title='python'

df3.shape
```
```python title='out:'
(9994, 11)
```
Ele nos retorna o número de linhas, número de colunas!

<br>
***

Aplicando um filtro que nos mostra se há a quantidade, 5,7,9 ou 11
```python title='python'

df3[ df3['Quantidade'].isin([5,7,9, 11])] 
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
    </tr>
  </thead>
  <tbody>
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
    </tr>
    <tr>
      <th>5</th>
      <td>CA-2014-115812</td>
      <td>2014-06-09</td>
      <td>BH-11710</td>
      <td>Consumer</td>
      <td>United States</td>
      <td>West</td>
      <td>FUR-FU-10001487</td>
      <td>Furniture</td>
      <td>Eldon Expressions Wood and Plastic Desk Access...</td>
      <td>48.8600</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>CA-2014-115812</td>
      <td>2014-06-09</td>
      <td>BH-11710</td>
      <td>Consumer</td>
      <td>United States</td>
      <td>West</td>
      <td>OFF-AP-10002892</td>
      <td>Office Supplies</td>
      <td>Belkin F5C206VTEL 6 Outlet Surge</td>
      <td>114.9000</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>10</th>
      <td>CA-2014-115812</td>
      <td>2014-06-09</td>
      <td>BH-11710</td>
      <td>Consumer</td>
      <td>United States</td>
      <td>West</td>
      <td>FUR-TA-10001539</td>
      <td>Furniture</td>
      <td>Chromcraft Rectangular Conference Tables</td>
      <td>1706.1840</td>
      <td>9.0</td>
    </tr>
    <tr>
      <th>14</th>
      <td>US-2015-118983</td>
      <td>2015-11-22</td>
      <td>HP-14815</td>
      <td>Home Office</td>
      <td>United States</td>
      <td>Central</td>
      <td>OFF-AP-10002311</td>
      <td>Office Supplies</td>
      <td>Holmes Replacement Filter for HEPA Air Cleaner...</td>
      <td>68.8100</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>9974</th>
      <td>US-2016-103674</td>
      <td>2016-12-06</td>
      <td>AP-10720</td>
      <td>Home Office</td>
      <td>United States</td>
      <td>West</td>
      <td>OFF-AR-10004752</td>
      <td>Office Supplies</td>
      <td>Blackstonian Pencils</td>
      <td>18.6900</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>9977</th>
      <td>US-2016-103674</td>
      <td>2016-12-06</td>
      <td>AP-10720</td>
      <td>Home Office</td>
      <td>United States</td>
      <td>West</td>
      <td>OFF-FA-10003467</td>
      <td>Office Supplies</td>
      <td>Alliance Big Bands Rubber Bands, 12/Pack</td>
      <td>13.8600</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>9981</th>
      <td>CA-2017-163566</td>
      <td>2017-08-03</td>
      <td>TB-21055</td>
      <td>Consumer</td>
      <td>United States</td>
      <td>East</td>
      <td>OFF-LA-10004484</td>
      <td>Office Supplies</td>
      <td>Avery 476</td>
      <td>16.5200</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>9982</th>
      <td>US-2016-157728</td>
      <td>2016-09-22</td>
      <td>RC-19960</td>
      <td>Consumer</td>
      <td>United States</td>
      <td>Central</td>
      <td>OFF-PA-10002195</td>
      <td>Office Supplies</td>
      <td>RSVP Cards &amp; Envelopes, Blank White, 8-1/2" X ...</td>
      <td>35.5600</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>9988</th>
      <td>CA-2017-163629</td>
      <td>2017-11-17</td>
      <td>RA-19885</td>
      <td>Corporate</td>
      <td>United States</td>
      <td>South</td>
      <td>TEC-PH-10004006</td>
      <td>Technology</td>
      <td>Panasonic KX - TS880B Telephone</td>
      <td>206.1000</td>
      <td>5.0</td>
    </tr>
  </tbody>
</table>
<p>2128 rows × 11 columns</p>
</div>

<br>
***

Aplicando o mesmo filtro, porém, quero ver apenas o formato do retorno, Quantas linhas e colunas
```python title='python'

df3[ df3['Quantidade'].isin([5,7,9, 11])].shape 
```
```python title='out:'
(2128, 11)
```
<br>
***

Aplicando o mesmo filtro, porém, visualizando apenas as 10 primeiras linhas!
```python title='python'

df3[ df3['Quantidade'].isin([5,7,9, 11])][:10]
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
    </tr>
  </thead>
  <tbody>
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
    </tr>
    <tr>
      <th>5</th>
      <td>CA-2014-115812</td>
      <td>2014-06-09</td>
      <td>BH-11710</td>
      <td>Consumer</td>
      <td>United States</td>
      <td>West</td>
      <td>FUR-FU-10001487</td>
      <td>Furniture</td>
      <td>Eldon Expressions Wood and Plastic Desk Access...</td>
      <td>48.8600</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>CA-2014-115812</td>
      <td>2014-06-09</td>
      <td>BH-11710</td>
      <td>Consumer</td>
      <td>United States</td>
      <td>West</td>
      <td>OFF-AP-10002892</td>
      <td>Office Supplies</td>
      <td>Belkin F5C206VTEL 6 Outlet Surge</td>
      <td>114.9000</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>10</th>
      <td>CA-2014-115812</td>
      <td>2014-06-09</td>
      <td>BH-11710</td>
      <td>Consumer</td>
      <td>United States</td>
      <td>West</td>
      <td>FUR-TA-10001539</td>
      <td>Furniture</td>
      <td>Chromcraft Rectangular Conference Tables</td>
      <td>1706.1840</td>
      <td>9.0</td>
    </tr>
    <tr>
      <th>14</th>
      <td>US-2015-118983</td>
      <td>2015-11-22</td>
      <td>HP-14815</td>
      <td>Home Office</td>
      <td>United States</td>
      <td>Central</td>
      <td>OFF-AP-10002311</td>
      <td>Office Supplies</td>
      <td>Holmes Replacement Filter for HEPA Air Cleaner...</td>
      <td>68.8100</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>21</th>
      <td>CA-2016-137330</td>
      <td>2016-12-09</td>
      <td>KB-16585</td>
      <td>Corporate</td>
      <td>United States</td>
      <td>Central</td>
      <td>OFF-AR-10000246</td>
      <td>Office Supplies</td>
      <td>Newell 318</td>
      <td>19.4600</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>22</th>
      <td>CA-2016-137330</td>
      <td>2016-12-09</td>
      <td>KB-16585</td>
      <td>Corporate</td>
      <td>United States</td>
      <td>Central</td>
      <td>OFF-AP-10001492</td>
      <td>Office Supplies</td>
      <td>Acco Six-Outlet Power Strip, 4' Cord Length</td>
      <td>60.3400</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>27</th>
      <td>US-2015-150630</td>
      <td>2015-09-17</td>
      <td>TB-21520</td>
      <td>Consumer</td>
      <td>United States</td>
      <td>East</td>
      <td>FUR-BO-10004834</td>
      <td>Furniture</td>
      <td>Riverside Palais Royal Lawyers Bookcase, Royal...</td>
      <td>3083.4300</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>35</th>
      <td>CA-2016-117590</td>
      <td>2016-12-08</td>
      <td>GH-14485</td>
      <td>Corporate</td>
      <td>United States</td>
      <td>Central</td>
      <td>TEC-PH-10004977</td>
      <td>Technology</td>
      <td>GE 30524EE4</td>
      <td>1097.5440</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>36</th>
      <td>CA-2016-117590</td>
      <td>2016-12-08</td>
      <td>GH-14485</td>
      <td>Corporate</td>
      <td>United States</td>
      <td>Central</td>
      <td>FUR-FU-10003664</td>
      <td>Furniture</td>
      <td>Electrix Architect's Clamp-On Swing Arm Lamp, ...</td>
      <td>190.9200</td>
      <td>5.0</td>
    </tr>
  </tbody>
</table>
</div>

<br>
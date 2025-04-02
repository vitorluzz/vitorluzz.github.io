

## Operadores Lógicos para manipulação de dados com Pandas

Filtrando as vendas que ocorreram no segmento Home Office E na região South
```
python

# Nesse caso, as duas condições precisam necessariamente ser verdadeiras para serem retornadas!
df3[ (df3.Segmento == 'Home Office') & (df3.Regiao == 'South') ].head()
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
      <th>182</th>
      <td>CA-2014-158274</td>
      <td>2014-11-19</td>
      <td>RM-19675</td>
      <td>Home Office</td>
      <td>United States</td>
      <td>South</td>
      <td>TEC-PH-10003273</td>
      <td>Technology</td>
      <td>AT&amp;T TR1909W</td>
      <td>503.9600</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>183</th>
      <td>CA-2014-158274</td>
      <td>2014-11-19</td>
      <td>RM-19675</td>
      <td>Home Office</td>
      <td>United States</td>
      <td>South</td>
      <td>TEC-PH-10004896</td>
      <td>Technology</td>
      <td>Nokia Lumia 521 (T-Mobile)</td>
      <td>149.9500</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>184</th>
      <td>CA-2014-158274</td>
      <td>2014-11-19</td>
      <td>RM-19675</td>
      <td>Home Office</td>
      <td>United States</td>
      <td>South</td>
      <td>TEC-AC-10002345</td>
      <td>Technology</td>
      <td>HP Standard 104 key PS/2 Keyboard</td>
      <td>29.0000</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>231</th>
      <td>US-2017-100930</td>
      <td>2017-04-07</td>
      <td>CS-12400</td>
      <td>Home Office</td>
      <td>United States</td>
      <td>South</td>
      <td>FUR-TA-10001705</td>
      <td>Furniture</td>
      <td>Bush Advantage Collection Round Conference Table</td>
      <td>233.8600</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>232</th>
      <td>US-2017-100930</td>
      <td>2017-04-07</td>
      <td>CS-12400</td>
      <td>Home Office</td>
      <td>United States</td>
      <td>South</td>
      <td>FUR-TA-10003473</td>
      <td>Furniture</td>
      <td>Bretford Rectangular Conference Table Tops</td>
      <td>620.6145</td>
      <td>3.0</td>
    </tr>
  </tbody>
</table>
</div>

<br>


Filtrando as vendas que ocorreram no segmento Home Office OU na região South

Mas agora eu estou vendo os últimos valores, estou vendo o 'Tail', a cauda do DF.
```
python

# Nesse caso, Apenas uma das condições precisa ser verdadeira para o valor ser retornado!
df3[ (df3.Segmento == 'Home Office') | (df3.Regiao == 'South') ].tail()
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
      <th>9979</th>
      <td>US-2016-103674</td>
      <td>2016-12-06</td>
      <td>AP-10720</td>
      <td>Home Office</td>
      <td>United States</td>
      <td>West</td>
      <td>OFF-BI-10002026</td>
      <td>Office Supplies</td>
      <td>Ibico Recycled Linen-Style Covers</td>
      <td>437.472</td>
      <td>14.0</td>
    </tr>
    <tr>
      <th>9980</th>
      <td>US-2015-151435</td>
      <td>2015-09-06</td>
      <td>SW-20455</td>
      <td>Consumer</td>
      <td>United States</td>
      <td>South</td>
      <td>FUR-TA-10001029</td>
      <td>Furniture</td>
      <td>KI Adjustable-Height Table</td>
      <td>85.980</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>9987</th>
      <td>CA-2017-163629</td>
      <td>2017-11-17</td>
      <td>RA-19885</td>
      <td>Corporate</td>
      <td>United States</td>
      <td>South</td>
      <td>TEC-AC-10001539</td>
      <td>Technology</td>
      <td>Logitech G430 Surround Sound Gaming Headset wi...</td>
      <td>79.990</td>
      <td>1.0</td>
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
      <td>206.100</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>9989</th>
      <td>CA-2014-110422</td>
      <td>2014-01-21</td>
      <td>TB-21400</td>
      <td>Consumer</td>
      <td>United States</td>
      <td>South</td>
      <td>FUR-FU-10001889</td>
      <td>Furniture</td>
      <td>Ultra Door Pull Handle</td>
      <td>25.248</td>
      <td>3.0</td>
    </tr>
  </tbody>
</table>
</div>

<br>

Filtrando as vendas que não ocorreram no segmento Home Office e não ocorreram na região South

Agora, estou vendo uma amostra de 5 valores, ou seja, 'Sample' de 5 valores de forma aleatória!!!
```
python

# Nesse caso, as duas condições precisam ser verdadeiras para o valor ser retornado!
df3[ (df3.Segmento != 'Home Office') & (df3.Regiao != 'South') ].sample(5)
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
      <th>5215</th>
      <td>CA-2016-145898</td>
      <td>2016-09-26</td>
      <td>CM-12445</td>
      <td>Consumer</td>
      <td>United States</td>
      <td>West</td>
      <td>OFF-PA-10001667</td>
      <td>Office Supplies</td>
      <td>Great White Multi-Use Recycled Paper (20Lb. an...</td>
      <td>29.900</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>3150</th>
      <td>CA-2015-147830</td>
      <td>2015-12-15</td>
      <td>NF-18385</td>
      <td>Consumer</td>
      <td>United States</td>
      <td>East</td>
      <td>TEC-AC-10002049</td>
      <td>Technology</td>
      <td>Plantronics Savi W720 Multi-Device Wireless He...</td>
      <td>2025.360</td>
      <td>6.0</td>
    </tr>
    <tr>
      <th>9352</th>
      <td>CA-2017-148411</td>
      <td>2017-09-24</td>
      <td>RO-19780</td>
      <td>Consumer</td>
      <td>United States</td>
      <td>Central</td>
      <td>FUR-CH-10003973</td>
      <td>Furniture</td>
      <td>GuestStacker Chair with Chrome Finish Legs</td>
      <td>520.464</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>1985</th>
      <td>CA-2014-164721</td>
      <td>2014-11-25</td>
      <td>LW-16825</td>
      <td>Corporate</td>
      <td>United States</td>
      <td>West</td>
      <td>OFF-PA-10000575</td>
      <td>Office Supplies</td>
      <td>Wirebound Message Books, Four 2 3/4 x 5 White ...</td>
      <td>26.760</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>3675</th>
      <td>CA-2017-154109</td>
      <td>2017-11-06</td>
      <td>ML-17410</td>
      <td>Consumer</td>
      <td>United States</td>
      <td>East</td>
      <td>OFF-PA-10000157</td>
      <td>Office Supplies</td>
      <td>Xerox 191</td>
      <td>47.952</td>
      <td>3.0</td>
    </tr>
  </tbody>
</table>
</div>

<br>

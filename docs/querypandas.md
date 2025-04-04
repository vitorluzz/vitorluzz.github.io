
## Query (Consulta) de Dados no DataFrame do Pandas

Com o pandas, podemos criar dataframes que são essencialmente tabelas. Como também podemos fazer consultas, ou simplesmente queries. Utilizando o método query():

Fazendo uma consulta a partir de uma coluna específica
```
python

df3.Valor_Venda.describe()
```
```
out:

    count     9994.000000
    mean       229.858001
    std        623.245101
    min          0.444000
    25%         17.280000
    50%         54.490000
    75%        209.940000
    max      22638.480000
    Name: Valor_Venda, dtype: float64
```
<br>
***

Criando um novo DF com o intervalo de vendas entre 229 e 10000
```
python

df2 = df3.query('229 < Valor_Venda < 10000')
```
***
Utilizando o describe no novo DF criado
```
python

df2.Valor_Venda.describe()
```
```
out:

    count    2357.000000
    mean      766.679142
    std       856.315136
    min       229.544000
    25%       323.100000
    50%       490.320000
    75%       859.200000
    max      9892.740000
    Name: Valor_Venda, dtype: float64
```
Podemos ver que a média de valores é 766
<br>
***

Criando um novo dataframe com os valores acima da média!
```
python

df4 = df3.query('Valor_Venda > 766')
```
***
Visualizando o DF criado
```
python

df4.head()
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
      <th>7</th>
      <td>CA-2014-115812</td>
      <td>2014-06-09</td>
      <td>BH-11710</td>
      <td>Consumer</td>
      <td>United States</td>
      <td>West</td>
      <td>TEC-PH-10002275</td>
      <td>Technology</td>
      <td>Mitel 5320 IP Phone VoIP phone</td>
      <td>907.1520</td>
      <td>6.0</td>
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
      <th>11</th>
      <td>CA-2014-115812</td>
      <td>2014-06-09</td>
      <td>BH-11710</td>
      <td>Consumer</td>
      <td>United States</td>
      <td>West</td>
      <td>TEC-PH-10002033</td>
      <td>Technology</td>
      <td>Konftel 250 Conference phone - Charcoal black</td>
      <td>911.4240</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>24</th>
      <td>CA-2015-106320</td>
      <td>2015-09-25</td>
      <td>EB-13870</td>
      <td>Consumer</td>
      <td>United States</td>
      <td>West</td>
      <td>FUR-TA-10000577</td>
      <td>Furniture</td>
      <td>Bretford CR4500 Series Slim Rectangular Table</td>
      <td>1044.6300</td>
      <td>3.0</td>
    </tr>
  </tbody>
</table>
</div>

<br>
***
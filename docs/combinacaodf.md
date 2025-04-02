
## Combinação de Strings

Passo a coluna que quero adicionar, passando como parametro o ID_Pedido, dizendo que quero que some com a coluna Segmento e separando por '-'

```
python

df3['Pedido Segmento'] = df3['ID_Pedido'].str.cat(df3['Segmento'], sep = '-')
```
Visualizando as alterações
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
      <th>Pedido Segmento</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>CA-2016-152156</td>
      <td>2016-11-08</td>
      <td>AX-12520</td>
      <td>Consumer</td>
      <td>United States</td>
      <td>South</td>
      <td>FUR-BO-10001798</td>
      <td>Furniture</td>
      <td>Bush Somerset Collection Bookcase</td>
      <td>261.9600</td>
      <td>3.0</td>
      <td>2016</td>
      <td>CA-2016-152156-Consumer</td>
    </tr>
    <tr>
      <th>1</th>
      <td>CA-2016-152156</td>
      <td>2016-11-08</td>
      <td>AX-12520</td>
      <td>Consumer</td>
      <td>United States</td>
      <td>South</td>
      <td>FUR-CH-10000454</td>
      <td>Furniture</td>
      <td>Hon Deluxe Fabric Upholstered Stacking Chairs,...</td>
      <td>731.9400</td>
      <td>3.0</td>
      <td>2016</td>
      <td>CA-2016-152156-Consumer</td>
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
      <td>CA-2016-138688-Corporate</td>
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
      <td>US-2015-108966-Consumer</td>
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
      <td>US-2015-108966-Consumer</td>
    </tr>
  </tbody>
</table>
</div>

<br>
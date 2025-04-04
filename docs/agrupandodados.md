
## Agrupamento de dados em DF com Group By

Primeiro: Filtramos os dados extraindo 3 colunas: Segmento, Região e Valor Venda.

Em seguida: Agrupamos por duas colunas: Segmento e Região.

Então: Calculamos a média da coluna que ficou de fora do groupby
```
python

df3[ ['Segmento', 'Regiao', 'Valor_Venda'] ].groupby(['Segmento', 'Regiao']).mean()
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
      <th></th>
      <th>Valor_Venda</th>
    </tr>
    <tr>
      <th>Segmento</th>
      <th>Regiao</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th rowspan="4" valign="top">Consumer</th>
      <th>Central</th>
      <td>207.946728</td>
    </tr>
    <tr>
      <th>East</th>
      <td>238.875539</td>
    </tr>
    <tr>
      <th>South</th>
      <td>233.390180</td>
    </tr>
    <tr>
      <th>West</th>
      <td>217.033955</td>
    </tr>
    <tr>
      <th rowspan="4" valign="top">Corporate</th>
      <th>Central</th>
      <td>234.763466</td>
    </tr>
    <tr>
      <th>East</th>
      <td>228.516929</td>
    </tr>
    <tr>
      <th>South</th>
      <td>238.992025</td>
    </tr>
    <tr>
      <th>West</th>
      <td>235.265911</td>
    </tr>
    <tr>
      <th rowspan="4" valign="top">Home Office</th>
      <th>Central</th>
      <td>208.248046</td>
    </tr>
    <tr>
      <th>East</th>
      <td>253.911805</td>
    </tr>
    <tr>
      <th>South</th>
      <td>272.996329</td>
    </tr>
    <tr>
      <th>West</th>
      <td>239.442692</td>
    </tr>
  </tbody>
</table>
</div>

>Ele nos retorna: Esse segmento, nas regiões, tem essa média POR REGIÃO!

<br>
***

### Agregação Múltipla com Group By

Retornando: A média, o Desvio Padrão e a Contagem das linhas!
```
python

df3[ ['Segmento', 'Regiao', 'Valor_Venda'] ].groupby(['Segmento', 'Regiao']).agg(
    Média=('Valor_Venda', 'mean'),
    Desvio_Padrão=('Valor_Venda', 'std'),
    Contagem=('Valor_Venda', 'count'))
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
      <th></th>
      <th>Média</th>
      <th>Desvio_Padrão</th>
      <th>Contagem</th>
    </tr>
    <tr>
      <th>Segmento</th>
      <th>Regiao</th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th rowspan="4" valign="top">Consumer</th>
      <th>Central</th>
      <td>207.946728</td>
      <td>587.906523</td>
      <td>1212</td>
    </tr>
    <tr>
      <th>East</th>
      <td>238.875539</td>
      <td>633.371169</td>
      <td>1469</td>
    </tr>
    <tr>
      <th>South</th>
      <td>233.390180</td>
      <td>559.346824</td>
      <td>838</td>
    </tr>
    <tr>
      <th>West</th>
      <td>217.033955</td>
      <td>551.997547</td>
      <td>1672</td>
    </tr>
    <tr>
      <th rowspan="4" valign="top">Corporate</th>
      <th>Central</th>
      <td>234.763466</td>
      <td>818.947521</td>
      <td>673</td>
    </tr>
    <tr>
      <th>East</th>
      <td>228.516929</td>
      <td>530.001654</td>
      <td>877</td>
    </tr>
    <tr>
      <th>South</th>
      <td>238.992025</td>
      <td>586.176947</td>
      <td>510</td>
    </tr>
    <tr>
      <th>West</th>
      <td>235.265911</td>
      <td>471.288764</td>
      <td>960</td>
    </tr>
    <tr>
      <th rowspan="4" valign="top">Home Office</th>
      <th>Central</th>
      <td>208.248046</td>
      <td>371.009180</td>
      <td>438</td>
    </tr>
    <tr>
      <th>East</th>
      <td>253.911805</td>
      <td>722.777318</td>
      <td>502</td>
    </tr>
    <tr>
      <th>South</th>
      <td>272.996329</td>
      <td>1404.798466</td>
      <td>272</td>
    </tr>
    <tr>
      <th>West</th>
      <td>239.442692</td>
      <td>529.242737</td>
      <td>571</td>
    </tr>
  </tbody>
</table>
</div>

<br>
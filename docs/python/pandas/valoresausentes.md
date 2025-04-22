
## Preenchendo valores ausentes em DataFrames do Pandas

Importando um DataFrame para manipulação
```python title='python'

df3 = pd.read_csv('dataset.csv')
```
<br>
***

Exibindo os valores, mostrando o cabeçalho, filtrando mostrando os 5 primeiros valores
```python title='python'

df3.head(5)
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
      <td>NaN</td>
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
      <td>NaN</td>
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
    </tr>
  </tbody>
</table>
</div>

<br>
***

Verificando se há valores ausentes e em qual coluna:
```python title='python'

df3.isna().sum()
```
```python title='out:'

    ID_Pedido       0
    Data_Pedido     0
    ID_Cliente      0
    Segmento        0
    Pais            0
    Regiao          0
    ID_Produto      0
    Categoria       0
    Nome_Produto    0
    Valor_Venda     0
    Quantidade      2
    dtype: int64
```
Se não houver valores ausentes, ele retornará zero, porém, se houver, ele retornará a quantidade de valores que estão faltando.


<br>
***

>  **MODA**
>
>__A moda é uma medida de tendência central que representa o valor mais frequente em um conjunto de dados!!__
>       
>Ela é extremamente útil quando queremos saber qual é o valor mais comum ou popular em um conjunto de dados!

Extraindo a moda da coluna quantidade
```python title='python'

moda = df3['Quantidade'].value_counts().index[0]
print(moda)
```
```python title='out:'
3.0 
```
<br>
***

Preenchendo os valores vazios com o valor da moda
```python title='python'

df3['Quantidade'].fillna(value = moda, inplace = True)

# O inplace é como se fosse para salvar as alterações!
# Se eu não utilizar o mesmo, ele irá criar uma cópia do DF e fazer a alteração apenas naquele escopo.
```


```python title='python'

# Verificando se ainda há valores vazios!
df3.isna().sum()
```
```python title='out:'


    ID_Pedido       0
    Data_Pedido     0
    ID_Cliente      0
    Segmento        0
    Pais            0
    Regiao          0
    ID_Produto      0
    Categoria       0
    Nome_Produto    0
    Valor_Venda     0
    Quantidade      0
    dtype: int64
```

>O nome dessa prática se chama **INTERPOLAÇÃO**! Quando utilizamos uma estatística da coluna para preencher valores ausentes!
<br>
***

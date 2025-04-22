
## Utilizando Python para trabalhar com linguagem SQL


```python title='python'

# Importando  os pacotes necessários
import sqlite3
print("A versão do sqlite é: " + sqlite3.sqlite_version)

import pandas as pd
print("A versão do pandas é: " + pd.__version__)
```
```python title='out:'

A versão do pandas é: 1.5.3
A versão do sqlite é: 3.39.3
```
<br>
***

### Conectando no Banco de Dados com Linguagem Python

Conectando no Banco de Dados
```python title='python'

# Conecta no banco de dados:
con = sqlite3.connect('cap12_dsa.db')
```
<br>
***


Abrindo um cursor que irá percorrer os dados e as linhas no banco de dados
```python title='python'

cursor = con.cursor()
```
<br>
***

APENAS criando a query de consulta
```python title='python'

# Query (consulta) SQL para extrair os nomes das colunas no banco de dados
# APENAS cria a query.
sql_query  = """SELECT name FROM sqlite_master WHERE type = 'table';"""
```
<br>
***

Executado a query de consulta
```python title='python'

# Executa a query SQL
cursor.execute(sql_query)
```

```python title='out:'
<sqlite3.Cursor at 0x7f467af08b90>
```

Ele nos retorna o objeto do cursor!

<br>
***

Agora, vamos visualizar o que resultado da consulta, verificando o que o cursor encontrou dentro do BD
```python title='python'

# Visualiza o resultado da consulta
print(cursor.fetchall())
```
```python title='out:'
[('tb_vendas_dsa',)]
```

<br>
***

Criando uma instrução SQL
```python title='python'

# Cria uma instrução SQL
query1 = 'SELECT * FROM tb_vendas_dsa'
```

Executando a query no BD
```python title='python'

# Executa a query no banco de dados
cursor.execute(query1)
```


```python title='out:'
<sqlite3.Cursor at 0x7f467af08b90>
```

<br>
***

Criando um List Comprehension afim de visualizarmos os nomes das colunas
```python title='python'

# List Comprehension para visualizar os nomes das colunas
nomes_colunas = [description[0] for description in cursor.description]
```

<br>
***

Visualizando o nome das colunas
```python title='python'

# Visualizando os nomes das colunas
print(nomes_colunas)

# Os nomes das colunas são METADADOS, pois é um dado sobre o dado, 
# E então dentro da tabela estão os dados
```
```python title='out:'
['ID_Pedido', 'ID_Cliente', 'Nome_Produto', 'Valor_Unitario', 'Unidades_Vendidas', 'Custo']
```

Recebendo os dados da execução da query e armazenando em uma variável
```python title='python'

# Retorna os dados da execução da query
dados = cursor.fetchall()
```

Visualizando os dados da variável:
```python title='python'

dados
```

```python title='out:'

    [(1, 63, 'Produto_38', 154.03, 7, 92.42),
     (2, 49, 'Produto_8', 171.52, 5, 102.91),
     (3, 83, 'Produto_39', 28.97, 13, 17.38),
     (4, 37, 'Produto_2', 104.55, 4, 62.73),
     (5, 19, 'Produto_1', 77.21, 19, 46.33),
     (6, 87, 'Produto_36', 161.97, 13, 97.18),
     (7, 59, 'Produto_24', 101.17, 7, 60.7),
     (8, 48, 'Produto_31', 92.03, 9, 55.22),
     (9, 73, 'Produto_4', 116.57, 6, 69.94),
     (10, 98, 'Produto_45', 46.16, 4, 27.7),
     (11, 86, 'Produto_30', 135.55, 12, 81.33),
     (12, 89, 'Produto_45', 119.4, 11, 71.64),
     (13, 96, 'Produto_11', 96.63, 13, 57.98),
     (14, 29, 'Produto_50', 191.3, 10, 114.78),
     (15, 63, 'Produto_21', 191.28, 14, 114.77),
     (16, 30, 'Produto_22', 67.58, 17, 40.55),
     (17, 5, 'Produto_41', 33.22, 2, 19.93),
     (18, 97, 'Produto_33', 67.77, 12, 40.66),
     (19, 19, 'Produto_18', 160.68, 15, 96.41),
     (20, 7, 'Produto_17', 34.37, 13, 20.62),
     
     [...]

     (490, 70, 'Produto_26', 124.03, 7, 74.42),
     (491, 97, 'Produto_39', 150.94, 17, 90.56),
     (492, 82, 'Produto_18', 178.03, 18, 106.82),
     (493, 45, 'Produto_37', 157.59, 9, 94.55),
     (494, 65, 'Produto_17', 73.05, 14, 43.83),
     (495, 53, 'Produto_26', 97.69, 9, 58.61),
     (496, 27, 'Produto_12', 155.02, 1, 93.01),
     (497, 32, 'Produto_23', 71.04, 6, 42.62),
     (498, 80, 'Produto_1', 67.83, 13, 40.7),
     (499, 13, 'Produto_50', 187.89, 16, 112.73),
     (500, 46, 'Produto_21', 82.81, 11, 49.69)]
```
<br>
***


### Aplicando Linguagem SQL direto no Banco de Dados com linguagem Python

>A query abaixo retorna a média de unidades vendidas por produto:

Criando uma instrução SQL
```python title='python'

# Cria uma instrução para calcular a média de unidades vendidas por produto
query3 = 'SELECT Nome_Produto as "Nome do Produto", AVG(Unidades_Vendidas) as "Média das Unidades" FROM tb_vendas_dsa GROUP BY Nome_Produto'
```
<br>
***

Executando a instrução no BD
```python title='python'

# Executa a query no banco de dados
cursor.execute(query3)
```


```python title='out:'
<sqlite3.Cursor at 0x7f467af08b90>
```


<br>
***

Visualizando o resultado da query
```python title='python'

# Visualizando os dados
cursor.fetchall()
```
```python title='out:'
    [('Produto_1', 12.0),
     ('Produto_10', 9.5),
     ('Produto_11', 14.181818181818182),
     ('Produto_12', 8.846153846153847),
     ('Produto_13', 6.0),
     ('Produto_14', 9.166666666666666),
     ('Produto_15', 9.75),
     ('Produto_16', 8.25),
     ('Produto_17', 11.714285714285714),
     ('Produto_18', 13.083333333333334),
     ('Produto_19', 9.727272727272727),
     ('Produto_2', 9.25),
     ('Produto_20', 7.555555555555555),
     ('Produto_21', 10.285714285714286),
     ('Produto_22', 13.6875),
     ('Produto_23', 10.818181818181818),
     ('Produto_24', 12.272727272727273),
     ('Produto_25', 9.538461538461538),
     ('Produto_26', 9.363636363636363),
     ('Produto_27', 11.1),
     ('Produto_28', 9.0),
     ('Produto_29', 9.692307692307692),
     ('Produto_3', 8.909090909090908),
     ('Produto_30', 9.875),
     ('Produto_31', 7.9),
     ('Produto_32', 11.923076923076923),
     ('Produto_33', 12.285714285714286),
     ('Produto_34', 8.1),
     ('Produto_35', 9.0),
     ('Produto_36', 9.090909090909092),
     ('Produto_37', 11.0),
     ('Produto_38', 12.8),
     ('Produto_39', 12.666666666666666),
     ('Produto_4', 11.153846153846153),
     ('Produto_40', 7.25),
     ('Produto_41', 11.857142857142858),
     ('Produto_42', 10.272727272727273),
     ('Produto_43', 11.0),
     ('Produto_44', 7.2),
     ('Produto_45', 8.875),
     ('Produto_46', 12.142857142857142),
     ('Produto_47', 10.571428571428571),
     ('Produto_48', 14.0),
     ('Produto_49', 11.875),
     ('Produto_5', 10.2),
     ('Produto_50', 10.545454545454545),
     ('Produto_6', 12.0),
     ('Produto_7', 13.5625),
     ('Produto_8', 11.071428571428571),
     ('Produto_9', 7.2)]
```
<br>

<br>

***


>A query abaixo retorna a média de unidades vendidas por produto **se** o valor unitárip for maior que 199:

Criando a instrução SQL
```python title='python'

# Cria uma instrução para calcular a média de unidades vendidas por produto,
# quando o valor unitário for maior que 199

query4 = """
            SELECT Nome_Produto, AVG(Unidades_Vendidas)
            FROM tb_vendas_dsa
            WHERE Valor_Unitario > 199
            GROUP BY Nome_Produto
        """
```

Execuntando a instrução
```python title='python'

# Executando a query no banco de dados
cursor.execute(query4)
```

```python title='out:'
<sqlite3.Cursor at 0x7f467af08b90>
```

<br>
***

Recebendo resultado do cursor
```python title='python'

cursor.fetchall()
```

```python title='out:'
    [('Produto_11', 1.0),
     ('Produto_15', 8.0),
     ('Produto_17', 14.0),
     ('Produto_20', 7.0),
     ('Produto_39', 16.0)]
```
<br>

<br>

***


A query abaixo retorna a média de unidades vendidas por produto se o valor unitário for maior que 199 e somente se a média de unidades vendidas for maior que 10:

FORMA ERRADA
```python title='python'

# Cria uma instrução para calcular a média de unidades vendidas por produto,
# quando o valor unitário for maior que 199

query5 = """
            SELECT Nome_Produto, AVG(Unidades_Vendidas)
            FROM tb_vendas_dsa
            WHERE Valor_Unitario > 199 and AVG(Unidades_Vendidas) > 10
            GROUP BY Nome_Produto
        """
```

>**Essa instrução dará erro!!!**
>
>*ERROR*: misuse or agregate: AVG()
>
> *ERRO*: USO INDEVIDO DA AGREGAÇÃO AVG()

<br>

<br>

***

A instrução SQL exige uma ordem de execução das cláusulas:

**PRIMEIRO**, será executado o *FROM*, para buscar os dados da tabela,

**EM SEGUIDA**, irá ser aplicado o *WHERE*, para buscar as colunas fazendo o agrupamento,

<br>
***

Então, em qual momento ele irá aplicar o AVG? 

**SOMENTE DEPOIS do GROUP BY!!!**

Na linha "AVG(Unidades_Vendidas) > 10" estamos tendando usar a média antes do group by,

ele ainda não fez o agrupamento, então não podemos usar!

<br>
***

FORMA CORRETA:
```python title='python'

# Cria uma instrução para calcular a média de unidades vendidas por produto,
# quando o valor unitário for maior que 199

query5 = """
            SELECT Nome_Produto, AVG(Unidades_Vendidas)
            FROM tb_vendas_dsa
            WHERE Valor_Unitario > 199 
            GROUP BY Nome_Produto
            HAVING AVG(Unidades_Vendidas) > 10
        """
```

**FORMA CORRETA**

A utilização da cláusula **HAVING** é usada para usar o filtro **DEPOIS do GROUP BY**

<br>

<br>

***


Executando a query
```python title='python'

cursor.execute(query5)
```


```python title='out:'
<sqlite3.Cursor at 0x7f467af08b90>
``` 

<br>
***

Visualizando os dados do cursor
```python title='python'

cursor.fetchall()
```

```python title='out:'
[('Produto_17', 14.0), ('Produto_39', 16.0)]
```

<br>
***

Fechando o cursor e encerrando a conexão com o banco de dados
```python title='python'

# Fecha o cursor e encerra a conexão
cursor.close()
con.close()
```


>**IMPORTANTE!!!**
>
>Sempre lembrar de encerrar a conexão depois de terminar a utilização do banco de dados!
>
>Deixar de fechar o cursor e a conexão com o DB pode ocasionar diversos problemas, como:
>
>- Ocasionar falhas de segurança,
>- Consumir Recursos de forma desnecessária,
>- Travar a conexão com o banco de dados.

<br>

<br>

***
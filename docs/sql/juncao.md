
---

###  **JOIN (Junção de Tabelas)**

O `JOIN` é utilizado para **combinar dados de duas ou mais tabelas** com base em uma coluna em comum entre elas. Com isso, conseguimos fazer buscas mais completas e detalhadas, reunindo informações que estão distribuídas em diferentes tabelas.

**EXEMPLO:**  
Imagine que temos uma tabela de **vendas**, onde cada registro possui apenas o **código do produto** vendido. Já os **detalhes dos produtos**, como o nome, categoria ou preço, estão armazenados em outra tabela chamada `Produtos`.

Se fizermos uma consulta apenas na tabela de vendas, não teremos acesso ao **nome do produto**, o que pode dificultar a leitura e interpretação dos dados por parte da audiência.

Usando o `JOIN`, podemos **unir essas tabelas** e exibir informações completas, como o nome do produto junto com os dados de venda, facilitando a identificação e tornando os relatórios mais informativos.
 

```SQL title='SQL'
SELECT Nome_Produto AS "Nome do Produto", 
    MIN(Valor_Venda) AS "Valor Mínimo", 
    MAX(Valor_Venda) AS "Valor Máximo", 
    AVG(Valor_Venda) AS "Média", 
    SUM(Valor_Venda) AS "Total", 
    COUNT(Valor_Venda)  AS "Contagem",
    Ano
FROM Vendas
JOIN Produtos
ON Vendas.Produto = Produtos.ID_Produto
GROUP BY Produto;
```

>Neste exemplo, estamos utilizando um `JOIN` para combinar os dados das tabelas **Vendas** e **Produtos**. A coluna `Nome_Produto` pertence à tabela **Produtos**, e por isso só conseguimos acessá-la após realizar a junção.
>
>A junção acontece por meio da cláusula `ON`, onde especificamos a relação entre as tabelas: a coluna `Produto` da tabela **Vendas** é uma **chave estrangeira** que faz referência à coluna `ID_Produto` da tabela **Produtos**. Isso permite que os dados correspondentes de cada produto nas duas tabelas sejam associados corretamente.


**OBSERVAÇÃO: TODO `JOIN` TEM `ON`!**

---

**TIPOS DE JOIN**

Existem diferentes tipos de junção, e cada uma afeta o resultado final da consulta de maneira distinta:

---

#### **INNER JOIN**

Retorna **apenas os registros que possuem correspondência nas duas tabelas.**
É o tipo de junção mais comum.

```SQL title='SQL'
SELECT *
FROM Vendas
INNER JOIN Produtos 
ON Vendas.Produto = Produtos.ID_Produto;
```
>Apenas os produtos que estão tanto na tabela de Vendas quanto na tabela Produtos serão exibidos.

---

#### **LEFT JOIN**

Retorna **todos os registros da tabela da esquerda** (a que vem antes do `JOIN`) e os correspondentes da tabela da direita.
Se não houver correspondência, os campos da tabela da direita virão como `NULL`.

```SQL title='SQL'
SELECT *
FROM Vendas
LEFT JOIN Produtos 
ON Vendas.Produto = Produtos.ID_Produto;
```
>Exibe todas as vendas, mesmo que o produto não exista mais na tabela Produtos.

---

#### **RIGHT JOIN**

Retorna **todos os registros da tabela da direita** (a que vem depois do `JOIN`) e os correspondentes da tabela da esquerda.
Se não houver correspondência, os campos da tabela da esquerda virão como `NULL`.

```SQL title='SQL'
SELECT *
FROM Vendas
RIGHT JOIN Produtos
ON Vendas.Produto = Produtos.ID_Produto;
```

>Exibe todos os produtos, mesmo os que não foram vendidos (ou seja, não aparecem na tabela Vendas).

---
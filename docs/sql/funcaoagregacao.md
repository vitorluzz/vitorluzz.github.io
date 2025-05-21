

### **Funções de Agregação**

As **funções de agregação** são utilizadas para realizar cálculos em um conjunto de valores de uma coluna, retornando um único resultado. Elas são muito úteis em análises de dados, principalmente quando queremos entender totais, médias, contagens, entre outros.

#### **AVG (Média)**

O AVG é utilizado para termos a média de uma coluna específicada:

```SQL title='SQL'
SELECT AVG(Valor)
FROM Produtos;
```

> Ou seja, estamos pegando os valores da coluna valor e fazendo a média da mesma

Como sabemos, fazer a média pode trazer muitos valores, podemos limpar e exibir apenas 2 casas decimais:

```SQL title='SQL'
SELECT TRUNCATE(AVG(Valor), 2)
FROM Produtos;
```
> Dessa forma, damos limpamos (Truncate) a média deixando apenas com 2 casas decimais.

---

#### **SUM (SOMA)**

A função SUM retorna a soma de todos os valores de uma coluna numérica:

```SQL title='SQL'
SELECT SUM(Quantidade)
FROM Vendas;
```
> Aqui, estamos somando todas as quantidades da tabela Vendas, obtendo o total de itens vendidos.

---
#### **COUNT (Contagem)**

A função COUNT é usada para contar o número de registros. Podemos usá-la para contar todas as linhas ou apenas valores não nulos de uma coluna:

```SQL title='SQL'
SELECT COUNT(*)
FROM Clientes;
```
> Esse exemplo conta todas as linhas da tabela Clientes, dessa forma, podemos saber quantos clientes cadastrados temos em nossa tabela.

```SQL title='SQL'
SELECT COUNT(Email)
FROM Clientes;
```

>Já esse conta apenas os registros onde a coluna Email não está nula.

---

#### **MAX (Máximo)**

A função MAX retorna o maior valor de uma determinada coluna:

```SQL title='SQL'
SELECT MAX(Preco)
FROM Produtos;
```

> Aqui, estamos buscando o maior valor da coluna Preco na tabela Produtos.

---

#### **MIN (Mínimo)**

A função MIN retorna o menor valor de uma determinada coluna:

```SQL title='SQL'
SELECT MIN(Preco)
FROM Produtos;
```

>Neste caso, estamos retornando o menor valor encontrado na coluna Preco.

---
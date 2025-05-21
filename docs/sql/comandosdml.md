
## **Comandos DML**

### **SELECT**

O select é usado para selecionar as linhas na qual serão visualizadas, exemplos da utilização:

```SQL title='SQL'
SELECT *
FROM Tabela;
```

> A sintaxe é essa, primeiro selecionar (SELECT), o * é para selecionar TODAS COLUNAS e depois especificamos a tabela na qual será feito a Query.

---

### **LIMIT**

O Limit serve para limitar as linhas a serem visualizadas no resultado da query, isso é muito útil, especialmente nos casos onde temos uma base de dados de **MUITAS** linhas, se por acaso fizermos o select em todo dataset, pode acabar travando o banco de dados. A melhor alternativa e limitar o select:

```SQL title='SQL'
SELECT *
FROM Tabela
LIMIT 10;
```

> O limit é declarado depois de declararmos a tabela a ser manipulada, nesse comando em específico, estamos limitando a resposta em até 10 registros.

---

### **DISTINCT**

Supomos que queremos saber quantos registros diferentes temos em uma coluna em específico. Vamos supor por exemplo, que queremos saber a quantidade de segmentos temos em nossa tabela:

```SQL title='SQL' 
SELECT DISTINCT Segmento
FROM Tabela;
```

> E então, ele irá nos retornar apenas os valores distintos.

---

### **WHERE**

O Where serve para filtrarmos o nosso select, por exemplo, queremos pesquisar em uma coluna de ano apenas em um ano específico, isso faria assim:

```SQL title='SQL'
SELECT *
FROM Tabela
WHERE Ano = 2014;
```
> Nesse exemplo, estamos levando em conta que temos uma coluna apenas com os anos e que essa coluna contenha APENAS números inteiros.

---

### Operadores de Comparação (=, >, <, >=, etc.)

Temos alguns operadores que nos auxiliam nos filtros:

Podemos usar o sinal de igualdade '=' para pegar os valores que sejam exatamente igual:

```SQL title='SQL'
SELECT *
FROM Tabela
WHERE Quantidade = 5;
```

Ou então, podemos ter um apenas os valores maior ou igual um determinado valor:

```SQL title='SQL'
SELECT *
FROM Tabela
WHERE Quantidade >= 5;
```

Ou então sendo menor ou igual a um determinado valor:
```SQL title='SQL'
SELECT *
FROM Tabela
WHERE Quantidade <= 5;
```

---

### Operadores Lógicos  (AND, OR, NOT)

Os operadores lógicos são aqueles que nos permitem **combinar múlticas condições** em uma cláusula `WHERE`, tornando os filtros mais precisos e poderosos. Eles são usados para refinar os critérios de busca ao trabalhar com consultas SQL.

Entre os principais operadores lógicos, temos:

- `AND`: retorna resultados que atendem **todas as condições**.
- `OR`: retorna resultados que atendem **pelo menos uma das condições**.
- `NOT`: **nega** uma condição, retornando os registros que **não** atendem ao critério especificado.

Alguns exemplos da utilização desses operadores:

```SQL title='SQL'
SELECT *
FROM Tabela
WHERE Quantidade <= 2 AND Valor > 100;
```
> Combinamos duas operações de comparação utilizando o operador logico AND (E), ou seja, ele apenas retornará os registros que passem como verdadeiro nas duas comparações.



```SQL title='SQL'
SELECT *
FROM Tabela
WHERE Quantidade >= 5 OR Valor <= 500;
```
> Agora, com o operador OR (OU) ele irá retornar os valores que derem verdadeiro em uma ou outra comparações, não necessariamente dependendo das duas comparações sendo verdadeiras apenas uma delas.
---

### **BETWEEN**

O operador Between (Entre) serve para procurar registros onde se tem dados entre um valor e outro, por exemplo

```SQL title='SQL'
SELECT *
FROM Tabela
WHERE Valor BETWEEN 50 AND 100;
```

> Aqui estamos fazendo um filtro nos registros que tenha os valores entre 50 e 100, todos registros que foram verdadeiros para essa cláusula, eles serão exibidos nas respostas.

---

### **LIKE**

O Like é usado para fazermos os filtros por linha considerando as variáveis do tipo texto, por exemplo:

```SQL title='SQL'
SELECT *
FROM Tabela
WHERE Nome LIKE '%Bacon%';
```

> O like tem uma **sintaxe intessante**, após a declaração do mesmo, precisamos colocar entre aspas e **usar o símbolo de porcentagem**. A palavra Bacon está com % no início e no final, isso quer dizer que, **não importa o quem vem antes ou depois**, se em algum momento da variável Nome aparecer 'Bacon', retorne o valor.

Agora essa outra cláusula:

```SQL title='SQL'
SELECT *
FROM Tabela
WHERE Nome LIKE '%Flor';
```

> Agora nesse caso em específico, usando o `%` apenas no início, eu estou dizendo que **não importa o que vem antes**, mas o valor **precisa terminar com "Flor"**. Ou seja, ele vai retornar todos os registros cujo valor na coluna `Nome` termine com "Flor", como por exemplo "Rosa Flor", "Linda Flor", etc.

E por fim, temos também o caso:

```SQL title='SQL'
SELECT *
FROM Tabela
WHERE Nome LIKE 'Ana%';
```

>Neste exemplo, o % está **apenas no final da palavra**. Isso significa que **o valor deve começar com "Ana"**, e **não importa o que vem depois**. A consulta retornará registros como "Ana Paula", "Anabela", "Ana Clara", e assim por diante.

---

#### **NOT LIKE**


Também é possível usar o `LIKE` em conjunto com o `NOT` para **excluir** determinados padrões da busca.

```SQL title='SQL'
SELECT *
FROM Tabela
WHERE Nome NOT LIKE '%Silva%';
```
> Neste exemplo, estamos dizendo que **não queremos os registros cujo nome contenha "Silva"** **em nenhuma parte do texto**. Ou seja, nomes como "João da Silva", "Maria Silva Souza" ou "Silvana" não serão retornados.

---

### **IN**

A cláusula IN (Dentro) é usada para pegar os registos que se enquadaram em algum parâmetro específico, por exemplo, queremos pegar os dados de produtos que estão dentro dentro de uma categoria em específico:

```SQL title='SQL'
SELECT *
FROM Produtos
WHERE Categoria IN ('Tecnologia', 'Móveis');
```
> Agora, ele irá retornar todos os registros que estejam dentro da categoria de tecnologia e móveis.

---

#### **NOT IN**

Podemos também fazer a negação da cláusula IN, ou seja, tudo o que for especificado não irá ser retornardo na resposta da Query:

```SQL title='SQL'
SELECT *
FROM Produtos
WHERE Categoria NOT IN ('Alimentício');
```
> Ou seja, tudo o que for da categoria de alimentos, não será retornado na resposta da Query.

---

### **ORDER BY**

O Order By serve para ordenarmos os registros com base em um parâmetro especificado:

```SQL title='SQL'
SELECT *
FROM Produtos
ORDER BY Valor DESC;
```
> Ou seja, estamos ordenando **(`ORDER BY`)** os produtos por valor em ordem decrescente **(`DESC`)**

---

### **AS (Alias)**

O AS serve para definirmos um 'Apelido' para a tabela selecionada na hora da exibição do resultado da Query, muito útil para deixar a exibição visualmente mais atrativa quando se temos tabelas com nomes não tão claros:

```SQL title='SQL'
SELECT Nome as 'Nome do Cliente'
FROM Clientes;
```

> Dessa forma deixamos de forma específica do que a coluna se trata.

---
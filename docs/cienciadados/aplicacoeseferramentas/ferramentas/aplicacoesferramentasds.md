

## **As Principais Ferramentes Para Data Science**

<br>

### **Python e Bibliotecas Essenciais** <img src="../../../../assets/linguagem_python.png" width='50px' style='margin-left:1vw; border-radius: 2rem;'>

> Python é uma linguagem de programação de alto nível, interpretada e de propósito geral. Amplamente conhecida por sua legebilidade e sua sintaxe que facilita a escrita de código limpo e compreensível. No contexto da Ciência de Dados, Python é particularmente valorizado por sua versatilidade, extensa comunidade e a vasta gama de bibliotecas disponíveis que facilitam a análise de dados, modelagem estatística, Machine Learning, visualização dos dados, etc.

Bibliotecas essenciais em Data Science:

- Numpy,    
- Pandas,
- Scikit-learn,
- Matplotlib,
- Seaborn
- Plotly
- Jupyter Notebook

<br>
***

### **R e Suas Aplicações em Data Science** <img src="../../../../assets/linguagem_r.png" width='50px' style='margin-left:1vw; border-radius: 2rem;'>


> R é uma linguagem e um ambiente de software especializado em análise estatística, visualização gráfca e relatórios. Diferente de python que abrange diversas áreas, R é focada apenas em análise estatística, dedicada para análises complexas. R é similar ao SAS e ao IBM SPSS (plataformas proprietárias de análise estatística).

Aplicações de R em Data Science:

**Análise Estatística:** R é uma das ferramentas mais poderosas para estatística descritiva, inferencial e multivariada. Isso inclui testes de hipóteses, análise de regressão, ANOVA, entre outros.

**Machine Learning:** Embora R não seja amplamente utilizada para Machine Learning quanto Python, a mesma possui bons pacotes para isso, como caret, mr e randomForest, que são utilizados para classificação, regressão e clustering.

**Visualização dos Dados:** R é renomada por ter uma capacidade de gerar visualizações de dados de alta qualidade. Pacotes como ggplot2, lattice e plotly permitem a criação de gráficos complexos e esteticamente agradáveis.

**Manipulação de dados:** Pacotes como dplyr, tidyr e data.table oferecem poderosas ferramentas para manipulação dos dados, tornando o processo de limpeza e preparação dos dados mais eficiente.

**Bioestatística e Epidemiologia:** R é frequentemente utilizada em bioestatística para análise genética, ensaios clínicos e estudos epidemiológicos, graças a pacotes especializados como Bioconductor.

**Análise de Séries Temporais:** R tem capacidades avançadas para análises de séries temporais como pacotes como forecast e tseries, que são utilizados para modelar e prever dados temporais.

**Relatórios e Shiny Apps:** R facilita a criação de relatórios dinâmicos e interativos através de pacotes como knitr e rmarkdown. Além disso, com o shiny, é possível criar aplicativos web interativos diretamente em R para apresentar análises e resultados.


<br>
***

### **SQL e Consultas Para Análise de Dados** <img src="../../../../assets/linguagem_sql.png" width='50px' style='margin-left:1vw; border-radius: 2rem;'>

> SQL (Structured Query Language), é uma linguagem utilizada para gerenciar e manipular bancos de dados relacionais. Projetada para inserir, consultar, atualizar e gerenciar dados, SQL é a ferramenta padrão para operar banco de dados em muitas aplicações comerciais e sistemas de gerenciamento de banco de dados. Possui outras variações, como : HQL (Hive) e CQL (Cassandra). É possível ainda executar análises em SQL a partir de código Python ou R.

Exemplos de instruções SQL:

```sql

    SELECT nome, idade FROM table_usuarios WHERE idade > 18;

    -- Selecionando o nome e a idade (SELECT nome, idade),
    -- Da tabela usuários (FROM table_usuarios),
    -- Onde irá filtrar somente se a idade for maior que 18 (WHERE idade > 18).
```
<br>

```sql

    SELECT nome, salario FROM table_funcionarios ORDER BY salario DESC;

    -- Selecionando o nome e o salário (SELECT nome, salario),
    -- Da tabela de funcionários (FROM table_funcionarios),
    -- Ordendando pelos salários em ordes decrescente (ORDER BY salarion DESC).
```
<br>

```sql

    -- Podemos ainda utilizar funções, vejamos:

    SELECT DATE(data_venda) AS dia, SUM (valor)
    FROM table_vendas
    WHRE data_venda BETWEEN '2024-01-01' AND '2025-12-31'
    GROUP BY dia;

    -- Convertendo uma coluna em formato de data (SELECT DATE(data_venda)),
    -- Somando a coluna valor (SUM (valor)),
    -- Da tabela vendas (From table_vendas),
    -- Onde a data de venda (WHERE data_venda),
    -- Será entre 01/01/2024 (BETWEEN '2024-01-01'),
    -- Até 31/12/2025 (AND '2025, 12, 31'),
    -- Agrupando pelo dia (GROUP BY dia).
```

<br>
***




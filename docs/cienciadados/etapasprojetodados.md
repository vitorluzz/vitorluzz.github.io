
### **Etapas Principais para Implementação de um Projeto**

#### **ETAPAS:**

1. **Definição do Problema,**
2. **Coleta e Armazenamento de Dados,**
3. **Preparação e Limpeza de Dados,**
4. **Análise Exploratória dos Dados,**
5. **Modelagem Preditiva/Estatística,**
6. **Avaliação e Teste,**
7. **Entrega do Resultado.**

<br>
***

#### **1. Definição do Problema**

Para melhor definirmos o problema de negócio a ser tratado, podemos seguir esses passos:

1. Entendimento do Objetivo do Negócio,
2. Definição dos Objetivos do Projeto,
3. Identificação das Perguntas de Pesquisa,
4. Análise dos Dados Disponíveis,
5. Definição das Métricas de Sucesso,
6. Planejamento do Projeto.

<br>

***

#### **2. Coleta e Armazenamento de Dados**

Dados precisos e relevantes são a base para análise e insights valiosos. Vamos envolver as partes interessadas para definir os requisitos de dados é vital para o projeto.


Existem diversos métodos de coleta de dados, a escolha do método dependedo tipo do dado necessário e do contexto do projeto.


Garantir a qualidade dos dados é fundamental. Dados incompletos, incorretos ou desatualizados podem levar a conclusões errôneas. Técnicas de limpeza e validação de dados ajudam a manter a integridade da precisão dos dados coletados. 


O armazenamento dos dados deve ser eficiente e seguro. Podemos utilizar BD relacionais, BD NoSQL, DL's, DW's ou Data Lakehouse, são algumas das opções disponíveis


Proteger dados coletados é fundamental para manter a confiança e cumprir regulamentações. Implementar medidas de segurança ajuda a proteger os dados contra acessos não autorizados e violações.

A Coleta e Armazenamento dos Dados normalmente costuma ser responsabilidade do Engenheiro de Dados.

<br>
***

#### **3. Preparação e Limpeza de Dados**

A preparação de dados em Ciência de Dados é o processo de transformar dados brutos em um formato adequado para análise e modelagem. 


Envolvendo as etapas de:

- Limpeza,
- Transformação,
- Integração/Combinação,
- Codificação,
- Redução

É uma etapa essencial na preparação. Envolve a remoção de valores nulos, duplicados e inconsistentes. A normalização e padronização dos dados também se fazem necessárias para garantirmos a consistência.

A transformação inclui a conversão dos dados em formatos apropriados para análise. Isso pode envolver a agregação, codificação e criação de novas variáveis. Ajudando a tornar os dados úteis e compreensíveis.

A integração dos dados combina dados de diferentes fontes para fornecermos uma visão unificada. Podemos aplicar técnicas ETL (Extração, Transformação e Carga) para consolidarmos dados de sistemas diversos em um repositório central.

<br>
***

#### **4. Análise e Exploratória dos Dados**

A exploração e visualização dos dados é uma etapa crítica no fluxo de trabalho em Ciência de Dados. Também é conhecida como EDA.

Ela envolve a análise inicial dos dados para entender suas principais características, padrões e anomalias. Utilizando técnicas estatísticas descritivas e ferramentas de visualização para resumir as distribuições dos dados, identificar relações entre variáveis e detectar valores discrepantes (outliers).

A mesma é usada para auxiliar a formular hipóteses, escolher métodos de processamento apropriados e previnir erros que possam surgir devido a problemas nos dados. Também é usada na análise preliminar e criação de insights.

As representações visuais gráficas, visuais claras e informativas facilitam a interpretação de resultados por stakeholders não técnicos, como gerentes executivos.

Podemos aplicar a EDA antes ou depois da preparação dos dados. O objetivo principal é explorar os dados para compreender os padrões e detectar eventuais problemas. Podemos também aplicar a engenharia de atributos antes ou depois da EDA.
***
<br>

#### **5. Modelagem Preditiva / Estatística**

Modelagem Preditiva e Modelagem estatística são duas abordagens amplamente usadas em Ciência de Dados, mas possuem objetivos e metodologias diferentes.

Na Modelagem Estatística estamos interessados em analisar e explicar a relação entre variáveis.
*Exemplo: O número de quartos de uma casa, influencia no preço da casa?*


Na Modelagem Preditiva estamos interessados em usar variáveis para fazer previsões.
*Exemplo: Posso usar o tamanho da casa ou número de quartos para prever o preço da casa.*


Podemos usar a Modelagem Estatística como técnicas de seleção de variáveis em Modelagem Preditiva.


<br><br>

##### __<h2>Principais diferenças: Modelagem Preditiva / Estatística</h2>__
###### **<h3>Objetivo</h3>**

**Modelagem Estatística**

**Propósito:** Entender a relação entre as variáveis, identificar padrões e fazer inferências sobre populações baseadas em amostras.  


**Foco:** Estabelecer relações causais ou associativas, testar hipóteses e construir modelos explicativos.

<br>

**Modelagem Preditiva**

**Propósito:** Prever valores futuros ou resultados baseados em dados históricos.   

**Foco:**  Otimizar a precisão das previsões, muitas vezes sem se preocupar com a interpretabilidade do modelo.

<br>
<br>

###### **<h3>Abordagem</h3>**


**Modelagem Estatística**

**Métodos:** Usa técnicas como Regressão linear, ANOVA, Testes de hipóteses, entre outros.

**Suposições:** Geralmente assume que os dados seguem certas distribuições (por exemplo, normalidade) e que ha relações lineares entre variáveis

<br>

**Modelagem Preditiva**

**Métodos:** Inclui uma ampla gama de técnicas como aprendizado de máquina supervisionada (Árvore de decisões, Redes neurais, SVM), não supervisionado (clusterização), entre outros.

**Suposições:** Cada algoritmo pode ter suas próprias suposições que devem ser validadas. Foca mais na performance preditiva.

<br>
<br>

###### **<h3>Interpretação</h3>**

**Modelagem Estatística**

**Interpretação:** Resultados são interpretáveis e podem ser usados para inferir relações causais.

**Saída:** Coeficientes com significados claros, intervalos de confiança, valores p.

<br>


**Modelagem Preditiva**

**Interpretação:** Pode ser mais difícil de interpretar, especialmente com modelos complexos como redes neurais.

**Saída:** Foco na precisão das previsões, medidas de performance como AUC, precisão, recall, etc.

<br>
<br>

###### **<h3>Exemplos de uso</h3>**

**Modelagem Estatística**

- Usada para testar hipóteses (por exemplo, efeito de um medicamento em uma doença).
- Análises de pesquisas de mercado para entender a relação entre variáveis demográficas e comportamento de compra

<br>

**Modelagem Preditiva**

- Usada em negócios para prever vendas futuras, compras de clientes ou detecção de fraude.
- Aplicações em engenharia para prever falhas de máquinas ou manutenção preditiva.

<br>
<br>

###### **<h3>Ferramentas e Técnicas</h3>**

**Modelagem Estatística**

- **Ferramentas:** Linguagem R, Stata, SAS, SPSS, Linguagem Python (Statsmodels).
- **Técnicas:** Regressão Linear, Regressão Logística, ANOVA, Análise de Sobrevivência, Análise Fatorial, Métodos Probabilísticos, etc.

<br>


**Modelagem Preditiva**

- **Ferramentas:** Linguagem Python (Scikit-learn, PyTorch, TensorFlow), Linguagem R (caret, randomForest), Julia, Rust, C++, Java, JavaScript.
- **Técnicas:** Árvores de Decisão, Floresta Aleatória, Redes Neurais, Deep Learning, SVM, Boosting, Bagging, Regressão Linear, Regressão Logística, etc.

<br><br>

#### **6. Avaliação e Teste**

> Precisamos avaliar e testar as soluções que criamos durante o projeto de Ciência de Dados

Podemos utilizar algumas técnicas para realizar isso:

- Métricas de Avaliação,
- Validação Cruzada,
- Overfitting e Underfitting,
- Curvas de Aprendizado,
- Análise de Erros (Resíduos),
- BenchMarking.

#### **7. Entrega do Resultado**

> A entrega de um projeto de Ciência de Dados pode variar amplamente dependendo dos objetivos, do público alvo e do contexto do negócio. Normalmente a definição do entregável ocorre na fase de planejamento do projeto.   

Aqui estão algumas das principais opções de entregar um projeto de Ciência de Dados:

1. Relatório Técnico ou Científico,
2. Relatório Executivo,
3. Dashboard Interativo ou Infográfico (com Storytelling),
4. Jupyter Notebook,
5. Código Fonte e Documentação,
6. API (Application Programming Interface),
7. Aplicação Web para Deploy do Modelo de ML,
8. Previsões do Modelo de ML em Arquivo CSV,
9. Previsões do Modelo de ML em um Banco de Dados,
10. Simplesmente Entregamos o Arquivo do Modelo de ML.

<br>


## **Conceitos Fundamentais da Estatística**

- **População e Amostra:**
    - **População:** O conjunto completo de itens ou eventos de interesse.
    - **Amostra:** Um subconjunto da população selecionado para análise.
- **Probabilidade:** Usada para quantificar a incerteza e é a base para a estatística inferencial.
- **Variáveis:**
    - **Variáveis Quantitativas:** Variáveis numéricas que podem representar medidas ou contagens.
    - **Variáveis Qualitativas:** Variáveis categóricas que descrevem características (por exemplo: cor dos olhos, gênero).
- **Correlação e Regressão:**
    - **Correlação:** Medida da força e direção da relação entre duas variáveis
    - **Regressão:** Análise que descreve a relação entre uma variável dependente e uma ou mais variáveis independentes.

> Vamos entrar em detalhe em cada Conceito:

<br>

### **População e Amosta**

#### **Amostra**

É um subconjunto da população, selecionado para análise, com o objetivo de inferir ou estimar características da população inteira. 

A amostra deve ser representativa para garantir que as conclusões tiradas a partir dela sejam válidas para a população como um todo. Métodos de amostragem, como a amostragem aleatória, são usados para selecionar amostras de forma que minimizem vieses.


> Por que não analisamos a população inteira? Por que se faz necessário uma amostra?

Por diversas razões:
- Custo
- Tempo
- Necessidade

<br>

### **Correlação e Regressão**

#### **Correlação:**

É a medida da força e direção da relação entre duas variáveis

Calculamos o coeficiente da correlação e interpretamos o resultado:

- Correlação Próxima de +1 (Forte Correlação Positiva)
- Correlação Próxima de -1 (Forte Correlação Negativa)
- Correlação Próxima de 0 (Não Há Correlação)

**-> Devemos ter cuidado: CORRELAÇÃO NÃO IMPLICA CAUSALIDADE!**

> **Exemplo:**
>    
> No mês janeiro em Recife, é um mês **alta temporada, calor e muitos turistas visitando a praia,**
> Nesse mesmo mês aumenta o número de **ataques de tubarões,** pois, as pessoas estão indo mais a praia,
> E nesse mesmo mês aumenta mais o número de **consumo de sorvete.**
>
> Se fizermos uma análise de correlação, teremos uma forte **correlação positiva entre ataques de tubarões e consumo de sorvete**, mas, **isso faz sentido? Claro que não!** Por mais exista uma correlação positiva, **precisamos fazer uma análise complementar** para chegar à essa conclusão, pois, nesse caso, existe um **terceiro fator** que está causando ambas, que nesse cenário, é o calor.

Se duas variáveis estão altamente correlacionadas, isso não significa que uma está causando a outra.

<br>

#### **Regressão:**

É a análise que descreve a relação entre uma variável dependente e uma ou mais variáveis independentes.

<img src="../../../../assets/regressao.png" width='500px' style='margin-left:4vw; border-radius: 1rem;'>

> **Exemplo:**
>
> O gráfico ilustra a regressão, a relação da variável está no eixo X, que é o Tamanho da Casa, com a variável no eixo Y que é o Preço da Casa, a linha vermelha é a linha de regressão que encontramos através do modelo. A linha vermelha nos indica que existe uma relação linear positiva entre o tamanho da casa e o preço da casa, se aumenta o tamanho, também aumenta o preço. Se criamos um modelo a partir da regressão, podemos aplicar em qualquer cenário para sabermos o preço da casa.

<br>
<br>

### **Parâmetros X Estatísticas**

#### **Parâmetros** 

Características sobre a população. Valores calculados usando dados da população são chamados de parâmetros.

<br>

#### **Estatísticas**

Características sobre a amostra. Valores calculados usando dados da amostra são chamados de estatísticas.

<br><br>
***

### **Dados Primários X Dados Secundários**


**Dados:** Os dados são valores coletados através da observação ou medição.

**Informação:** Dados que são transformados em fatos relevantes e usados para um propósito específico.

> Dados não fazem sentido, se não forem colocados em contexto.

Os dados podem ser obtidos através de duas fontes principais:

**Dados primários:** São coletados por quem faz a análise, mais confiáveis, possuem maior controle.

**Dados secundários:** Coletados por terceiros, menos confiáveis, não possuem muito controle.

<br>
***

### **Observações X Variáveis**

Uma observação é uma ocorrência de um item específico que é gravada sobre uma unidade de dados. Também chamada de registro.

Variável é a característica de interesse que é medida em cada elemento da amostra ou população. Como o nome sugere, seus valores variam de elemento para elemento. As variáveis podem assumir valores numéricos ou não numéricos.

<img src="../../../../assets/observacoes.png" width='500px' style='margin-left:4vw; border-radius: 1rem;'>

<br>
***

### **Tipos de Variáveis**

As variáveis podem ser:

**Qualitativas** - Utilizam termos descritivos para descrever algo de interesse. Ex: cor dos olhos, estado civil, religião, gênero, grau de escolaridade, classe social, etc...

**Quantitativas** - Representadas por valores numéricos que podem ser contados ou medidos. Ex: número de filhos de uma família, peso do corpo humano, idade, número de crianças em uma sala de aua, etc...

<img src="../../../../assets/tiposvariaveis.png" width='500px' style='margin-left:4vw; border-radius: 1rem;'>

> Atenção, o tipo da variável pode depender ao contexto a ser trabalhado, EXEMPLO:

    Um dado classificado como "idade" é quantitativo.
    EX: 11, 15, 18, 22, 45 anos.

    MAS se esse dado for informado por "faixa etária" ele é qualitativo (ordinal).
    EX: 0 - 5 anos.
        0 - 12 anos.
        13 - 18 anos.
        19 - 28 anos.

> A importância de classificar os tipos de dados impactam na fase de escolher o melhor teste estatístico a ser utilizado na análise dos dados.

<br>
***

### **Teoria da Probabilidade**

A teoria da probabilidade é um ramo fundamental da Estatística que lida com a análise e quantificação  da  incerteza.  Ela  fornece  um  modelo matemático  para  entender  e  prever  o comportamento de sistemas complexos e fenômenos aleatórios. Alguns conceitos básicos:

**Experimento Aleatório:** É qualquer processo ou ação cujo resultado não pode ser previsto com certeza. Exemplos incluem lançar uma moeda, rolar um dado ou medir a temperatura em um dia específico.
 
**Espaço Amostral:** O  conjunto  de  todos  os  possíveis  resultados  de  um  experimento aleatório é chamado de espaço amostral. Por exemplo, o espaço amostral de um lançamento de moeda é {cara, coroa}.

**Evento:** Um evento é qualquer conjunto de resultados dentro  do espaço amostral. Um evento pode ser simples, como obter "cara" em um lançamento de moeda, ou mais complexo, como obter um número par ao rolar um dado.

**Probabilidade:** A probabilidade de um evento é uma medida que indica quão provável é que  esse  evento  ocorra.  É  um  número  entre  0  e  1,  onde  0  indica  impossibilidade  e  1  indica certeza.  A  probabilidade  de  um evento  é  definida  formalmente  como  o  número  de  resultados favoráveis dividido pelo número total de resultados possíveis no espaço amostral.

**Variáveis Aleatórias:** Uma variável aleatória é uma função que associa um número a cada resultado de um experimento aleatório. As variáveis aleatórias podem ser discretas (assumem valores contáveis) ou contínuas (assumem qualquer valor em um intervalo).

**Distribuição de Probabilidade:** Descreve como as probabilidades são distribuídas entre os  diferentes  resultados  possíveis  de  uma  variável  aleatória.  Exemplos  incluem  a  distribuição binomial   para  experimentos  com  dois  resultados  possíveis  e  a  distribuição  normal  para fenômenos que seguem um padrão de sino.

**Lei  dos  Grandes  Números:** Este  teorema  estabelece  que,  à  medida  que  o  número  de ensaios em um experimento aleatório aumenta, a média dos resultados tende a se aproximar do valor esperado.

**Teorema Central do Limite:** Um princípio poderoso na teoria da probabilidade que afirma que, sob condições bastante gerais, a distribuição da média de uma amostra grande extraída de uma    população    com    variância    finita    se    aproxima    de    uma    distribuição    normal, independentemente da forma da distribuição origina.

<br>
<br>
***
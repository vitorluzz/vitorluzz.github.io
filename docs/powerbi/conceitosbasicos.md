Iremos abordar alguns conceitos básicos sobre BI:

## Importação de dados

Primeiro passo, devemos clicar na opção 'Obter dados':
![alt text](../assets/importardados1.png)

Em seguida selecionar o tipo de dado do dataset que vamos manipular:
![alt text](../assets/importardados2.png)

Ao terminar de importar, deve-se verificar se foi importado de maneira correta, se não, ajustar, e em seguida clicar em 'Carregar':
![alt text](../assets/importardados3.png)

Para visualizar os dados carregados, clique na opção 'Modo exibição de tabela':
![alt text](../assets/importardados4.png)

E pronto, você terá a visualização de seus dados de forma tabular:
![alt text](../assets/importardados5.png)

> **IMPORTANTE:** O Power BI tem alguns limites em termos de carga de dados, se o volume de dados for elevado, não se pode fazer dessa maneira, deve colocar em um banco de dados e conectar o Power BI ao banco de dados!

### Cabeçalho do dataset

Muitas vezes, quando vamos carregar dados para a ferramente, ela não consegue identificar os dados da primeira coluna como um cabeçalho, então por padrão, o mesmo coloca os nomes como 'Coluna 1', 'Coluna 2', etc... Veja isso abaixo:

![alt text](cabecalhoerrado1.png)

> Podemos observar que a primeira linha é o cabeçalho, mas ele não conseguiu compreender isso!

Uma maneira fácil de fazer isso é antes mesmo de carregar esses dados, vamos em 'Transformar Dados':

![alt text](cabecalhoerrado2.png)

E então selecionar a opção 'Usar a Primeira Linha como Cabeçalho':
![alt text](cabecalhoerrado3.png) 

E pronto, já alteramos nosso cabeçalho para a forma correta!
![alt text](cabecalhoerrado4.png) 




---

## Tipos de Dados

Para sabermos os tipos de dados que estamos manipulando, podemos utilizar a aba de 'Transfomar dados':

![alt text](transformar.png)

> Ele irá nos dar a visão geral do data-set, no topo de cada coluna ele indica o tipo dos dados, 'ABC = Texto', '123 = Inteiro',  '1.2 = Decimal', etc.

---

## Cartão de visitas

Vamos clicar no ícone do 'cartão':

![alt text](cartao1.png)

Vamos selecionar o cartão inserido no tela de desenho e depois na aba de dados:
![alt text](cartao2.png)

E então, selecionamos o dado que deverá ser exibido nesse cartão, nesse caso, vamos selecionar o total de vendas:
![alt text](cartao3.png)

> Os dados que tem ao lado o símbolo de somatório **∑**, indicam que podemos fazer operações matemáticas com eles

---

## Gráfico Pizza

Vamos criar um gráfico de pizza, então, selecione a visualização desse gráfico:

![alt text](pizza1.png)

Então, vamos selecionar o campo 'Categoria':

![alt text](pizza2.png)

Então, vamos arrastar a categoria 'ID_Pedido' para o campo das visualizações 'Valores':
![alt text](pizza3.png)

E então, pronto, gráfico de pizza criado com sucesso!
![alt text](pizza4.png)

> **QUANDO USAR O GRÁFICO DE PIZZA?**
>
> Quando estamos manipulando poucas categorias, o gráfico de pizza é uma das melhores opções, porém, se for muitas categorias, ele se torna uma das piores opções!

---
## Gráfico de Barras Empilhadas

Vamos criar um gráfico de barras empilhadas, começando a selecionar a visualização desse gráfico:
![alt text](empilhadas1.png)

Vamos selecionar para o eixo Y os dados de 'Pais':
![alt text](empilhadas2.png)

Para o eixo X a contagem do 'ID_Pedido':
![alt text](empilhadas3.png)

E como legenda, a 'Prioridade':
![alt text](empilhadas4.png)

E pronto, dessa forma temos o nosso gráfico de barras empilhadas:
![alt text](empilhadas5.png)

> Importante se atentar aos Eixos e Legendas, pois fazem total diferença na apresentação dos dados.

---
## Gráfico de Barras Horizontais
Vamos criar um gráfico de barras horizontais, começando a selecionar a visualização desse gráfico:
![alt text](horizontal1.png)

Então, para o Eixo Y vamos selecionar os dados de 'SubCategoria':
![alt text](horizontal2.png)

E para o Eixo X, os dados de 'Desconto':
![alt text](horizontal3.png)

A ferramenta escolheu a 'Soma de Desconto' como padrão, mas, queremos a média, então, basta selecionar e alterar o comportamento:
![alt text](horizontal4.png)

---

## Gráfico de Colunas Clusterizado

> O gráfico de Barras pode parecer simples, porém, para ter a informação precisa, é necessário conhecimento sobre.

Estamos buscando saber a seguinte informação: Quantidade de vendas por 'Tem ou Não Tem Filhos em Casa'. Porém, quando estamos colocando as colunas nos eixos, devemos tomar cuidado, pois pode haver erros e exibir as informações de forma errada:
![alt text](graficobarras.png)

> Nesse cenário, foi preciso colocar a mesma coluna, tanto em Eixo X e em Eixo Y, o fator influenciador é a Legenda e a Contagem que faz toda diferença.
---
## Mapa Mundial

Vamos criar um Mapa com os dados, vamos selecionar a visualização 'Mapa':
![alt text](mapa1.png)

Como temos uma coluna 'Pais' em nosso dataset, vamos selecionar colocar ela no campo 'Localização':
![alt text](mapa2.png)

E para os dados de 'Total_Vendas' no campo 'Tamanho da Bolha':
![alt text](mapa3.png)

E selecionar a média de 'Total_Vendas':
![alt text](mapa4.png)

E então vamos ter um gráfico Mapa Mundial:
![alt text](mapa5.png)

---

## Gráfico de Cascata

Vamos selecionar o ícone do gráfico de cascata:
![alt text](cascata.png)

Coloque a coluna 'Modo Envio' para 'Categoria':
![alt text](cascata2.png)

E arraste o 'Valor Venda' para o 'Eixo Y':
![alt text](cascata3.png)

E pronto, temos o gráfico de cascata criado:
![alt text](cascata4.png)

> Esse gráfico é recomendado apenas quando se tem poucas categorias, quando se tem muitas, esse gráfico não é uma opção tão viável.

---
## Gráfico TreeMap

Selecione o ícone de visualização do 'Treemap':
![alt text](treemap1.png)

Então, vamos colocar a coluna 'Mercado' para a  'Categoria':
![alt text](treemap2.png)

Então, vamos colocar o 'Custo Envio' para 'Valores':
![alt text](treemap3.png)

E vamos colocar como 'Média de Custo de Envio':
![alt text](treemap4.png)

Pronto, gráfico treemap criado:
![alt text](treemap5.png)

---

## Gráfico de Dispersão

Vamos selecionar o ícone de visualização 'Gráfico de dispersão':
![alt text](dispersao1.png)

Para o eixo X, vamos selecionar o 'Salário Anual':
![alt text](dispersao2.png)

E para o eixo Y, selecionar o 'Gasto com Alimentos':
![alt text](dispersao3.png)
> Por padrão, o PowerBI ele tenta agrupar os dados, porém, nesse contexto, a soma dos dados nos retorna um gráfico sem sentido, vamos consertar isso.

Em vez da soma, para o 'Salario Anual', selecione 'Não resumir':
![alt text](dispersao4.png)


E pronto, temos um gráfico de dispersão criado:
![alt text](dispersao5.png)

>Se a variável discreta tiver poucos valores distintos (como "Sim" e "Não", ou "Baixo", "Médio", "Alto"), um gráfico de dispersão pode não ser o mais adequado — gráficos de caixa (boxplots) ou de barras podem transmitir melhor a informação. Pode haver sobreposição de pontos, dificultando a visualização, especialmente se a variável discreta tiver poucos valores.

---

## Árvore Hierárquica

Vamos selecionar o ícone de visualização 'Árvore hierárquica':
![alt text](arvore1.png)

Então, vamos selecionar a variável a ser analisada:
![alt text](arvore2.png)

Devemos escolher uma variável categórica para o 'Explicar por':
![alt text](arvore3.png)

E então, temos o gráfico criado, ao clicar, nós escolhemos como ele irá exibir esses dados:
![alt text](arvore4.png)

E pronto, podemos ter a visão específica do nosso dataset:
![alt text](arvore5.png)

---

## Matriz

> Funcionando como uma tabela, a matriz nos permite cruzar diversos dados.

Vamos selecionar o ícone de visualização da Matriz:

![alt text](matriz.png)

Vamos cruzar duas colunas na matriz:
![alt text](matriz2.png)

E então, cruzando mais colunas, podemos expandir a matriz deixando cada vez mais específico:
![alt text](matriz3.png)
---
## Indicador Chave de Performance (KPI)

Vamos selecionar o ícone de visualização 'Indicador':
![alt text](indicador.png)

Então, selecionar a coluna 'Valor Venda' para 'Valor':
![alt text](indicador2.png)

Vamos colocar como 'Média Valor Venda':
![alt text](indicador3.png)
> Por enquanto, a média não está associada a nenhuma categoria, a ferramenta fez apenas a média aritmética.

Vamos então colocar uma linha de meta para esse indicador, vamos colocar o valor de 350.
Vá nas opções de 'Formatar visual', depois em 'Eixo do Medidor', vamos ter algumas opções como 'Min', 'Max' e 'Destino':
![alt text](indicador4.png)
> O min, serve como o inicial para o indicador, o max serve para melhor dimensionarmos o gráfico, já o destino é como o alvo ou a meta do objetivo.

---
## Aplicando Filtros

O mapa está poluido, da forma que está dificulta a compreensão e visualização, vamos aplicar um filtro para olhar apenas alguns valores, vamos abrir a aba de filtros:

![alt text](filtros1.png)

Vamos selecionar a 'Média de total vendas':
![alt text](filtros2.png)

Selecionar que queremos ver somente 'quando for maior que':
![alt text](filtros3.png)

E colocar que queremos ver acima de '250':
![alt text](filtros4.png)

E então temos que aplicar os filtros selecionados:
![alt text](filtros5.png)

E então a visualização desse gráfico ficou mais limpa e fácil de compreender:
![alt text](filtros6.png)

---

## Segmentação dos Dados

A segmentação dos dados permite que o usuário possa filtrar os dados dos gráficos de maneira prática, para fazer isso, em visualizações clique em 'Segmentação dos Dados':
![alt text](segmento1.png)

E então, clicar na caixa de segmento criada e depois nos dados que será parâmetro para filtro, por exemplo, 'Pais':
![alt text](segmento2.png)

E então, de maneira fácil foi criado um filtro por Pais:
![alt text](segmento3.png)

Criei um segmento por 'Data_Pedido', como o tipo do dado é Data, ele já deixa em um formato adequado:
![alt text](segmento4.png)

Porém, queremos olhar apenas para os anos, então, vamos desmarcar a caixa 'Data_Pedido', expandir a 'Hierarquia de Datas' e selecionar apenas o 'Ano':
![alt text](segmento6.png)

---
## Títulos

Podemos adicionar uma caixa de texto com o título de nosso Dashboard criado, para isso, devemos ir em 'Inserir':
![alt text](titulo.png)

Depois selecionar a opção 'Caixa de texto':
![alt text](titulo2.png)

E então podemos criar diversos títulos informando o Dashboard:
![alt text](titulo3.png)

Podemos ainda modificar um título de um gráfico específico, vamos selecionar o gráfico e abrir a janela de 'Visualizaçãoes':
![alt text](titulo4.png)

Vamos então selecionar a opção de 'Formatar seu visual':
![alt text](titulo5.png)

Vamos selecionar a aba 'Geral' e então expandir o 'Título', podemos modificar o título de nosso gráfico:
![alt text](titulo6.png)

Então podemos dar um título personalizado, em negrito e centralizado:
![alt text](titulo7.png)

Modificando todos os títulos, deixamos de maneira mais agradável a leitura e exibição das análises:
![alt text](titulo8.png)

---

## Estilos

Podemos aplicar outros estilos para nosso Dashboard, vamos na seção 'Exibição':

![alt text](estilos1.png)


Clicando para expandir, podemos ver que tem diversos estilos disponíveis para aplicar aos modelos:
![alt text](estilos2.png)

Pronto, de maneira rápida alteramos o estilo de nosso Dashboard!
![alt text](image-3.png)

---

## Removendo Duplicatas nos Dados

Vamos no nosso editor PowerQuery, então clique na opção 'Transformar Dados':
![alt text](duplicatas1.png)

Selecione a tabela a ser manipulada:
![alt text](duplicatas2.png)

Então, clique com o botão direito no nome da coluna e vá na opção 'Agrupar por':
![alt text](duplicatas3.png)

Selecione a opção 'Contagem' e depois clique em 'Ok':
![alt text](duplicatas4.png)

E então, iremos ver que temos um ID duplicado, pois a contagem contou 2 IDS com o mesmo número:
![alt text](duplicatas5.png)

Clique nessa opção:
![alt text](duplicatas6.png)

E então, vá na opção 'Remover Duplicadas':
![alt text](duplicatas7.png)

E pronto, já foi removido os dados duplicados, clique em 'Fechar e Aplicar':
![alt text](duplicatas8.png)

---

## Criando Nova Coluna

Clique em 'Modo de Exibiçã de Tabela' e depois em 'Nova coluna':
![alt text](novacoluna1.png)

Então, irá abrir a caixa para colocar a fórmula da nova coluna,
Como estamos fazendo uma coluna de lucro, implementei da seguinte forma:
![alt text](novacoluna2.png)
> Primeiro o nome da nova coluna e então a regra que ele terá para definir os valores


E pronto, teremos uma nova coluna criada:
![alt text](novacoluna3.png)

> A grande vantagem é que podemos adicionar novas medidas às tabelas de dados que podemos usar para construção de gráficos.

---
### Nova Coluna com DAX

Vamos criar a coluna de margem de lucro com função DAX,
Vá em 'Modo exibição de tabela', selecione qual tabela terá a nova coluna, e depois vá em 'Nova coluna': 
![alt text](colunadax1.png)

Então, vamos usar a seguinte expressão DAX:
```SQL title='DAX'
MargemLucro = ROUND(DIVIDE(Vendas[Lucro], Vendas[Valor Venda]) * 100, 2)
```

> Ele está dividindo o Lucro de vendas pelo Valor Venda (DIVIDE), multipilicando por 100 para se ter o percentual (* 100) e depois arredondando para apenas 2 casas decimais (ROUND, 2).

![alt text](colunadax2.png)

E pronto, aplicando as alterações, já temos a nova coluna criada:
![alt text](colunadax3.png)

---

## Removendo Outliers

Quando identificado um Outlier, precisamos remover o mesmo, vá em 'Transformar Dados':
![alt text](outliers.png)

Vamos selecionar a coluna que se tem o outlier e colocar em ordem Crescente ou Decrescente para visualizar o outlier:
![alt text](outliers2.png)

E pronto, conseguimos identificar o outlier:
![alt text](outliers3.png)
> Podemos perceber que o segundo salário mais alto, é muito menor que o primeiro, isso impacta diretamente na construção dos gráficos.

Vamos selecionar 'Reduzir Linhas', 'Remover Linhas' e 'Remover Linhas Superiores', e então selecionar a primeira linha:
![alt text](outliers4.png)

E pronto, o outlier foi removido:
![alt text](outliers5.png)

---

## Criando Medidas

### SUMX

>**CENÁRIO:** Estamos trabalhando em um dataset onde se tem muitos gastos, porém, não se tem uma coluna com o total de gastos, vamos criar uma coluna pra isso.

No modo de exibição de tabela, vamos em 'Nova medida':
![alt text](medida1.png)


Vamos criar essa nova medida DAX:
```SQL title='DAX'
TotalGasto = SUMX(NomeDoDataset, NomeDoDataset[ColunaGasto1] + NomeDoDataset[ColunaGasto2] NomeDoDataset[ColunaGasto3])
```
![alt text](medida2.png)
>A função SUM ela faz o agrupamento geral, o SUMX faz o agrupamento por linha, nesse cenário ela é a melhor.

E pronto, a medida foi criada para que podemos usar em nossas visualizações!

---

### COUNTROWS

>**CENÁRIO:** Estamos trabalhando em um dataset onde se tem os dados de diversos funcionários, porém, queremos saber apenas a quantidade de funcionários.

Poderiamos criar uma medida DAX, tendo como premissa cada linha ser um funcionário:
```SQL title='DAX'
TotalFuncionarios = COUNTROWS(DatasetRH)
```
E pronto, contamos a quantidade de linhas e geramos uma nova medida! 

---

### CALCULATE

>**CENÁRIO:** Agora, queremos saber a quantidade de funcionários do sexo feminimo e masculino.

Podemos criar uma função DAX que calcula a quantidade de funcionários do sexo feminino:
```SQL title='DAX'
TotalFeminino = CALCULATE([TotalFuncionarios], DatasetRH[Genero] = "Feminino")
```

E essa outra função para o sexo masculino:
```SQL title='DAX'
TotalMasculino = CALCULATE([TotalFuncionarios], DatasetRH[Genero] = "Masculino")
```
---

## Substituição de Valores

> Quando trabalhamos com um dataset onde temos um valor que seja positivo e negativo, esse pode ser representado por 0 ou 1, sendo 0 a ação negativa e 1 a ação positiva. 

Vá em transformar valores:

![alt text](substituir.png)

Vá na coluna a ter os valores substituidos, clique com o botão direito e vá em 'Substituir valores':
![alt text](substituir2.png)

E então, vamos colocar para 1, o valor 'Sim' (Fazer o mesmo para 0 sendo 'Não'):
![alt text](substituir3.png)

Depois, fechar e aplicar para salvar as alterações:
![alt text](substituir4.png)

> Com isso facilitamos a interpretação de diversas visualizações, deixando o entendimento melhor.

---

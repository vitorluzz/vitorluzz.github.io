
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
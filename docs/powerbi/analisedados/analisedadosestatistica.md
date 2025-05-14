Sabemos que medidas como Média, Mediana, Mínimo, Máximo e Contagem são de fácil acesso na interface do Power BI. A própria ferramenta oferece recursos intuitivos para a criação dessas medidas básicas por meio de menus suspensos, botões de agregação e opções pré-configuradas nas visualizações. Para quem está começando, isso é uma vantagem, pois permite explorar os dados sem a necessidade imediata de escrever fórmulas.

No entanto, à medida que a análise se torna mais profunda e personalizada, algumas métricas estatísticas e cálculos específicos exigem conhecimento em DAX (Data Analysis Expressions) — a linguagem de expressões do Power BI.

## Moda

**CENÁRIO:** Queremos saber a medida da moda da altura de pacientes.

Vamos então, criar uma medida DAX para isso:

```DAX title='DAX'
ModaAltura = 
VAR TabelaFrequencia = 
    SUMMARIZE(
        dados_pacientes,
        dados_pacientes[altura(cm)],
        "Frequencia", COUNT(dados_pacientes[altura(cm)])
    )
VAR MaiorFrequencia = 
    MAXX(
        TabelaFrequencia,
        [Frequencia]
    )
RETURN
    CONCATENATEX(
        FILTER(TabelaFrequencia, [Frequencia] = MaiorFrequencia),
        dados_pacientes[altura(cm)],
        ", "
    )
```
> **O que esse código faz?**
>
> Eu crio uma variável chamada **"TabelaFrequencia"**, então faço a sumarização **(SUMMARIZE)** da tabela dados_pacientes, então busco a coluna altura e chamo isso de frequência e faço a contagem **(COUNT)** disso e chamo isso de **'Frequência'**. Então eu vou procurar a maior frequência **(MaiorFrequencia)**, ou seja, a frequência que aparece em mais quantidade de vezes, então, essa será a MaiorFrequencia, ou melhor, será a nossa Moda. Feito isso, irei retornar no formato concatenado **(CONCATENATEX)** e fazendo o filtro **(FILTER)** pelas variáveis criadas no item anterior. 


---

## Coeficiente de Variação

Sabemos que o cálculo do Desvio Padrão é facilmente acessível no Power BI, sendo uma medida estatística padrão disponível diretamente nas opções de agregação. No entanto, quando lidamos com variáveis de naturezas diferentes, como por exemplo idade e peso de pacientes, a simples análise da variância ou do desvio padrão pode gerar confusão — afinal, essas medidas não são diretamente comparáveis devido às suas unidades distintas.

É nesse cenário que o Coeficiente de Variação (CV) se torna extremamente útil. Por ser uma medida relativa (expressa geralmente em percentual), o CV permite comparar a variabilidade entre variáveis com escalas diferentes, facilitando a interpretação dos dados e a tomada de decisões.

Você pode preparar essa medida com linguagem DAX dessa forma:

```DAX title='DAX'
CVIdade = 
    DIVIDE(
        STDEV.P(dados_pacientes[idade(anos)]), 
        AVERAGE(dados_pacientes[idade(anos)])
        ) * 100
```

## Matplotlib

É um pacote python que nos permite criar gráficos, porém, eles serão criados via código python! É possível criar dashboards inteiras apenas com essa biblioteca.

Vamos instalar as dependências do matplotlib
```bash title='bash'
pip install matplotlib==3.7.1
```
***

Importando o MatPlotLib para utilização do mesmo
```python title='python'

import matplotlib as mpl
mpl.__version__
```
```python title='out:'
'3.7.1'
```
Talvez seja preciso dar um downgrade na sua versão do numpy!

Caso seja preciso, faça isso:
```bash title='bash'

pip install "numpy<2"
```
***

Vamos importar o pacote do pyplot da biblioteca do matplotlib!
```python title='python'

# O pyplot é um pacote dentro do matplotlib!
import matplotlib.pyplot as plt
%matplotlib inline
```

<br>
***


### Gráfico de Linha

O método plot define os eixos do gráfico
```python title='python'


plt.plot([1,3,5], [2,4,7])
plt.show()
```


<img src="../../../../assets/4b76a093-44de-4f1a-a395-afefe8891c53.png" style='width: 550px;'>
> com apenas 2 linhas de código é possível criar um gráfico de forma prática
    
<br>
***


Mais um gráfico de linha
```python title='python'

x = [2,3,5]
y = [3,5,7]

# passamos como parâmetro as listas
plt.plot(x,y)

# Damos um título pro eixo X
plt.xlabel('Variável 1')

# Damos um título pro eixo Y
plt.ylabel('Variável 2')

# Damos um título pro Gráfico em si
plt.title('Teste Plot')

# Exibir o gráfico
plt.show()
```


out:
<img src="../../../../assets/b3d89811-1f45-4f1c-8a25-96107bc9006c.png" style='width: 550px;'>



<br>
***


### Gráfico de Barras

Criando um gráfico de barras
```python title='python'

x1 = [2,4,6,8,10]
y1 = [6,7,8,2,4]

# Para criar o gráfico de barras, é preciso declarar o '.bar'
plt.bar(x1,y1, label = 'Barras', color = 'green')
plt.legend()
plt.show()
```

out:

<img src="../../../../assets/c98e7900-7b40-4409-8710-d6b35bb97032.png" style='width: 550px;'>
    
    
<br>
***


Criando dois gráficos de barras na mesma área de plotagem
```python title='python'

x2 = [1,3,5,7,9]
y2 = [7,8,2,4,2]

plt.bar(x1,y1, label = 'Listas1', color = 'blue')
plt.bar(x2,y2, label = 'Listas2', color = 'red')
plt.legend()
plt.show()
```


out:

<img src="../../../../assets/3bdaab56-3656-4bbc-9c60-f6e970e150e9.png" style='width: 550px;'>

>Como chamamos o método bar duas vezes, ele cria dois gráficos na mesma área de plotagem!
>Pode parecer que é apenas 1 gráfico, mas são dois que estão se combinando!

<br>
***




Criando um gráfico de barras com os índices criados a partir de um range a partir da lista de valores
```python title='python'

idades = [22, 65, 45, 55, 21, 22, 34, 42, 41, 4, 99, 101, 120, 122, 130, 111, 115, 80, 75, 54, 44, 64, 13, 18, 48]

# Criando um intervalo de valores com os índices da lista
ids = [x for x in range(len(idades))]

plt.bar(ids, idades)
plt.show()
```

out:

<img src="../../../../assets/11c81c00-67c9-457f-b676-60a0f986d1fd.png" style='width: 550px;'>

<br>

***

Criando um histograma de barras:
```python title='python'

bins = [0,10,20,30,40,50,60,70,80,90,100,110,120,130]

# Se parece com um gráfico de barra, mas não é!
# o rwidth define a largura de cada barra.
plt.hist(idades, bins, histtype = 'bar', rwidth = 0.5)
plt.show()
```

out:

<img src="../../../../assets/11c81c00-67c9-457f-b676-60a0f986d1fd.png" style='width: 550px;'>
    
<br>
***



Criando um gráfico de barras com as barras preenchidas umas com as outras
```python title='python'

# Com o stefilled, as barras ficaram preenchidas umas com as outras.
plt.hist(idades, bins, histtype = 'stepfilled', rwidth = 0.8)
plt.show()
```

out:

<img src="../../../../assets/066a6327-b135-49c4-9261-bf6c61b87808.png" style='width: 550px;'>
    
<br>
***



>Essa biblioteca nos permite customizar os gráficos com diversas opções!
>Importante sempre consultar a documentação para estudo.

URL: https://matplotlib.org/

### Gráfico de Dispersão (Scatter Plot)

Criando um gráfico de dispersão
```python title='python'

x = [1,2,3,4,5,6,7,8]
y = [5,2,4,5,6,8,4,8]

# Para chamarmos esse gráfico, utilizamos o 'scatter'
# Esse marker é como os pontos irão ser plotados no gráfico, pode ser *, um X, entre outros.
plt.scatter(x,y, label = 'Pontos', color = 'black', marker = 'o')
plt.legend()
plt.show()
```

out:

<img src="../../../../assets/77a12be8-1963-44bd-b356-2110ca40aa75.png" style='width: 550px;'>
    
<br>
***



### Gráfico de Área Empilhada

Basicamente um gráfico de área, mas na mesma área de plotagem

Criando um gráfico de área empilhada
```python title='python'

import matplotlib.pyplot as plt

# Dados
dias = [1, 2, 3, 4, 5]
dormir = [7, 8, 6, 7, 7]
comer = [2, 3, 4, 5, 3]
trabalhar = [7, 8, 7, 2, 2]
passear = [8, 5, 7, 8, 13]

# Criando o gráfico de áreas empilhadas
plt.stackplot(dias, dormir, comer, trabalhar, passear, colors=['m', 'c', 'r', 'k', 'b'], labels=['Dormir', 'Comer', 'Trabalhar', 'Passear'])

# Adicionando legenda e título
plt.legend(loc='upper left')
plt.title('Distribuição de Atividades ao Longo dos Dias')
plt.xlabel('Dias')
plt.ylabel('Horas')

# Exibir o gráfico
plt.show()
```

out:

<img src="../../../../assets/0af1ff12-4d36-4de5-86ca-56cdca2c2307.png" style='width: 550px;'>
    
    
<br>
***


### Gráfico de Pizza (Pie Plot)

Criando um gráfico de pizza
```python title='python'

# Aqui eu coloco os valores
fatias = [7,2,2,13]

# Aqui eu coloco os labels, ou seja, as fatias
atividades = ['dormir', 'comer', 'passear', 'trabalhar']

# crio uma lista de cores
cores = ['olive', 'lime', 'violet', 'royalblue']

# crio o pieplot, colocando os valores, as fatias, as cores, defino um ângulo para começar, 
# coloco uma sombra para estilizar e então defino que  a fatia comer irá ter o efeito de sendo retirada.
plt.pie(fatias, labels = atividades, colors = cores, startangle = 90, shadow = True, explode = (0,0.2,0,0))
plt.show()
```

out:

<img src="../../../../assets/0730e480-2409-4814-9c1b-c772f2008b49.png" style='width: 550px;'>
    
    
<br>
***


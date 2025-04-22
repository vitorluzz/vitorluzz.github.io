
## Seaborn
O Seaborn é uma biblioteca de visualização de dados para Python baseada no Matplotlib e integrada ao Pandas. Ele facilita a criação de gráficos estatísticos bonitos e informativos com poucas linhas de código.


URL: https://seaborn.pydata.org/

Instalando os pacotes necessários
```python title='python'

!pip install seaborn==0.12.2
```
***

Importando as bibliotecas que serão utilizadas
```python title='python'

import random
import numpy as np
import pandas as pd
import matplotlib as mat
import matplotlib.pyplot as plt
import warnings
warnings.filterwarnings('ignore')
import seaborn as sea
%matplotlib inline
```
<br>

***

### Criando os gráficos com Seaborn

Carregando um dos datasets que vem com o seaborn para estudo
```python title='python'

dados = sea.load_dataset("tips")

dados.head()
```


out:

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>total_bill</th>
      <th>tip</th>
      <th>sex</th>
      <th>smoker</th>
      <th>day</th>
      <th>time</th>
      <th>size</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>16.99</td>
      <td>1.01</td>
      <td>Female</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>2</td>
    </tr>
    <tr>
      <th>1</th>
      <td>10.34</td>
      <td>1.66</td>
      <td>Male</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>3</td>
    </tr>
    <tr>
      <th>2</th>
      <td>21.01</td>
      <td>3.50</td>
      <td>Male</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>3</td>
    </tr>
    <tr>
      <th>3</th>
      <td>23.68</td>
      <td>3.31</td>
      <td>Male</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>2</td>
    </tr>
    <tr>
      <th>4</th>
      <td>24.59</td>
      <td>3.61</td>
      <td>Female</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>4</td>
    </tr>
  </tbody>
</table>
</div>

<br>
***

Criando gráficos bivariados e univariados na mesma área de plotagem
```python title='python'

# O método joinplot cria plot de 2 variáveis com gráficos bivariados e univariados
sea.jointplot(data = dados, x = 'total_bill', y = 'tip', kind = 'reg')
```



out:

<img src="../../../../assets/b35ff9a5-54a0-49f3-9ebc-c7f42682f650.png" style='width: 550px;'>
    
    


 Ele retorna um gráfico que diz: Os pontos são a relação entre valor da conta e gorjeta, a linha azul diagonal é o modelo de regressão, a área sombreada entre ela é o intervalo sendo a margem de erro, temos o histograma da variável total_bill e o gráfico de densidade! Tanta coisa em apenas 1 gráfico!
<br><br>
***

Criando um gráfico que contém modelos de regressão
```python title='python'

# O método lmplot() cria a plot com dados e modelos de regressão
sea.lmplot(data = dados, x = 'total_bill', y = 'tip', col = 'smoker')
```



out:

<img src="../../../../assets/76b4066e-200f-4586-ba2e-42a1287a8a4b.png" style='width: 550px;'>
    
>Temos a linha de regressão entre total_bill e tip, isso quando, o cliente era fumante ou não (Smoker True ou False)

<br>
***

Vamos criar um DF vazio
```python title='python'

# Criando um dataframe vazio
df = pd.DataFrame()
```

Vamos preencher o DF com valores vazios
```python title='python'

# Alimentando o dataframe com valores aleatórios
df['idade'] = random.sample(range(20, 100), 30)
df['peso'] = random.sample(range(55, 150), 30)
```

Verificando a forma do  DF
```python title='python'

df.shape
```
```
out: (30, 2)
```

<br>
***

Visualizando os dados com pandas:
```python title='python'

df.head()
```

out:

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>idade</th>
      <th>peso</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>24</td>
      <td>58</td>
    </tr>
    <tr>
      <th>1</th>
      <td>81</td>
      <td>68</td>
    </tr>
    <tr>
      <th>2</th>
      <td>86</td>
      <td>133</td>
    </tr>
    <tr>
      <th>3</th>
      <td>48</td>
      <td>69</td>
    </tr>
    <tr>
      <th>4</th>
      <td>58</td>
      <td>97</td>
    </tr>
  </tbody>
</table>
</div>

<br>

***

### Gráfico de dispersão

Criando um gráfico de dispersão com um modelo de regressão na mesma área de plotagem
```python title='python'

# O fit_reg nos retorna um modelo de regressão
sea.lmplot(data = df, x = 'idade', y = 'peso', fit_reg = True)
```

out:

<img src="../../../../assets/4687b802-2f92-4c93-b0a8-c960d5e16df6.png" style='width: 550px;'>
    
    
<br>

***

### Gráfico de densidade

Criando um gráfico de densidade
```python title='python'

# Gráfico de densidade
sea.kdeplot(df.idade)
```


out:

<img src="../../../../assets/1b407f26-4b07-464e-a3ac-5f9dab62180c.png" style='width: 550px;'>
    
    
<br>

***

### Gráfico de densidade com histograma

Criando um gráfico de densidade com um histograma na mesma área de plotagem
```python title='python'

sea.distplot(df.peso)
```

out:

<img src="../../../../assets/8db79e58-f7c5-4b51-99f5-6b163c51ce15.png" style='width: 550px;'>
    
    
<br>

***

### Histograma

Criando um histograma com um rugplot incluso
```python title='python'

# Utilizando o histograma do matplotlib, com o rugplot do seaborn
plt.hist(df.idade, alpha = .3)
sea.rugplot(df.idade)
```

out:

<img src="../../../../assets/a142f86c-e54a-49fc-a9c9-8ac25d76c9bc.png" style='width: 550px;'>
    
    
<br>

***

### BoxPlot

Criando um gráfico boxplot
```python title='python'

sea.boxplot(df.idade, color = 'm')
```



out:

<img src="../../../../assets/645464e5-6ae8-4014-bb49-6817bb89b344.png" style='width: 550px;'>
    
    


***

### Violin Plot

Criando um gráfico Violin
```python title='python'

sea.violinplot(df.peso, color = 'cyan')
```


out:

<img src="../../../../assets/d455edef-13d7-4edf-adcd-3aee6dfa815c.png" style='width: 550px;'>
    
    


***

### Cluster Map

Criando um Gráfico Cluster Map
```python title='python'

sea.clustermap(df)
```

out:

<img src="../../../../assets/4602455f-b891-4c38-8440-145295056d76.png" style='width: 550px;'>
    
    
<br>

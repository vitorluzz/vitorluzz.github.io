
## Matplotlib, Seaborn, NumPy e Pandas na criação de gráfico estatístico

Vamos utilizar todas as bibliotecas para criar um gráfico de dispersão com um modelo de regressão


Criando os dados a serem manipulados
```python title='python'

# valores randômicos
np.random.seed(42)
n = 1000
pct_smokers = 0.2

# Variáveis
flag_fumante = np.random.rand(n) < pct_smokers
idade = np.random.normal(40,70, n)
altura = np.random.normal(170,10,n)
peso = np.random.normal(70,10,n)

# DataFrame
dados = pd.DataFrame({'altura': altura, 'peso': peso, 'flag_fumante': flag_fumante})

# Cria os dados para a variável fumante
dados['flag_fumante'] = dados['flag_fumante'].map({True: 'Fumante', False: 'Não Fumante'})
```

Visualizando os dados
```python title='python'

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
      <th>altura</th>
      <th>peso</th>
      <th>flag_fumante</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>155.936825</td>
      <td>78.745171</td>
      <td>Não Fumante</td>
    </tr>
    <tr>
      <th>1</th>
      <td>169.168944</td>
      <td>63.502348</td>
      <td>Não Fumante</td>
    </tr>
    <tr>
      <th>2</th>
      <td>154.952796</td>
      <td>57.967991</td>
      <td>Não Fumante</td>
    </tr>
    <tr>
      <th>3</th>
      <td>177.600560</td>
      <td>59.579556</td>
      <td>Não Fumante</td>
    </tr>
    <tr>
      <th>4</th>
      <td>170.824398</td>
      <td>65.127971</td>
      <td>Fumante</td>
    </tr>
  </tbody>
</table>
</div>

<br>

Criando o gráfico de dispersão
```python title='python'

# Style
sea.set(style = 'ticks')

# lmplot
sea.lmplot(x = 'altura',
          y = 'peso',
          data = dados,
          hue = 'flag_fumante',
          palette = ['tab:blue', 'tab:orange'],
          height = 7)

# Labels e Título
plt.xlabel('Altura (cm)')
plt.ylabel('Peso (kg)')
plt.title('Relação entre altura e peso de fumantes e não fumantes')

# Remove as bordas
sea.despine()

# Mostrando o gráfico
plt.show()
```

out:

<img src="../../../../assets/b875660a-c3f8-4255-b2b3-a638c65509c8.png" style='width: 550px;'>


<br>
<br>
<br>


Podemos criar infinidades de gráficos, muitos com apenas 1 linha de código, se termos o conhecimento de como manipularmos, o céu é o limite.

> Existem milhares de formas de fazer a mesma coisa, mas, a sua capacidade de profissional que define qual a melhor ferramenta e forma de fazer com base em cada caso e demanda.
    


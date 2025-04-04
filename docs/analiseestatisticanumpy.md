ㅤ
## **Análise Estatística Básica com NumPy**

### Média
```
python

arr14 = np.array([15,23,63,94,75])
```
Calculando a média de um conjunto de valores
```
python

np.mean(arr14)
```
```
out: 54.0
```


***
ㅤ

### Calcular Desvio Padrão (Standard Deviation)

>O desvio padrão é uma medida estatística de dispersão que indica quanto os valores de um conjunto de dados se afastam da média. Ele é calculado como a raiz quadrada da variância que é a média dos quadrados das diferenças entre cada valor e a média. Com isso, conseguimos calcular a variabilidade dos dados em torno da média, se os valores estiverem próximos da média, o desvio padrão será baixo, porém se estiverem distantes, o desvio será alto. ** Muito utilizado em análise de dados! **

```
python

# Desvio padrão 
np.std(arr14)
```
```
out: 30.34468652004828
```


***
ㅤ

### Variância

>A variância é uma medida estatística que quantifica a dispersão dos valores em um conjunto de dados em relação à média. Ela é calculada como a média dos quadrados das diferenças entre cada valor e a média.

```
python

np.var(arr14)
```
```
out: 920.8
```

A variância e o desvio padrão são medidas de dispersão dos dados. A variância é uma medida quadrática que pode ser usada para calcular outras estatísticas, mas seus valores costumam ser elevados, dificultando a interpretação. O desvio padrão, que é a raiz quadrada da variância, tem a mesma unidade dos dados, facilitando a análise. O desvio padrão é mais utilizado por ser mais intuitivo, mas a escolha entre ele e a variância depende do contexto da análise.


ㅤ
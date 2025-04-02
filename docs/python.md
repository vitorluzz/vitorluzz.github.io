# **Conceitos Básicos - Python**
## **Primeiros Exemplo**

```python
print('Primeiro programa')
1 \
  + 2

# o Python ele se importa com quebras de linha, diferentes de outras linguagens!!!
```
<br>
<br>

## **TIPOS**
### **Tipos Básicos!**

```
python

print(True)   # Booleano (Verdadeiro)
print(False)  # Booleano (Falso)
print(1.2 + 1)  # Número decimal (float)
print("Texto")  # String
print('Você é ' + 3 * 'muito ' + 'legal!')  # Concatenação de strings
```

📌 Python é uma linguagem dinamicamente tipada, ou seja, você não precisa declarar o tipo de uma variável explicitamente.

<br>
<br>

### **Váriaveis**
As variáveis armazenam valores e podem ser utilizadas ao longo do código:
```
python

a = 10
b = 5.2

print(a + b)  # Soma dos valores
```
```
out: 15.2
```

### **Listas**

Listas são coleções ordenadas de elementos.

```
python

numeros = [1, 2, 3, 4, 5]
print(numeros[0])  # Primeiro elemento -> 1
```
```
out: 1
```

Manipulação de listas:
As listas são coleções ordenadas e mutáveis.
```python
numeros.append(6)  # Adiciona o número 6
print(numeros)
```
```
out: [1,2,3,4,5,6]
```
<br>
<br>

### **Dicionários**

Dicionários armazenam pares de chave-valor.

```
python

pessoa = {"nome": "João", "idade": 20}
print(pessoa["nome"])  
```
```
out: ["João"]
```
<br>

Adicionando novos valores:

```
python

pessoa["cidade"] = "São Paulo"
print(pessoa)
```
```
out: {"nome": "João", "idade": 20, "cidade": "São Paulo"}
```
<br>
<br>

### **Conjuntos**

Conjuntos armazenam elementos únicos e não ordenados.

```
python

numeros = {1, 2, 3, 4, 5}
numeros.add(6)
print(numeros)
```
```
out: {1,2,3,4,5,6}
```
<br>
<br>

### **Tuplas**

Tuplas são similares a listas, mas são imutáveis.

```
python

tupla = (1, 2, 3)
print(tupla[0])  
```
```
out: 1
```

<br>
<br>

## **Comentários**
Comentários são trechos de código ignorados pelo interpretador.
```
python

# Variáveis de exemplo
salario = 3450.45
despesas = 2456

"""
Este é um comentário de várias linhas.
Aqui podemos documentar o código de forma mais detalhada.
"""

print("Chegou ao Fim!")
```
<br>
<br>

## **OPERADORES**
### **Operadores Aritméticos**

```
python

print(2 + 3)  # Soma
print(4 - 7)  # Subtração
print(2 * 5.3)  # Multiplicação
print(9.4 / 3)  # Divisão
print(9.4 // 3)  # Divisão inteira
print(2 ** 8)  # Exponenciação
print(10 % 8)  # Módulo (resto da divisão)
```

<br>
<br>

### **Operadores de Comparação**

Os operadores de comparação são usados para comparar valores.

```
python

x = 10
y = 5

print(x == y)  # Igual a -> False
print(x != y)  # Diferente de -> True
print(x > y)   # Maior que -> True
print(x < y)   # Menor que -> False
print(x >= y)  # Maior ou igual a -> True
print(x <= y)  # Menor ou igual a -> False
```

<br>
<br>

### **Operadores Lógicos**

Os operadores lógicos são usados para combinar expressões booleanas.

```
python

cond1 = True
cond2 = False

print(cond1 and cond2)  # AND -> False
print(cond1 or cond2)   # OR -> True
print(not cond1)        # NOT -> False
```

<br>
<br>

## **CONTROLE**
### **Estruturas Condicionais**

As estruturas condicionais permitem que o código tome decisões com base em condições.

```
python

idade = 18
if idade >= 18:
    print("Maior de idade")
else:
    print("Menor de idade")
```
```
out: "Maior de idade"
```
<br>

Também podemos usar a estrutura `elif` para múltiplas condições:

```
python

nota = 7
if nota >= 9:
    print("Excelente")
elif nota >= 7:
    print("Bom")
elif nota >= 5:
    print("Regular")
else:
    print("Reprovado")
```
```
out: "Bom"
```

<br>
<br>

### **Estruturas de Repetição**

As estruturas de repetição permitem executar um bloco de código várias vezes.

#### **Loop `for`**

```python
for i in range(5):  # Itera de 0 a 4
    print(i)
```

Percorrendo listas:

```python
nomes = ["Alpha", "Bravo", "Charlie"]
for nome in nomes:
    print(nome)
```
```
out:    Alpha
        Bravo
        Charlie 
```

<br>
<br>

#### **Loop `while`**

```
python

contador = 0
while contador < 5:
    print(contador)
    contador += 1
```
```
out: 0
     1
     2
     3
     4
```

<br>
<br>

## **Funções**

As funções permitem reutilizar blocos de código.

```
python

def saudacao(nome):
    return f"Olá, {nome}!"

print(saudacao("Camila"))
```
```
out: "Olá, Camila!"
```

<br>

Função com múltiplos argumentos:

```
python

def soma(a, b):
    return a + b

print(soma(3, 4)) 
```
```
out: 7
```
<br>
<br>


## **Manipulação de Strings**

```
python

texto = "Python é incrível!"
print(texto.upper())  # Transforma em maiúsculas
print(texto.lower())  # Transforma em minúsculas
print(texto.split())  # Divide a string em uma lista
```
```
out: PYTHON É INCRÍVEL!
     python é incrível!
     ['Python', 'é', 'incrível!']
```
<br>
<br>

## **Entrada e Saída**

```
python

nome = input("Digite seu nome: ")
print(f"Bem-vindo, {nome}!")
```

<br>
<br>

## **Tratamento de Exceções**

```
python

try:
    resultado = 10 / 0
except ZeroDivisionError:
    print("Erro: divisão por zero não permitida")
```
```
out: "Erro: divisão por zero não permitida"
```


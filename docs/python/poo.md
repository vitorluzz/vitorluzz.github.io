# POO (Programação Orientada a Objeto) - Python
## Classes

>Em POO (Programação Orientada a Objeto), classe é a estrutura que descreve um objeto, contendo valores, atributos e comportamentos.
>Cada objeto criado a partir da mesma classe terá os mesmos atributos e comportamentos.
***

Para criar uma Classe, utiliza-se a palavra reservada `class`.
É uma convenção usar a primeira letra maiúscula em cada palavra no nome da classe!

```python title='python'

# Criando a classe
class Livro():
    
    # quando você ver o nome __init__, é um método Construtor, usado para inicializar os atributos de uma classe.
    def __init__(self, titulo, isbn):
        self.titulo = titulo
        self.isbn = isbn
        print("Seu construtor foi criado!")
        
    def imprime(self, titulo, isbn):
        print(f"Foi criado o livro {titulo} com ISBN {isbn}")
```

Em Python, a palavra reservada `self` é uma referência ao objeto atual da classe. Quando um objeto é criado a partir de uma classe, `self` se refere a esse objeto específico.

```python title='python'

# Criando um objeto a partir da classe
meu_livro = Livro("Python para Iniciantes", "1234567890")
meu_livro.imprime(meu_livro.titulo, meu_livro.isbn)
```
***

## Herança

A herança permite que uma classe herde atributos e métodos de outra classe, promovendo a reutilização de código.

```python title='python'

# Criando uma classe que herda de Livro
class Ebook(Livro):
    def __init__(self, titulo, isbn, formato):
        super().__init__(titulo, isbn)
        self.formato = formato
        
    def imprime_formato(self):
        print(f"O eBook está no formato {self.formato}")
```

```python title='python'

# Criando um objeto da classe Ebook
meu_ebook = Ebook("Python Avançado", "9876543210", "PDF")
meu_ebook.imprime(meu_ebook.titulo, meu_ebook.isbn)
meu_ebook.imprime_formato()
```

***

## Polimorfismo
    
É o conceito que permite que objetos de diferentes classes possam ser tratados de forma uniforme. Significa que um objeto pode ser tratado como se fosse um objeto de uma superclasse, mesmo que ele seja de uma subclasse.

```python title='python'

class Impressora():
    def imprimir(self):
        print("Imprimindo um documento genérico...")

class ImpressoraLaser(Impressora):
    def imprimir(self):
        print("Imprimindo um documento com qualidade laser...")

class ImpressoraJatoDeTinta(Impressora):
    def imprimir(self):
        print("Imprimindo um documento com qualidade jato de tinta...")
```

```python title='python'

# Criando objetos das classes
impressora1 = ImpressoraLaser()
impressora2 = ImpressoraJatoDeTinta()

# Chamando o método imprimir, cada classe tem um comportamento diferente
impressora1.imprimir()
impressora2.imprimir()
```

>Com o polimorfismo, podemos usar o único nome do método, para que ele tenha comportamentos diferentes no objeto!

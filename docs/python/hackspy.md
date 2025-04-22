## 🐍 Introdução

Seja bem-vindo! Aqui você vai encontrar **hacks**, **dicas** e outras sacadas maneiras para mandar bem em **Python**!

## 📦 Requirements — Como gerenciar dependências no seu projeto

Quando criamos um projeto Python, é essencial garantir que qualquer pessoa consiga rodá-lo com todas as bibliotecas necessárias. Pra isso, usamos o famoso **`requirements.txt`** — ele lista tudo que seu projeto precisa pra funcionar direitinho.

Existem duas formas de gerar esse arquivo:  
**Manual** ou utilizando uma ferramenta chamada **Poetry**.

### ✍️ Modo manual (clássico e direto)

```bash
pip freeze > requirements.txt
```

Esse comando “congela” o estado atual do seu ambiente Python, listando todas as libs instaladas e salvando no arquivo requirements.txt.

---

Depois, quem for usar seu projeto, basta rodar


```bash title='bash'
pip install -r requirements.txt
```

```python title='python'
print('Hello World')
```
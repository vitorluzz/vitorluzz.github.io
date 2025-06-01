# 🐍 Python Hacks!

Se liga! Aqui você vai encontrar **hacks**, **dicas** e outras sacadas maneiras pra mandar bem em **Python** — seja no terminal, nos projetos ou na organização do código. 🚀

## 📦 Requirements — Como gerenciar dependências no seu projeto

Sempre que criamos um projeto em Python, é fundamental garantir que **qualquer pessoa consiga rodá-lo com todas as bibliotecas certas**. Pra isso, usamos o famoso arquivo: `requirements.txt`, Ele lista tudo o que seu projeto precisa pra funcionar perfeitamente — sem dor de cabeça.


Existem duas formas de gerar esse arquivo:  
**Manual** ou utilizando uma ferramenta chamada **Poetry**.

### ✍️ Modo manual (clássico e direto)

```bash title='bash'
pip freeze > requirements.txt
```

Esse comando “congela” o estado atual do seu ambiente Python, listando todas as libs instaladas e salvando no arquivo requirements.txt.

---

Depois, quem for usar seu projeto, basta rodar


```bash title='bash'
pip install -r requirements.txt
```
> E pronto, você já instalou as dependências necessárias para isso!
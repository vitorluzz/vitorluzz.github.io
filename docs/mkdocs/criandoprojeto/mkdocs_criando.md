> Essa página foi criada com base na documentação oficial do MkDocs Material, caso queira se aprofundar em outros conceitos, acesse a documentação oficial: [MkDocs-Material-Getting started](https://squidfunk.github.io/mkdocs-material/getting-started/)  


## Criando o Projeto

> Vamos criar seu projeto em **APENAS 9 passos!**  
>
> 💡 Os comandos abaixo são para **Linux**, mas funcionam em outros sistemas com pequenas adaptações.

---

### 1️⃣ Criar o diretório do projeto:

```bash title='bash'

mkdir seunome.github.io
cd seunome.github.io
```

---

### 2️⃣ Abrir o projeto no editor:

> Utilizaremos o **Visual Studio Code**, mas pode usar qualquer outro editor.

```bash title='bash'

code .
```

---

### 3️⃣ Abrir o terminal no VSCode:

- Atalho: `Ctrl + Shift + '`
- Ou: Menu `... > Terminal > New Terminal`

---

### 4️⃣ Criar o ambiente virtual (venv):

```bash title='bash'

python -m venv .venv
```
OU
```bash title='bash'

python3 -m venv .venv
```

---

### 5️⃣ Ativar o ambiente virtual:

```bash title='bash'

source .venv/bin/activate
```

> ✅ Após ativar, verá algo como `(.venv)` no início da linha de comando.

---

### 6️⃣ Instalar o MkDocs Material:

```bash title='bash'

pip install mkdocs-material
```

---

### 7️⃣ Criar o projeto MkDocs:

```bash title='bash'

mkdocs new .
```

---

### 8️⃣ Alterar o arquivo `mkdocs.yml`:

Edite o arquivo `mkdocs.yml` e substitua pelo conteúdo abaixo:

```yaml title='yaml'
site_name: My site
site_url: https://mydomain.org/mysite
theme:
  name: material
```

---

### 9️⃣ Rodar o projeto localmente:

```bash title='bash'

mkdocs serve
```

Acesse `http://127.0.0.1:8000/mysite/` no navegador para visualizar o site.  
> Para parar o servidor local, use `CTRL + C`.

---

> ✅ Pronto! Seu projeto MkDocs está funcionando localmente e pronto para ser publicado!

---

<br>


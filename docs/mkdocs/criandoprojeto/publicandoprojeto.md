> Essa página foi criada com base na documentação oficial do MkDocs Material, caso queira se aprofundar em outros conceitos, acesse a documentação oficial: [MkDocs-Material- Publishing your site](https://squidfunk.github.io/mkdocs-material/getting-started/)  

## Publicando no GitHub

### 1️⃣ Criar repositório remoto:

No GitHub, crie um repositório com o seu nome de usuário GitHub: `seunome.github.io`  
Marque a opção para incluir o README.

---

### 2️⃣ Inicializar repositório local:

No terminal do VSCode:

```bash title='bash'

git init
```

---

### 3️⃣ Adicionar repositório remoto:

```bash title='bash'
git remote add origin https://github.com/seunome/seunome.github.io.git
```
---
### 4️⃣ Adicionando a Git Ignore:

```bash title='bash'
curl -o .gitignore https://www.toptal.com/developers/gitignore/api/python,visualstudiocode,pycharm+all
```

---

### 5️⃣ Fazer o deploy com MkDocs:

```bash title='bash'

mkdocs gh-deploy --force
```

> ⚠️ Esse comando gera e publica seu site automaticamente no GitHub Pages!

---

### 6️⃣ Adicionar arquivos ao Git:

```bash title='bash'

git add .
```

---

### 7️⃣ Fazer commit:

```bash title='bash'

git commit -m "Adicionando meu projeto MkDocs! \o/"
```

---

### 8️⃣ Enviar para o repositório remoto:

```bash title='bash'

git push -u origin master
```

> Use `-u origin master` apenas na primeira vez para vincular a branch.

---

### 9️⃣ Alterar a branch padrão no GitHub:

1 - Vá em **Settings** do seu repositório.

<img src="../../../../assets/passo1.png" width='1000px' style='border-radius: 0.5rem;'>

<br>


2 - Clique na opção de alterar a branch:

<img src="../../../../assets/passo2.png" width='1000px' style='border-radius: 0.5rem;'>

<br>

3 -  Clique na branch 'gh-pages' e depois em 'Update':

<img src="../../../../assets/passo3.png" width='1000px' style='border-radius: 0.5rem;'>

<br>

4 - Confirme as alterações:

<img src="../../../../assets/passo4.png" width='1000px' style='border-radius: 0.5rem;'>

---

> 🟢 Após isso, seu site estará disponível em:  
> `https://seunome.github.io`

---

## Dicas Finais

- O nome do repositório **deve ser idêntico ao seu usuário GitHub** para funcionar como `seunome.github.io`.
- Adicione um bom `README.md` explicando seu projeto.
- Use **Shields.io** para adicionar selos e status visuais ao seu README.
- Explore a aba **Projects** no GitHub para usar o Kanban integrado!


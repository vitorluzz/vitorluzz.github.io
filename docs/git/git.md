# 🛠️ Git e GitHub – Guia Completo
## 📌 Introdução
### O que é o GitHub?

O **GitHub** é uma plataforma de hospedagem de código-fonte que utiliza o **Git** como sistema de controle de versões. Ele permite que desenvolvedores e equipes colaborem em projetos de software de forma organizada, eficiente e segura.

Com o GitHub, você pode:

- Armazenar seus projetos e mantê-los versionados;
- Trabalhar em equipe com controle sobre cada modificação feita;
- Criar e gerenciar issues, tarefas e bugs;
- Publicar sites com **GitHub Pages**, como portfólios ou documentações;
- Exibir seu trabalho para a comunidade e até usá-lo como um **currículo online**.

> 💡 O GitHub é amplamente utilizado por profissionais de tecnologia e é um

---

## 🔧 Configuração inicial do Git

```bash title='bash'

# Definir o nome do usuário
git config --global user.name "Seu Nome"

# Definir o e-mail do usuário
git config --global user.email "seu@email.com"

# Verificar as configurações atuais
git config --list
```

---

## 🚀 Início do Projeto

### Duas formas de começar:
1️⃣ Inicializar localmente e depois enviar para o GitHub  
2️⃣ Criar o repositório no GitHub e clonar para seu computador

```bash title='bash'

# Inicializar um repositório Git local
git init

# Adicionar a URL do repositório remoto
git remote add origin URL-DO-SEU-REPOSITÓRIO
```

```bash title='bash'

# Clonar um repositório do GitHub
git clone <URL-do-repositório>
```

---

## 📌 **HACK** - Criando uma GitIgnore para Python


```bash title='bash'
curl -o .gitignore https://www.toptal.com/developers/gitignore/api/python,visualstudiocode,pycharm+all
```

---
## 📄 Gerenciamento de Arquivos

```bash title='bash'

# Verificar o status dos arquivos
git status

# Adicionar todos os arquivos ao controle de versão
git add .

# Adicionar um arquivo específico
git add nome_do_arquivo

# Comentar alterações realizadas
git commit -m "Comentário explicativo"

# Adicionar e comentar de uma vez (para arquivos já versionados)
git commit -am "Comentário"
```

---

## 📜 Histórico e Diferenças

```bash title='bash'

# Ver histórico de commits
git log

# Visualizar o histórico em forma resumida e gráfica
git log --oneline --graph --all

# Ver diferenças entre arquivos
git diff
```

```bash title='bash'

# Restaurar estado anterior de um arquivo
git restore nome_do_arquivo

# Voltar para um commit específico
git reset --hard <hash-do-commit>
```

---

## 🌿 Branches

> Um *branch* é uma ramificação do código, usada para desenvolver funcionalidades sem afetar o código principal.

```bash title='bash'

# Ver todas as branches
git branch

# Criar nova branch
git branch nome-da-branch

# Mudar para uma branch
git checkout nome-da-branch

# Excluir uma branch
git branch -d nome-da-branch

# Fazer merge entre branches
git merge nome-da-branch
```

⚠️ Atenção: verifique se não há conflitos antes de fazer merge.

---

## 🔄 Atualizar o Repositório Remoto

```bash title='bash'

# Verificar status dos arquivos
git status

# Adicionar alterações
git add .

# Comentar alterações
git commit -m "Comentário"

# Enviar para o repositório remoto
git push origin nome-da-branch
# ou
git push -u
```

```bash title='bash'

# Atualizar alterações feitas remotamente
git pull origin nome-da-branch
# ou
git pull
```

---

## 🧑‍💻 Abrir o repositório no editor

```bash title='bash'

code .
```

---

## 🐧 GitHub no Linux

```bash title='bash'

# Atualizar o repositório local
sudo apt-get update

# Instalar o Git
sudo apt-get install git
```

Mesmos comandos para definir nome e e-mail:

```bash title='bash'

git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"
```

Ver dados configurados:

```bash title='bash'

cat .gitconfig
```

---

## 🍴 Fork

O **fork** é como uma cópia de um repositório para seu perfil, permitindo modificar sem alterar o projeto original.  
Você pode contribuir com o projeto original via *pull request*.

---

## 💼 GitHub como Currículo

O GitHub pode funcionar como um **portfólio profissional**. Mantenha-o organizado e bem estruturado.

---

## 📋 README

Um bom projeto no GitHub deve ter um arquivo `README.md`, que explica:

- O que é o projeto
- Como utilizar
- Como contribuir

### Dicas para um bom README:

- Use **Markdown**
- Adicione GIFs, imagens, links e listas
- Use [Shields.io](https://shields.io) para criar badges como:
  - Linguagens usadas
  - Tamanho do repositório
  - Status do build
  - Contato ou redes sociais

---

## 📌 Projeto Kanban

No GitHub, é possível utilizar a aba de **Projects**, baseada na metodologia **Kanban**, com colunas como:

- 📋 A Fazer
- 🔄 Em Progresso
- ✅ Concluído

Ajuda a acompanhar o progresso do projeto de forma visual e organizada.

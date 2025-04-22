
> **Essa página terá apenas uma introdução da estilização, porém, caso queira aprofundar mais, entre na documentação oficial do MkDocs, para mais informações:** [MkDocs-Material-Customization](https://squidfunk.github.io/mkdocs-material/customization/)  

## 🎨 Estilizando seu Projeto com MkDocs Material

O tema **MkDocs Material** já oferece um visual moderno por padrão, mas você pode deixar o site com a sua cara! Veja algumas formas de personalizar o visual do seu projeto:

---

### 🧩 1. Personalize as Cores

Você pode alterar as cores primárias e de destaque direto no seu `mkdocs.yml`:

```yaml title='yaml'

theme:
  name: material
  palette:
    scheme: default
    primary: indigo
    accent: pink
```

> 💡 Você pode trocar por cores como: `red`, `blue`, `green`, `purple`, `teal`, `amber`, entre outras!

---

### 🌙 2. Modo Escuro/Claro Automático

Ative o suporte a temas claro/escuro de acordo com as preferências do navegador:

```yaml title='yaml'

theme:
  name: material
  palette:
    - scheme: default
      primary: blue
      accent: light blue
      toggle:
        icon: material/lightbulb-outline
        name: Modo claro
    - scheme: slate
      primary: blue
      accent: light blue
      toggle:
        icon: material/lightbulb
        name: Modo escuro
```

---

### 🖼️ 3. Adicione um Logo e Ícone

Você pode adicionar um logotipo para a barra superior e um ícone para a aba do navegador:

```yaml title='yaml'

theme:
  name: material
  logo: assets/img/logo.png
  favicon: assets/img/favicon.ico
```

Crie a pasta `assets/img` dentro da pasta raiz do projeto e coloque suas imagens lá.

---

### 📝 4. Tipografia e Estilo

Você também pode mudar a fonte ou utilizar classes CSS personalizadas. Para isso:

1. Crie um arquivo CSS, por exemplo: `docs/styles/custom.css`
2. Adicione seu estilo:
```css
h1 {
  color: #4A90E2;
  font-family: 'Arial', sans-serif;
}
```
3. Referencie no `mkdocs.yml`:
```yaml title='yaml'

extra_css:
  - styles/custom.css
```

---

### 🧭 5. Outras Customizações Legais

- **Navbar fixa**:  
```yaml title='yaml'

theme:
  features:
    - navigation.top
```

- **Rodapé customizado**:  
```yaml title='yaml'

extra:
  social:
    - icon: fontawesome/brands/github
      link: https://github.com/seuusuario
    - icon: fontawesome/brands/linkedin
      link: https://linkedin.com/in/seuusuario
```

---

Com essas opções, seu site pode ficar único e profissional!  
Quer deixar ainda mais visual? Dá pra adicionar animações, grids e muito mais com HTML/CSS direto nos seus arquivos `.md`.

> ⚠️ Dica: vá testando cada alteração com `mkdocs serve` para ver o resultado em tempo real!

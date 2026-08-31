# Meu Blog com Hugo + PaperMod

Guia para criar seu próprio blog estático usando [Hugo](https://gohugo.io/) com o tema [PaperMod](https://themes.gohugo.io/themes/hugo-papermod/).

## Pré-requisitos

- [Hugo](https://gohugo.io/installation/) (extended, `>= 0.112.4`)
- [Git](https://git-scm.com/)

## 1. Criar um novo site

```bash
hugo new site meu-blog
cd meu-blog
```

## 2. Instalar o tema PaperMod

Como submódulo git (recomendado):

```bash
git init
git submodule add https://github.com/adityatelange/hugo-PaperMod themes/PaperMod
```

> Alternativa: baixe o tema e extraia o `.zip` em `themes/PaperMod`.

## 3. Configurar o tema

Adicione ao seu `hugo.yaml`:

```yaml
theme: PaperMod
```

Crie os arquivos básicos para o tema funcionar:

```bash
hugo new content/posts/meu-primeiro-post.md
hugo new content/archives/_index.md
hugo new content/search.md
```

## 4. Rodar localmente

```bash
hugo server -D
```

Acesse `http://localhost:1313/` no navegador. Use `-D` para incluir posts em rascunho (`draft = true`).

## 5. Publicar em um post

```bash
hugo new posts/meu-primeiro-post.md
```

No arquivo criado em `content/posts/`, altere `draft = true` para `draft = false` e adicione o conteúdo.

## 6. Build do site estático

```bash
hugo --gc --minify
```

Os arquivos finais serão gerados na pasta `public/`.

## Próximos passos

- Configure `baseURL`, `title`, menus e perfil do autor no `hugo.yaml`
- Opções de deploy: [GitHub Pages](https://gohugo.io/hosting-and-deployment/hosting-on-github/), [Netlify](https://gohugo.io/hosting-and-deployment/hosting-on-netlify/), [Cloudflare Pages](https://gohugo.io/hosting-and-deployment/hosting-on-cloudflare-pages/), etc.
- Veja a documentação completa em [PaperMod | Hugo Themes](https://themes.gohugo.io/themes/hugo-papermod/) e em [adityatelange/hugo-PaperMod](https://github.com/adityatelange/hugo-PaperMod).

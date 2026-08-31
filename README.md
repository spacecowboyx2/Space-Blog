# Palagi Blog

Um blog pessoal criado com [Hugo](https://gohugo.io/) usando o tema [PaperMod](https://github.com/adityatelange/hugo-PaperMod). Escrito por Pedro (Space/Palagi) — uma mistura de autodesenvolvimento, reflexões pessoais, hobbies e um pouco de tudo.

🔗 **[Acesse o blog](https://pedrodiashm.github.io/My-Blog/)**

---

## Tecnologias

| Ferramenta | Uso |
|---|---|
| Hugo | Gerador de sites estáticos |
| PaperMod | Tema |
| GitHub Actions | CI/CD |
| GitHub Pages | Hospedagem |

## Estrutura

```
├── .github/workflows/hugo.yaml   # Pipeline de deploy
├── archetypes/default.md          # Template padrão para posts
├── content/
│   ├── archives/_index.md         # Página de arquivos
│   └── posts/                     # Artigos do blog
├── hugo.yaml                      # Configuração principal
├── static/images/                 # Imagens estáticas
└── themes/PaperMod/               # Tema (vendored)
```

## Como rodar localmente

### Pré-requisitos

- [Hugo](https://gohugo.io/installation/) (>= 0.112.4)

### Instalação e execução

```bash
git clone https://github.com/pedrodiashm/My-Blog.git
cd My-Blog
hugo server
```

O site estará disponível em `http://localhost:1313/My-Blog/`.

## Deploy

O deploy é automático via **GitHub Actions**. Ao fazer push na branch `main`, o workflow:

1. Instala Hugo (v0.130.0 extended) e Dart Sass
2. Builda o site com `hugo --gc --minify`
3. Faz deploy no **GitHub Pages**

Também é possível disparar o deploy manualmente via `workflow_dispatch`.

## Criando um novo post

```bash
hugo new posts/nome-do-post.md
```

O arquivo será criado com `draft = true`. Altere para `false` e publique.

## Conteúdo do blog

Posts escritos em **português** e **inglês** sobre:

- Autodesenvolvimento e hábitos
- Reflexões pessoais
- Boxing e astronomia
- Escrita criativa


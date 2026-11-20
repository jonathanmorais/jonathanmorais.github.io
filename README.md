# Blog

Blog minimalista em Jekyll para GitHub Pages.

## Publicar

1. Edite `_config.yml` (título, nome, `url`, `baseurl` e links do rodapé).
2. Crie um repositório no GitHub:
   - `SEU_USUARIO.github.io`: o site fica em `https://SEU_USUARIO.github.io/` (`baseurl: ""`)
   - qualquer outro nome, ex. `blog`: o site fica em `https://SEU_USUARIO.github.io/blog/` (`baseurl: "/blog"`)
3. Envie o código:
   ```sh
   git add . && git commit -m "Primeiro commit"
   git remote add origin git@github.com:SEU_USUARIO/NOME_DO_REPO.git
   git push -u origin main
   ```
4. No GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch → `main` / `(root)`**.

Em um ou dois minutos o site está no ar.

## Novo post

Crie `_posts/AAAA-MM-DD-titulo.md`:

```markdown
---
layout: post
title: Meu post
subtitle: Opcional
---

Texto em Markdown...
```

Imagens: coloque em `assets/img/` e use `![descrição](/assets/img/foto.png)` (com `baseurl`, use `{{ '/assets/img/foto.png' | relative_url }}`).

## Rodar localmente (opcional)

Precisa de Ruby: `bundle install && bundle exec jekyll serve`, depois abra http://localhost:4000.

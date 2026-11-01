# CFF — Conscience Fast Forward

Blog pessoal de César Ciuffo, feito com [Quarto](https://quarto.org) e publicado no GitHub Pages:
**https://ciuffciuff.github.io/ciuffo_blog/**

## Como publicar um novo texto

1. Escolha a seção (pasta): `pesquisa`, `gestao`, `estrategia`, `dados-ia`, `internacional`, `historia` ou `cronicas`.
2. Dentro dela, crie uma pasta com data e nome curto, sem acentos: `gestao/2026-11-15-cultura-de-dados/`.
3. Copie o arquivo `_modelo-post.qmd` para essa pasta com o nome `index.qmd` e escreva.
4. Veja como ficou no seu computador: no Terminal do RStudio, `quarto preview`.
5. Envie para o GitHub (no RStudio: aba **Git** → *Commit* → *Push*).
   Em 2 a 3 minutos o site é atualizado sozinho.

## Estrutura

| Arquivo / pasta | Para que serve |
|---|---|
| `_quarto.yml` | configurações: título, menu, links, tema |
| `estilo.scss` | cores e fontes (paleta azul ApexBrasil + âmbar) |
| `index.qmd` | página inicial |
| `about.qmd` | página "Sobre" |
| `publicacoes.qmd` | lista de artigos publicados |
| `<seção>/index.qmd` | página de listagem de cada seção |
| `<seção>/_metadata.yml` | autor e capa padrão dos posts da seção |
| `imagens/` | logo, favicon e capas das seções |
| `_freeze/` | resultados já calculados dos códigos R (não apague) |
| `.github/workflows/publicar.yml` | publicação automática |

## Dica sobre código R

Se um post usar pacotes além do R básico (ex.: `ggplot2`), rode `quarto render` no seu
computador antes do *commit* e envie também a pasta `_freeze/`. Assim o GitHub não precisa
instalar esses pacotes para publicar.

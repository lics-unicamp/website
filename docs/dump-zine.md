# DUMP Zine

Seção de artigos técnicos da LICS (`/<idioma>/dump-zine/`), com visual próprio de terminal e separada do tema principal.

## Arquivos

| Arquivo | Função |
|---|---|
| `themes/org/layouts/dump-zine/baseof.html` | Base da zine: meta tags, OpenGraph, `hreflang`, fonte Fira Code e CSS próprio (sem Bootstrap). |
| `themes/org/layouts/dump-zine/list.html` | Capa: logo, apresentação e índice agrupado por edição. |
| `themes/org/layouts/dump-zine/single.html` | Artigo: autor com foto e link para o perfil, sumário automático, navegação Anterior/Próximo. |
| `themes/org/layouts/_partials/dump-zine/` | Logo ASCII, barra superior (home, capa, idioma), rodapé e nome do autor. |
| `themes/org/assets/zine/zine.css` | Estilos da zine. Fica fora de `assets/css/` para não entrar no CSS do site principal. |
| `archetypes/dump-zine.md` | Modelo de artigo novo. |

Os textos da interface estão em `themes/org/i18n/*.yaml` (chaves `dump-zine-*`). O botão da home usa `home-s1-nav5` e o menu fica em `config/_default/menus.*.yaml`.

## Novo artigo

```bash
hugo new content/pt-br/dump-zine/meu-artigo.md
hugo new content/en-us/dump-zine/meu-artigo.md
```

Preencha o front matter:

| Campo | Uso |
|---|---|
| `title` | Estilo da zine: `0x0A_Titulo_do_Artigo`. |
| `description` | Uma frase; vai para o preview em redes sociais. |
| `author` | Slug do membro (nome do arquivo em `content/<idioma>/membros/`). Mostra foto e link para o perfil. Texto livre também funciona, sem link. |
| `edition` | Edição, ex.: `0x4`. A capa agrupa os artigos por esse campo. |
| `weight` | Ordem do artigo; define também Anterior/Próximo. |
| `translationKey` | Igual nas duas versões, para ligar PT e EN na troca de idioma. |
| `draft` | Começa `true`; remova para publicar. |

Estrutura do texto: `## 0 - Introdução` → código → `## 1 - <tema>` → código → `## 2 - Conclusão`. O sumário é gerado a partir dos títulos `##`, então não precisa escrever à mão. Legendas de código vão em itálico logo abaixo do bloco (`_Figura 1. ..._`).

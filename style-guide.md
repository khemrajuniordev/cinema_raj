# Guia de estilos — Cinemas Raj

Este guia explica onde ficam os estilos do projeto e como fazer mudanças sem
alterar o visual das outras páginas.

## Qual arquivo CSS devo editar?

| Arquivo | Página que usa o arquivo | O que contém |
|---|---|---|
| `style.css` | `index.html` | Página inicial, catálogo, programação e modais dos filmes |
| `compra.css` | `comprar-sessao.html`, `comprar-assentos.html`, `comprar-resumo.html` e `comprar-confirmacao.html` | Etapas do fluxo de compra |
| `cinema.css` | `cinema.html` | Uma página de demonstração independente chamada LUMIÈRE |

Cada HTML carrega seu CSS com uma linha no `<head>`. Por exemplo:

```html
<link rel="stylesheet" href="style.css">
```

Edite o arquivo CSS já ligado à página. Evite carregar dois desses arquivos no
mesmo HTML: eles têm classes e variáveis com nomes iguais, como `.nav`, `.btn`
e `--bg`, mas com visuais diferentes.

## Organização dos arquivos

Os três arquivos têm seções separadas por comentários. Em `style.css`, a ordem
geral é:

1. Fonte, cores e configurações gerais.
2. Navegação e botões.
3. Destaque principal (hero), faixa de gêneros e seções.
4. Filtros, cards, programação e rodapé.
5. Janelas de detalhes e ajustes para telas menores.

Em `compra.css`, as regras seguem o fluxo da compra: navegação, etapas,
sessões, assentos, pagamento e confirmação. `cinema.css` tem os estilos da
página de demonstração LUMIÈRE.

## Cores e variáveis

As variáveis ficam no bloco `:root` no começo de cada CSS. Elas permitem mudar
uma cor usada em vários componentes de uma vez.

| Variável | Uso em `style.css` e `compra.css` | Valor |
|---|---|---|
| `--bg` | Fundo escuro da página | `#0a0a0c` |
| `--surface` | Fundo discreto de cards e controles | `rgba(255,255,255,.04)` |
| `--stroke` | Bordas suaves | `rgba(255,255,255,.10)` |
| `--stroke-2` | Bordas mais visíveis | `rgba(255,255,255,.18)` |
| `--text` | Texto principal | `#f4f4f7` |
| `--muted` | Texto secundário | `#9aa0ad` |
| `--gold` | Destaques e botões principais | `#f5c518` |
| `--rose` | Alertas e últimas sessões | `#ff3d71` |
| `--radius` | Arredondamento padrão | `18px` |
| `--ease` | Curva das animações | `cubic-bezier(.22,1,.36,1)` |
| `--shadow` | Sombra de destaque | `0 30px 60px -20px rgba(0,0,0,.8)` |

`cinema.css` usa os mesmos nomes de variáveis com valores e cores adicionais
próprios. Por isso, não copie uma variável de um arquivo para outro sem
verificar o resultado nessa página.

## Como ler os nomes das classes

O projeto usa nomes que agrupam componentes:

- `.card` identifica um card de filme.
- `.card__body` identifica uma parte do card.
- `.btn--primary` identifica uma variação principal do botão.

Em geral, `__` indica uma parte do componente e `--` indica uma variação ou
estado. Para encontrar os estilos de um elemento, procure a classe usada no
HTML dentro do CSS correspondente àquela página.

## Recursos feitos só com CSS

Alguns controles dependem da estrutura do HTML. Se mudar os seletores, confira
também os elementos e a ordem deles no HTML:

- **Filtros do catálogo:** `style.css` usa radio buttons e seletores `:checked`
  para destacar o gênero escolhido e esconder cards que não correspondem.
- **Menu para celular:** um checkbox com `.nav-toggle` abre e fecha os links
  dentro da media query de 860px.
- **Detalhes dos filmes:** os modais usam `:target`; o link com `#id` abre o
  modal correspondente.
- **Assentos e pagamento:** `compra.css` usa radio buttons e estados
  `:checked` para mostrar assentos selecionados e o painel de pagamento.
- **Etapas de compra:** os painéis de sessão usam `:target` para mostrar o
  conteúdo ligado ao fragmento da URL.

## Responsividade e acessibilidade

`style.css` adapta a grade de filmes para três colunas até 1000px, duas
colunas até 680px e reorganiza o destaque, menu e modal até 860px. A
programação também tem ajustes até 700px.

`compra.css` reduz o espaço do indicador de etapas até 560px. Os estilos
também respeitam a preferência do sistema por movimento reduzido, reduzindo
animações e transições.

Na página inicial, o foco do teclado é destacado em links, botões, filtros e
controles. Preserve as regras `:focus-visible` ao alterar esses componentes.

## Dicas para fazer uma mudança

1. Identifique qual HTML mostra o elemento.
2. Confira qual arquivo CSS esse HTML carrega.
3. Procure a classe do elemento nesse arquivo.
4. Altere uma propriedade por vez e atualize a página no navegador.
5. Confira também a versão para celular e os estados de hover, seleção e foco.

As fontes Inter e Playfair Display são carregadas do Google Fonts por meio de
`@import`. Sem conexão, o navegador usa a fonte alternativa definida em `font-family`.

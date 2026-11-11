# Cinemas Raj

Projeto desenvolvido como parte do **Bootcamp 1000Devs**: uma plataforma de
cinema pensada para oferecer uma experiência simples e organizada. É possível
consultar filmes em cartaz, verificar horários, escolher uma sessão e percorrer
as etapas de compra de ingressos.

O projeto foi uma oportunidade para praticar HTML, CSS, responsividade e
construção de interfaces inspiradas em desafios reais do mercado. Também
explora conceitos de experiência do usuário (UX), organização de informações e
fluxo de navegação.

## O que foi praticado

- HTML semântico.
- CSS responsivo.
- Estruturação de interfaces modernas.
- Experiência do usuário (UX).
- Organização e exibição de informações.
- Fluxo de navegação e conversão.
- Boas práticas de desenvolvimento Front-End.

## Funcionalidades

- Catálogo de filmes com filtros por gênero.
- Programação de sessões.
- Janelas com detalhes dos filmes.
- Fluxo de compra demonstrativo: escolha da sessão, assentos, forma de
  pagamento e confirmação.
- Página extra de demonstração visual LUMIÈRE.

## Tecnologias

- HTML5
- CSS3

O projeto não usa frameworks, bibliotecas JavaScript ou processo de build.
Algumas interações, como filtros, modais e seleção de assentos, são feitas
diretamente com CSS.

## Como abrir

1. Abra a pasta do projeto no VS Code.
2. Abra `index.html` no navegador ou use uma extensão como Live Server.
3. Navegue pelo catálogo e selecione **Comprar** para percorrer o fluxo
   demonstrativo.

Também é possível iniciar um servidor local a partir desta pasta:

```bash
python -m http.server 8000
```

Depois, acesse <http://localhost:8000>.

## Estrutura do projeto

| Arquivo ou pasta | Descrição |
|---|---|
| `index.html` | Página inicial, catálogo e programação |
| `comprar-sessao.html` | Escolha do filme e da sessão |
| `comprar-assentos.html` | Seleção de assentos |
| `comprar-resumo.html` | Resumo do pedido e opções de pagamento |
| `comprar-confirmacao.html` | Tela de confirmação demonstrativa |
| `cinema.html` | Página de demonstração visual LUMIÈRE |
| `style.css` | Estilos da página inicial |
| `compra.css` | Estilos das páginas do fluxo de compra |
| `cinema.css` | Estilos da página LUMIÈRE |
| `img/` | Imagens dos filmes e pôsteres |
| `style-guide.md` | Guia para entender e editar os estilos |

Cada página HTML carrega o arquivo CSS correspondente no `<head>`. Consulte
[`style-guide.md`](./style-guide.md) antes de alterar os estilos.

## Observação sobre pagamentos

Este é um projeto de interface para fins demonstrativos. As opções de
pagamento, os dados dos pedidos e a confirmação são exemplos fixos: nenhum
dado é enviado, armazenado ou processado e não há integração com serviços de
pagamento.

As fontes Inter e Playfair Display são carregadas do Google Fonts; para
visualizá-las, é necessário ter conexão com a internet. Sem conexão, o
navegador usa fontes alternativas.

## Equipe

- Devanngelles Frazão
- Artur Soares
- Jaciele Freitas
- Mike Vieira
- Alexandre Santos
- Matheus Dantas
- Natalia Caetano da Silva

## Bootcamp

**1000Devs**, com **Johnson & Johnson** e **Hospital Israelita Albert Einstein**.

## Tags

`#1000Devs` `#Frontend` `#DesenvolvimentoWeb` `#HTML` `#CSS` `#Programação`
`#TechCareer` `#Portfolio` `#AprendizadoContínuo` `#DevEmFormação`

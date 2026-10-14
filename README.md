# Portfólio · Danielli Arçari

Portfólio profissional construído sob medida, com estética premium inspirada em
Linear, Vercel e Raycast. Foco em maturidade visual, hierarquia tipográfica
forte e UX fluida.

---

## Stack

- **HTML5** semântico
- **CSS3** com custom properties (design tokens)
- **JavaScript vanilla** (sem framework, sem build step)
- **Google Fonts**, Inter, Instrument Serif, JetBrains Mono
- **SVG inline** para os gráficos e thumbnails, mais prints reais dos dashboards em `img/`

Zero build step, zero dependências. Abre direto no navegador ou faz deploy
estático em qualquer lugar (Vercel, Netlify, GitHub Pages, Cloudflare Pages).

---

## Estrutura de pastas

```
portfolio/
├── index.html                  ← Home (Hero · Sobre · Stack · Projetos · Trajetória · Contato)
│
├── projetos/                   ← 7 páginas de case (uma por projeto)
│   ├── divida-ativa-pgfn.html  ← 01 · Dívida ativa da União (Databricks, 45,5 mi de linhas)
│   ├── imdb-filmes.html        ← 02 · Reputação x retorno financeiro no cinema
│   ├── divvy-cyclistic.html    ← 03 · Bicicletas compartilhadas (Google Data Analytics)
│   ├── telecomx.html           ← 04 · Churn da Telecom X
│   ├── sqlalchemy.html         ← 05 · CSV para banco SQLite com SQLAlchemy
│   ├── populacao-prisional.html← 06 · Sistema prisional de MG (dados abertos)
│   └── bd-faculdade.html       ← 07 · Modelagem relacional em MySQL
│
├── img/                        ← prints reais dos dashboards e gráficos dos projetos
│
├── css/
│   ├── tokens.css              ← Design system (cores, tipografia, espaçamento, motion)
│   ├── base.css                ← Reset, defaults, background ambient, accessibility
│   ├── components.css          ← Nav, Buttons, Tags, Cards, Footer (primitivas)
│   ├── home.css                ← Estilos específicos da home (hero, marquee, stack, projects)
│   └── project.css             ← Estilos específicos das páginas de case (TOC, viz, stats)
│
├── js/
│   └── main.js                 ← IntersectionObserver, spotlight cursor, scrollspy, nav state
│
└── README.md                   ← Este arquivo
```


### Acessibilidade

- HTML semântico (`<main>`, `<nav>`, `<article>`, `<aside>`, `<section>`)
- Headings com hierarquia correta (h1 único por página, h2/h3 aninhados)
- `aria-label` em ícones e links sem texto
- Focus-visible com outline de 2px (não removido)
- Contraste WCAG AA em todos os textos
- Imagens decorativas com `aria-hidden`
- Scroll-padding-top para anchor jumps respeitarem o nav fixo
- Suporte a `prefers-reduced-motion`


## Performance

- **Sem imagens raster**, todos os gráficos são SVG inline
- **Sem build, sem JS frameworks**, tempo de carregamento mínimo
- **Fontes via Google Fonts** com `preconnect` para minimizar handshake
- **CSS modular**, só carrega o que cada página precisa
- **Lazy loading natural**, IntersectionObserver evita animações fora da tela

Espera-se Lighthouse 95+ em todas as métricas (Performance, Accessibility,
Best Practices, SEO) com deploy estático em Vercel/Netlify.

---

© 2026 Danielli Arçari · axiadmc@gmail.com

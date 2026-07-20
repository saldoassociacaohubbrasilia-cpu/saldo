# 📊 Saldo+ — Dashboard de Indicadores

Dashboard interativo em HTML, desenvolvido para consolidar e apresentar os principais indicadores de acompanhamento e impacto do programa **Saldo+** (trilha de educação financeira gamificada para estudantes do ensino médio da rede pública do Distrito Federal), comparando os resultados do **Piloto** com o **Semestre Atual (2026)**.

## Sobre o projeto

O Saldo+ é implementado em escolas públicas do Distrito Federal através da plataforma Ludos Pro. Este dashboard reúne, em uma única página, os indicadores operacionais (inscrição, ativação, conclusão, retenção), a distribuição por escola/turma e os resultados de impacto social (ITF — Índice de Transformação Financeira, mudança de comportamento financeiro, intenção de uso do benefício Pé-de-Meia).

Todo o conteúdo é estático (sem backend) e os dados dos gráficos estão embutidos diretamente no HTML/JS — ideal para publicar como página estática (ex: GitHub Pages) ou compartilhar como arquivo único.

## Abas do dashboard

| Aba | Conteúdo |
|---|---|
| **1 · Visão Geral** | KPIs principais (inscritos, ativação, conclusão, retenção), volume por etapa, estrutura institucional (regionais, escolas, turmas) e meta de inscritos x realizado |
| **2 · Taxas e Comparativos** | Painel de taxas-chave, comparativo Piloto x Semestre Atual, variação relativa e crescimento absoluto entre os dois ciclos |
| **3 · Escolas e Turmas** | Ranking de ativação por escola, perfil de inscritos por escola e engajamento das 33 turmas |
| **4 · Impacto Social** | Funil de engajamento, ITF por dimensão (T0 x T1), mudança de comportamento financeiro dos concluintes e intenção de uso do Pé-de-Meia |
| **· Avançado** | Funil de volume/conversão em SVG, mapa de calor interativo (Leaflet) e mapa estático exportável com a localização real das escolas no DF |

## Tecnologias utilizadas

- HTML5 + CSS3 (variáveis customizadas para o tema de cores)
- JavaScript puro (sem framework)
- [Chart.js 4.4.1](https://www.chartjs.org/) + [chartjs-plugin-datalabels](https://chartjs-plugin-datalabels.netlify.app/)
- [Leaflet.js](https://leafletjs.com/) + [Leaflet.heat](https://github.com/Leaflet/Leaflet.heat) (mapa de calor de engajamento)
- Google Fonts (Poppins)

Todas as bibliotecas são carregadas via CDN — é necessária conexão com a internet para o dashboard renderizar corretamente.

## Como usar

Não há build nem instalação. Basta abrir o arquivo `.html` diretamente no navegador:

```bash
git clone <url-do-repositorio>
cd <pasta-do-repositorio>
open index.html   # ou dê duplo clique no arquivo
```

Ou publique com o GitHub Pages: em **Settings → Pages**, selecione a branch e a pasta raiz — o dashboard fica acessível via URL pública.

## Funcionalidades

- **Exportação de imagens:** cada gráfico tem um botão "Baixar imagem (.png)" que gera uma versão em alta resolução, com título e legenda, pronta para apresentações e relatórios.
- **Mapa de calor interativo:** localização real das 8 escolas participantes no Distrito Federal, com tooltip de ativação e inscritos por escola.
- **Navegação por abas:** conteúdo organizado por tema, sem depender de um scroll único.

## Principais indicadores (Semestre Atual)

- **1.096** alunos inscritos
- **46,0%** taxa de ativação
- **15,3%** taxa de conclusão
- **33,3%** taxa de retenção
- **ITF geral:** 3,71 → 4,10 (T0 → T1)
- **94,1%** dos concluintes passaram a planejar gastos

## Notas sobre os dados

- **ITF (Índice de Transformação Financeira):** média das notas de conhecimento, comportamento e planejamento financeiro (escala 1–5). **T0** = antes do programa · **T1** = depois do programa.
- O cruzamento entre intenção de uso do Pé-de-Meia e taxa de conclusão usa subgrupos pequenos (1–2 concluintes por grupo) — deve ser lido como indício exploratório, não como conclusão estatisticamente robusta.

## Estrutura do repositório

```
.
├── index.html    # dashboard completo (HTML + CSS + JS em um único arquivo)
└── README.md
```

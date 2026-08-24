# COURSE PLAN — INEMA Command Language (formato-curso-v2)

Fonte-de-verdade ESTRUTURAL deste curso. Qualquer página gerada deve seguir este plano EXATAMENTE.
Conteúdo didático vem de `ref/INEMA_Command_Language_DSL_v0.1.md` (ler antes de escrever qualquer módulo).
Design system: skill `/work/.dsh/skills/formato-curso-v2/` — ler SKILL.md + references/MASTER_COMPLETO.md +
references/CHECKLIST_REVISAO.md + references/SVG-FUTURISTA.md + references/LEARN-LAYER.md.
Página canônica de referência (copiar padrões de markup daqui): `index.html` (landing).

## Identidade

| Campo | Valor |
|---|---|
| Nome do curso | INEMA Command Language |
| Logo/nav | 🧭 + "INEMA DSL" (link para `../../index.html` nos internos; `index.html` na landing) |
| Emoji do curso | 🧭 |
| courseId (`<meta name="inema-course">`) | `inema-dsl` |
| Idioma | pt-BR, tom direto/concreto, brasileiro, sem coachzinho |
| Tagline | "Uma linguagem operacional de 100 comandos para pesquisar, verificar, decidir e executar com IA." |

## Raiz e arquivos

```
curso-inema-dsl/               ← raiz (esta pasta)
├── index.html                 ← landing (pronta, usar como template)
├── COURSE_PLAN.md             ← este arquivo
├── ref/INEMA_Command_Language_DSL_v0.1.md   ← CONTEÚDO-FONTE
├── assets/learn.css           ← camada v2 (referenciar por caminho relativo)
├── assets/learn.js            ← camada v2 (referenciar por caminho relativo)
└── curso/
    ├── trilha1/index.html + modulo-1-1.html + modulo-1-2.html
    ├── trilha2/… (2-1, 2-2)
    ├── trilha3/… (3-1, 3-2)
    ├── trilha4/… (4-1, 4-2)
    ├── trilha5/… (5-1, 5-2)
    └── trilha6/… (6-1, 6-2)
```

Caminhos relativos OBRIGATÓRIOS:
- Em `index.html`: `assets/learn.css`, `assets/learn.js`, trilhas em `curso/trilhaN/index.html`.
- Em `curso/trilhaN/*.html`: assets em `../../assets/…`; landing em `../../index.html`; trilha irmã em `../trilhaM/index.html`.

## Trilhas, cores e níveis

| Trilha | Cor | Nome curto (nav) | Nome completo | Nível |
|---|---|---|---|---|
| T1 | Emerald | Fundamentos | Fundamentos da Linguagem | Básico |
| T2 | Blue | Pesquisa | Pesquisa & Análise | Intermediário |
| T3 | Purple | Crítica | Crítica & Decisão | Intermediário |
| T4 | Amber | Plano | Plano & Execução | Intermediário |
| T5 | Teal | Negócio | Negócio & IA aplicada | Avançado |
| T6 | Rose | Maestria | Comunicação & Maestria | Avançado |

Light-mode accent (Parte 2 do bloco CSS): emerald `#059669` rgba(5,150,105) · blue `#2563eb` rgba(37,99,235) ·
purple `#7c3aed` rgba(124,58,237) · amber texto `#92400e` + bg/border rgba(217,119,6) · teal `#0d9488` rgba(13,148,136) ·
rose `#9f1239` + bg/border rgba(225,29,72). Landing inclui TODAS as 6 (+ hover/group-hover).

SVG paleta (stroke primária / forte / fill caixa): emerald `#34d399`/`#10b981`/`#0e2018` · blue `#60a5fa`/`#3b82f6`/`#0e1622` ·
purple `#c084fc`/`#a855f7`/`#1a1230` · amber `#fbbf24`/`#f59e0b`/`#1f1604` · teal `#2dd4bf`/`#14b8a6`/`#0c1f1c` ·
rose `#fb7185`/`#f43f5e`/`#2a0f16`. Secundária sempre ciano `#38bdf8` (fill `#0e1b26`). IDs de defs prefixados `mXY-`.

## Módulos e tópicos (CONTAGENS FIXAS — manifesto depende delas)

### Trilha 1 — Fundamentos (Emerald)
**1.1 ⌨️ A linguagem /inema** (~65 min, 7 tópicos) `modulo-1-1.html`
1. O que é a INEMA Command Language · 2. A sintaxe-base: `/comando [parâmetros]` · 3. As 10 regras da linguagem ·
4. Composição em linha (`/truth /gaps /rank`) · 5. Encadear com `/chain` e controlar ordem ·
6. `/mode` e `/preset`: modo global e macros · 7. Runtime: registro, confiança, aceitação e fallback

**1.2 🔍 Verdade e verificação** (~75 min, 8 tópicos) `modulo-1-2.html`
1. `/truth` — separe fato de inferência · 2. `/verify` — confirme a afirmação · 3. `/evidence` — exija base probatória ·
4. `/sources` — priorize fontes por autoridade · 5. `/factcheck` — audite alegações uma a uma ·
6. `/confidence` — calibre a certeza · 7. `/uncertainty` + `/assumptions` — exponha o que não sabe ·
8. `/provenance` + `/freshness` — rastreie origem e validade

### Trilha 2 — Pesquisa & Análise (Blue)
**2.1 🛰️ Pesquisa e descoberta** (~75 min, 8 tópicos) `modulo-2-1.html`
1. `/research` — investigue de forma estruturada · 2. `/deepresearch` — vá a fundo com triangulação ·
3. `/scan` — varra amplo sem afundar · 4. `/discover` — encontre o não óbvio · 5. `/gaps` — descubra o que falta ·
6. `/trends` + `/signals` — separe modismo de mudança · 7. `/future` — construa cenários plausíveis ·
8. `/benchmark` + `/landscape` — mapeie referências e ecossistema

**2.2 🧪 Análise e síntese** (~75 min, 8 tópicos) `modulo-2-2.html`
1. `/analyze` — decomponha o problema · 2. `/synthesize` — integre sem apagar divergências ·
3. `/model` — crie o modelo mental · 4. `/framework` — construa a estrutura analítica ·
5. `/causes` — distinga correlação de causa · 6. `/secondorder` — veja os efeitos indiretos ·
7. `/tradeoffs` + `/constraints` — torne concessões visíveis · 8. `/leverage` + `/simplify` — alavanque e simplifique

### Trilha 3 — Crítica & Decisão (Purple)
**3.1 🥊 Red team e robustez** (~75 min, 8 tópicos) `modulo-3-1.html`
1. `/pushback` — conteste antes de recomendar · 2. `/challenge` — teste a tese · 3. `/redteam` — ataque como adversário ·
4. `/stress` + `/failure` — quebre o plano no teste · 5. `/premortem` — simule o fracasso ·
6. `/counterexample` — busque o contraexemplo · 7. `/bias` + `/blindspots` — audite vieses e pontos cegos ·
8. `/robust` — fortaleça sob incerteza

**3.2 🎯 Comparação e decisão** (~75 min, 8 tópicos) `modulo-3-2.html`
1. `/criteria` + `/weights` — defina como escolher · 2. `/rank` — ordene com justificativa ·
3. `/score` — pontue em escala explícita · 4. `/compare` — compare sem decidir cedo demais ·
5. `/decide` — decida com evidência e reversibilidade · 6. `/tradeoffmatrix` — cruze alternativas × critérios ·
7. `/pareto` — ache a fronteira dominante · 8. `/bet` + `/stop` — aposte sob incerteza e saiba parar

### Trilha 4 — Plano & Execução (Amber)
**4.1 📐 Planejamento e arquitetura** (~75 min, 8 tópicos) `modulo-4-1.html`
1. `/blueprint` — do objetivo ao plano executável · 2. `/roadmap` + `/milestones` — sequência verificável ·
3. `/dependencies` — mapeie pré-requisitos · 4. `/resources` — estime pessoas, dados e orçamento ·
5. `/architecture` — desenhe componentes e interfaces · 6. `/workflow` — processo em estados e fluxos ·
7. `/SOP` — procedimento padrão repetível · 8. `/checklist` + `/sequence` — verifique e otimize a ordem

**4.2 🚀 Execução e operações** (~75 min, 8 tópicos) `modulo-4-2.html`
1. `/execute` — converta plano em ação · 2. `/next` — a próxima melhor ação · 3. `/tasks` + `/owner` — decomponha e atribua ·
4. `/estimate` — estime sem falsa precisão · 5. `/priority` — priorize por impacto e risco ·
6. `/parallel` + `/automate` — paralelize e automatize · 7. `/monitor` — indicadores e limiares ·
8. `/review` — revise contra critérios e corrija

### Trilha 5 — Negócio & IA aplicada (Teal)
**5.1 💼 Produto, negócios e monetização** (~75 min, 8 tópicos) `modulo-5-1.html`
1. `/market` — analise mercado e dinâmica · 2. `/customer` — jobs, dores e desejos ·
3. `/segment` + `/position` — segmente e posicione · 4. `/offer` — construa a oferta ·
5. `/pricing` — preço e captura de valor · 6. `/monetize` — converta ativos em receita ·
7. `/businessmodel` + `/moat` — modele e defenda · 8. `/growth` — loops de crescimento

**5.2 🤖 Prototipagem e agentes de IA** (~75 min, 8 tópicos) `modulo-5-2.html`
1. `/prototype` + `/MVP` — o mínimo testável · 2. `/spec` — especifique requisitos e limites ·
3. `/agent` — projete o agente completo · 4. `/prompt` + `/tools` — prompt robusto e ferramentas ·
5. `/memory` — memória do sistema · 6. `/eval` — avalie antes de escalar ·
7. `/guardrails` — limites, fallback, escalonamento · 8. `/integrate` — integrações e sincronização

### Trilha 6 — Comunicação & Maestria (Rose)
**6.1 🗣️ Comunicação e aprendizado** (~70 min, 8 tópicos) `modulo-6-1.html`
1. `/brief` — síntese executiva em uma tela · 2. `/explain` — explique para o nível certo ·
3. `/teach` — ensine progressivamente · 4. `/translate` + `/rewrite` — intenção preservada ·
5. `/format` — transforme formato, não conteúdo · 6. `/audience` — adapte à audiência ·
7. Pipeline `/brief → /explain → /audience` · 8. Oficina: um email em 4 formatos

**6.2 🎛️ Meta-comandos e maestria** (~65 min, 7 tópicos) `modulo-6-2.html`
1. `/mode` — perfis globais de comportamento · 2. `/chain` — encadeamento com passagem de saída ·
3. `/preset` — pacotes oficiais de comandos · 4. As 5 receitas compostas do documento ·
5. Estrutura interna YAML de um comando · 6. Precedência e resolução de conflitos · 7. Roadmap v0.2

**Totais: 6 trilhas · 12 módulos · 94 tópicos · ~14h**

## MANIFESTO (idêntico em TODAS as páginas, no `<head>`)

```html
<script type="application/json" data-inema-manifest>
{"course":"inema-dsl","tracks":[
{"n":"1","title":"Fundamentos","modules":[{"id":"1-1","title":"A linguagem /inema","topics":7,"href":"curso/trilha1/modulo-1-1.html"},{"id":"1-2","title":"Verdade e verificação","topics":8,"href":"curso/trilha1/modulo-1-2.html"}]},
{"n":"2","title":"Pesquisa & Análise","modules":[{"id":"2-1","title":"Pesquisa e descoberta","topics":8,"href":"curso/trilha2/modulo-2-1.html"},{"id":"2-2","title":"Análise e síntese","topics":8,"href":"curso/trilha2/modulo-2-2.html"}]},
{"n":"3","title":"Crítica & Decisão","modules":[{"id":"3-1","title":"Red team e robustez","topics":8,"href":"curso/trilha3/modulo-3-1.html"},{"id":"3-2","title":"Comparação e decisão","topics":8,"href":"curso/trilha3/modulo-3-2.html"}]},
{"n":"4","title":"Plano & Execução","modules":[{"id":"4-1","title":"Planejamento e arquitetura","topics":8,"href":"curso/trilha4/modulo-4-1.html"},{"id":"4-2","title":"Execução e operações","topics":8,"href":"curso/trilha4/modulo-4-2.html"}]},
{"n":"5","title":"Negócio & IA aplicada","modules":[{"id":"5-1","title":"Produto, negócios e monetização","topics":8,"href":"curso/trilha5/modulo-5-1.html"},{"id":"5-2","title":"Prototipagem e agentes de IA","topics":8,"href":"curso/trilha5/modulo-5-2.html"}]},
{"n":"6","title":"Comunicação & Maestria","modules":[{"id":"6-1","title":"Comunicação e aprendizado","topics":8,"href":"curso/trilha6/modulo-6-1.html"},{"id":"6-2","title":"Meta-comandos e maestria","topics":7,"href":"curso/trilha6/modulo-6-2.html"}]}
]}
</script>
```

## Subtítulos PUNCHY (Mapa da trilha + cards)

1.1 "Uma gramática, cem superpoderes" · 1.2 "Fato nunca misturado com palpite"
2.1 "Do sinal fraco à descoberta" · 2.2 "Dez entradas, uma visão coerente"
3.1 "Ataque sua ideia primeiro" · 3.2 "Decidir é comparar sob incerteza"
4.1 "Objetivo vira plano executável" · 4.2 "Do plano à rotina operante"
5.1 "Dor real, oferta pagante" · 5.2 "Do protótipo ao agente avaliado"
6.1 "Contexto certo, audiência certa" · 6.2 "Cadeias que pensam por você"

## Contrato técnico de toda página (resumo — detalhes no MASTER)

1. `<html lang="pt-BR" class="dark">`; `<head>`: charset, viewport, title, `<meta name="inema-course" content="inema-dsl">`,
   **anti-FOUC inline PRIMEIRO** (snippet da landing, trocar só nada — é idêntico em todas), Tailwind CDN + config,
   Inter, **manifesto**, `<link rel="stylesheet"> learn.css relativo`, `<style>` com: CSS base + `.topic-explanation`,
   bloco light-mode COMPLETO (Partes 1-4 + acento(s) da página + `html:not(.dark) svg[role="img"]{filter:saturate(.82) brightness(.96)}`),
   bordas suavizadas dark (`border-dark-600` E `divide-dark-600` → `#374151`), `scroll-margin-top:88px` em alvos,
   keyframes `wf-pulse` sob `prefers-reduced-motion: no-preference`.
2. Body: `<a class="skip" href="#conteudo">` (classe .skip no CSS), nav sticky completo (logo | INEMA.CLUB sky - PRO amber/slate,
   6 botões de trilha com ativa colorida, mobile T1..T6, botão "Minha jornada" `data-inema-journey-open` + badge,
   trigger de aparência `data-inema-appearance-toggle="[data-inema-appearance]"` + painel `[data-inema-appearance]`
   (markup §3.7 do LEARN-LAYER), theme toggle sol/lua). `<main id="conteudo">`. Footer.
3. Fim do body: JS-núcleo v1 (toggleTopic, theme-toggle, openModal/closeModal quando houver modal),
   depois `<script src="…assets/learn.js"></script>`, depois `INEMA.init()`. NUNCA outra ordem.
4. Módulos: cada seção `<section id="topico-N" data-inema-topic="modulo-X-Y#topico-N">` com círculo GRANDE w-12,
   título h2 emoji, intro com parágrafos anotáveis (`data-inema-block="mXY-tN-pK"`), boxes variados,
   glossário-inline "Novo aqui?" para TODO termo técnico novo, botão marcar-lido (`data-inema-read-toggle aria-pressed`,
   `justify-start`, spans `.inema-ico-todo/.inema-ico-done/.inema-label-todo/.inema-label-done`),
   dúvida (`data-inema-doubt-toggle`) no header do tópico, wrapper externo `<article id="modulo-X-Y"
   data-inema-module="X-Y" data-inema-track="N">`, medidores (`data-inema-meter="modulo:X-Y"` barra + `trilha:N` + `curso`
   compactos), TOC sticky `data-inema-toc` + contador, ≥1 SVG futurista, ≥1 checagem leve (`data-inema-check` +
   `INEMA.registerCheck`), resumo final com checklist ✓ + próximo módulo + CTAs.
5. Index de trilha: hero SVG, header gradiente + 4 stats, **Mapa da trilha** (grid âncoras `#modulo-X-Y`,
   `justify-between` X.Y+duração, emoji+punchy, SEM círculo extra), cartões simples clicáveis (grid 2 cols `<a>` sem botões),
   h2 simples "Conteúdo detalhado", cards completos `id="modulo-X-Y"` com tópicos expansíveis
   (`<button onclick="toggleTopic(this)" aria-expanded aria-controls>`, número em círculo, 3 seções obrigatórias,
   painel com `id`), botões `justify-start` ("Ver em Modal" + "Ver Completo"), modais iframe por módulo
   (`role=dialog`-like padrão v1 + ESC), medidor `trilha:N`, navegação trilha anterior/próxima.
6. Erros críticos #1-#31: zero exceção. Botões `justify-start`; nunca `▶`; 3 seções por tópico;
   INEMA.CLUB `text-sky-400` + PRO ao lado; título de módulo `text-2xl`; profundidade 500-800 linhas/módulo com variedade
   (≥2 grids ✓/✗, ≥1 timeline, ≥2 tip boxes, code box copy-run com objetivo+bloco+verificação);
   ambar nunca texto em superfície clara; exemplos reais coláveis com `<isto você troca>` marcado.

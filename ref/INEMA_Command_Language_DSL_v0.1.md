# INEMA Command Language — DSL v0.1

## Propósito
Uma linguagem operacional curta para controlar como modelos e agentes de IA pesquisam, verificam, analisam, criticam, decidem, planejam, executam e comunicam.

## Sintaxe-base

```text
/comando [parâmetros opcionais]
/comando1 /comando2 /comando3
/chain(/research -> /truth -> /rank -> /decide)
```

### Regras da linguagem
1. Comandos são instruções declarativas, não códigos secretos do modelo.
2. A ordem importa quando houver cadeia explícita.
3. Um comando pode receber parâmetros: `/rank criteria=impact,cost,risk`.
4. Comandos podem ser compostos: `/truth /gaps /pushback /rank`.
5. Em conflito, vence a regra mais específica; depois, a mais recente.
6. `/preset` expande macros; `/chain` controla sequência; `/mode` define comportamento global.
7. O runtime deve registrar entradas, saídas, ferramentas usadas, confiança e falhas.
8. Comandos que exigem informação atual podem acionar pesquisa ou conectores.
9. A execução deve separar geração de verificação quando o risco for relevante.
10. Todo comando deve poder ter critérios de aceitação e fallback.

## 01 — Verdade e Verificação

| # | Comando | Função | Protocolo |
|---:|---|---|---|
| 1 | `/truth` | Separar fato, inferência, hipótese e desconhecido. | Verifica premissas; evita afirmar como fato o que não foi sustentado; informa confiança. |
| 2 | `/verify` | Confirmar uma afirmação específica. | Procura evidência suficiente para confirmar, corrigir ou rejeitar a afirmação. |
| 3 | `/evidence` | Exigir base probatória. | Mostra quais evidências sustentam cada conclusão importante e onde ainda faltam dados. |
| 4 | `/sources` | Priorizar fontes. | Identifica e organiza fontes por autoridade, atualidade, proximidade do fato e independência. |
| 5 | `/factcheck` | Auditar um conjunto de alegações. | Quebra o conteúdo em claims verificáveis e classifica cada um como confirmado, impreciso, falso, inconclusivo ou opinativo. |
| 6 | `/confidence` | Calibrar certeza. | Atribui nível de confiança às conclusões e explica quais fatores mais aumentariam ou reduziriam essa confiança. |
| 7 | `/uncertainty` | Mapear incertezas. | Expõe dados faltantes, variáveis desconhecidas e pontos onde mais de uma interpretação é plausível. |
| 8 | `/assumptions` | Tornar premissas explícitas. | Lista premissas usadas no raciocínio e marca quais são verificadas, razoáveis ou frágeis. |
| 9 | `/provenance` | Rastrear origem da informação. | Mostra de onde cada informação crítica veio e diferencia dado primário, secundário, inferido ou fornecido pelo usuário. |
| 10 | `/freshness` | Checar validade temporal. | Identifica o que pode ter mudado e exige atualização antes de usar dados sensíveis ao tempo. |

## 02 — Pesquisa e Descoberta

| # | Comando | Função | Protocolo |
|---:|---|---|---|
| 11 | `/research` | Investigar um tema de forma estruturada. | Define perguntas, coleta evidências, sintetiza achados e encerra com lacunas e próximos passos. |
| 12 | `/deepresearch` | Executar pesquisa aprofundada. | Amplia fontes, triangula evidências, compara interpretações e documenta conflitos relevantes. |
| 13 | `/scan` | Fazer varredura ampla. | Busca sinais, atores, soluções, movimentos e temas emergentes sem aprofundar prematuramente. |
| 14 | `/discover` | Encontrar oportunidades não óbvias. | Procura padrões, adjacências, combinações e espaços ainda pouco explorados. |
| 15 | `/gaps` | Descobrir o que está faltando. | Identifica perguntas ausentes, dados necessários, riscos, exceções e oportunidades ignoradas. |
| 16 | `/trends` | Detectar tendências. | Separa modismo, crescimento sustentado, sinal emergente e mudança estrutural. |
| 17 | `/signals` | Encontrar sinais fracos. | Procura indícios iniciais que possam antecipar mudanças importantes antes de virarem consenso. |
| 18 | `/future` | Explorar futuros plausíveis. | Constrói cenários plausíveis, gatilhos, indicadores antecedentes e implicações. |
| 19 | `/benchmark` | Comparar com referências. | Seleciona benchmarks relevantes e mede diferenças de desempenho, estratégia, produto ou processo. |
| 20 | `/landscape` | Mapear o ecossistema. | Organiza mercado, atores, categorias, tecnologias, concorrentes, parceiros e relações. |

## 03 — Análise e Síntese

| # | Comando | Função | Protocolo |
|---:|---|---|---|
| 21 | `/analyze` | Analisar um problema. | Decompõe o problema, identifica causas, relações, evidências e implicações. |
| 22 | `/synthesize` | Integrar múltiplas informações. | Combina materiais heterogêneos em uma visão coerente sem apagar divergências importantes. |
| 23 | `/model` | Criar um modelo mental. | Representa variáveis, relações, mecanismos, entradas, saídas e feedbacks. |
| 24 | `/framework` | Construir uma estrutura analítica. | Cria dimensões e categorias mutuamente úteis para organizar o problema. |
| 25 | `/causes` | Investigar causalidade. | Distingue correlação, causa provável, causa necessária, causa suficiente e fatores de confusão. |
| 26 | `/secondorder` | Analisar efeitos de segunda ordem. | Investiga consequências indiretas, atrasadas, sistêmicas e comportamentais. |
| 27 | `/tradeoffs` | Explicitar concessões. | Mostra ganhos, perdas e restrições inevitáveis entre alternativas. |
| 28 | `/constraints` | Mapear restrições. | Identifica limites técnicos, financeiros, humanos, legais, temporais e operacionais. |
| 29 | `/leverage` | Encontrar pontos de alavancagem. | Prioriza mudanças pequenas com potencial de produzir impacto desproporcional. |
| 30 | `/simplify` | Reduzir complexidade sem perder essência. | Remove detalhes dispensáveis e preserva decisões, mecanismos e riscos centrais. |

## 04 — Crítica, Red Team e Robustez

| # | Comando | Função | Protocolo |
|---:|---|---|---|
| 31 | `/pushback` | Contestar a proposta do usuário. | Tenta refutar a ideia antes de recomendar; mantém, modifica ou rejeita com justificativa. |
| 32 | `/challenge` | Testar uma tese. | Procura contraexemplos, condições de falha e explicações alternativas. |
| 33 | `/redteam` | Atacar adversarialmente. | Assume postura de adversário para encontrar vulnerabilidades, abusos, falhas e pontos cegos. |
| 34 | `/stress` | Submeter a estresse. | Testa o plano sob aumento de carga, queda de receita, atrasos, falta de pessoas e outros cenários extremos. |
| 35 | `/failure` | Imaginar como falharia. | Identifica modos de falha, causas, impacto, detecção e mitigação. |
| 36 | `/premortem` | Simular fracasso futuro. | Assume que o projeto fracassou e reconstrói as razões mais plausíveis. |
| 37 | `/counterexample` | Buscar caso que contradiga. | Tenta encontrar uma situação válida que derrube uma regra ou conclusão generalizada. |
| 38 | `/bias` | Auditar vieses. | Procura vieses cognitivos, de seleção, incentivo, confirmação, sobrevivência e mensuração. |
| 39 | `/blindspots` | Localizar pontos cegos. | Pergunta o que pessoas, dados ou perspectivas relevantes podem estar ausentes. |
| 40 | `/robust` | Fortalecer a solução. | Revisa a proposta para funcionar melhor diante de incerteza, falhas e mudanças de contexto. |

## 05 — Comparação e Decisão

| # | Comando | Função | Protocolo |
|---:|---|---|---|
| 41 | `/rank` | Ordenar alternativas. | Define critérios, pesos e evidências; entrega ranking com justificativa. |
| 42 | `/score` | Pontuar opções. | Cria escala explícita e atribui notas comparáveis a cada alternativa. |
| 43 | `/decide` | Tomar decisão recomendada. | Combina objetivos, evidências, riscos, reversibilidade e custo de oportunidade. |
| 44 | `/compare` | Comparar lado a lado. | Mostra diferenças relevantes sem forçar uma escolha prematura. |
| 45 | `/criteria` | Definir critérios de escolha. | Transforma preferências e objetivos em critérios mensuráveis ou observáveis. |
| 46 | `/weights` | Atribuir pesos. | Distribui importância relativa entre critérios e testa sensibilidade. |
| 47 | `/tradeoffmatrix` | Criar matriz de decisão. | Cruza alternativas e critérios para tornar perdas e ganhos visíveis. |
| 48 | `/pareto` | Encontrar soluções dominantes. | Identifica opções dominadas e a fronteira de melhores compromissos. |
| 49 | `/bet` | Escolher sob incerteza. | Formula a decisão como aposta: probabilidade, upside, downside, custo e aprendizado. |
| 50 | `/stop` | Definir condição de parada. | Estabelece quando continuar, pivotar, pausar ou abandonar uma iniciativa. |

## 06 — Planejamento e Arquitetura

| # | Comando | Função | Protocolo |
|---:|---|---|---|
| 51 | `/blueprint` | Transformar objetivo em plano executável. | Converte objetivo em etapas, dependências, recursos, responsáveis, métricas, riscos e próxima ação. |
| 52 | `/roadmap` | Construir sequência temporal. | Organiza horizontes, marcos, dependências e entregas ao longo do tempo. |
| 53 | `/milestones` | Definir marcos. | Cria pontos verificáveis de progresso com critérios claros de conclusão. |
| 54 | `/dependencies` | Mapear dependências. | Identifica pré-requisitos, bloqueios, ordem de execução e dependências externas. |
| 55 | `/resources` | Planejar recursos. | Estima pessoas, ferramentas, dados, orçamento, infraestrutura e conhecimento necessários. |
| 56 | `/architecture` | Desenhar arquitetura. | Define componentes, interfaces, fluxos, responsabilidades e decisões estruturais. |
| 57 | `/workflow` | Desenhar fluxo operacional. | Transforma o processo em estados, entradas, ações, decisões, saídas e exceções. |
| 58 | `/SOP` | Criar procedimento padrão. | Converte um processo recorrente em passos repetíveis, controles e critérios de qualidade. |
| 59 | `/checklist` | Gerar verificação operacional. | Cria itens objetivos para evitar omissões antes, durante ou depois da execução. |
| 60 | `/sequence` | Otimizar ordem de ações. | Encontra a menor sequência de passos que desbloqueia resultado ou aprendizado real. |

## 07 — Execução e Operações

| # | Comando | Função | Protocolo |
|---:|---|---|---|
| 61 | `/execute` | Converter plano em ações. | Começa pela próxima ação possível e produz artefatos ou instruções operacionais concretas. |
| 62 | `/next` | Determinar próxima melhor ação. | Escolhe o passo de maior valor esperado considerando bloqueios e reversibilidade. |
| 63 | `/tasks` | Decompor em tarefas. | Transforma objetivo em unidades pequenas, verificáveis e atribuíveis. |
| 64 | `/owner` | Definir responsabilidade. | Atribui dono, apoio, aprovador e dependências para cada ação. |
| 65 | `/estimate` | Estimar esforço. | Estima tempo, complexidade, custo e incerteza sem falsa precisão. |
| 66 | `/priority` | Priorizar trabalho. | Ordena tarefas por impacto, urgência, dependências, risco e esforço. |
| 67 | `/parallel` | Encontrar o que pode rodar em paralelo. | Separa atividades independentes das que exigem sequência. |
| 68 | `/automate` | Identificar automações. | Procura tarefas repetitivas, regras claras, gatilhos, APIs e pontos adequados para automação. |
| 69 | `/monitor` | Definir monitoramento. | Especifica indicadores, frequência, limiares e ações quando algo muda. |
| 70 | `/review` | Executar revisão operacional. | Compara resultado com critérios, registra desvios, aprendizados e correções. |

## 08 — Produto, Negócios e Monetização

| # | Comando | Função | Protocolo |
|---:|---|---|---|
| 71 | `/market` | Analisar mercado. | Avalia problema, demanda, segmentos, concorrência, dinâmica e barreiras. |
| 72 | `/customer` | Entender cliente. | Define jobs, dores, desejos, contexto, alternativas atuais e critérios de compra. |
| 73 | `/segment` | Segmentar público. | Cria segmentos úteis por necessidade, comportamento, valor ou contexto de uso. |
| 74 | `/position` | Definir posicionamento. | Clarifica para quem é, qual problema resolve, categoria, diferença e prova. |
| 75 | `/offer` | Construir oferta. | Organiza promessa, entregáveis, preço, prova, risco percebido e chamada à ação. |
| 76 | `/pricing` | Estruturar preço. | Compara modelos de captura de valor, disposição a pagar, unidade econômica e simplicidade comercial. |
| 77 | `/monetize` | Encontrar formas de monetização. | Converte ativos, audiência, dados, software, conhecimento ou distribuição em modelos de receita. |
| 78 | `/businessmodel` | Desenhar modelo de negócio. | Mapeia criação, entrega e captura de valor, custos, canais e vantagens. |
| 79 | `/moat` | Avaliar defensabilidade. | Analisa marca, dados, rede, distribuição, switching costs, escala, know-how e velocidade. |
| 80 | `/growth` | Desenhar crescimento. | Identifica loops, canais, gargalos, métricas, experimentos e mecanismos de retenção. |

## 09 — Produto Digital, IA e Prototipagem

| # | Comando | Função | Protocolo |
|---:|---|---|---|
| 81 | `/prototype` | Criar versão mínima testável. | Reduz a ideia ao menor artefato capaz de validar a hipótese crítica. |
| 82 | `/MVP` | Definir produto mínimo viável. | Escolhe o conjunto mínimo de capacidades que entrega valor e gera aprendizado real. |
| 83 | `/spec` | Especificar solução. | Define requisitos, interfaces, comportamento, limites, exceções e critérios de aceitação. |
| 84 | `/agent` | Projetar agente de IA. | Define objetivo, ferramentas, memória, regras, entradas, saídas, limites e avaliação. |
| 85 | `/prompt` | Projetar prompt robusto. | Especifica papel, objetivo, contexto, regras, ferramentas, formato e critérios de qualidade. |
| 86 | `/tools` | Selecionar ferramentas. | Mapeia tarefas para ferramentas e define quando usar, não usar ou escalar. |
| 87 | `/memory` | Projetar memória do sistema. | Separa memória de sessão, perfil, fatos persistentes, histórico e política de atualização. |
| 88 | `/eval` | Criar avaliação. | Define casos de teste, critérios, métricas, falhas críticas e limiar de aprovação. |
| 89 | `/guardrails` | Definir limites operacionais. | Cria regras de segurança, autorização, validação, fallback e escalonamento. |
| 90 | `/integrate` | Planejar integrações. | Mapeia sistemas, APIs, autenticação, dados, eventos, erros e sincronização. |

## 10 — Comunicação, Aprendizado e Meta-Comandos

| # | Comando | Função | Protocolo |
|---:|---|---|---|
| 91 | `/brief` | Produzir síntese executiva. | Entrega apenas contexto indispensável, decisão, evidências, riscos e próxima ação. |
| 92 | `/explain` | Explicar com clareza. | Adapta profundidade e vocabulário ao nível do público e usa exemplos quando melhoram compreensão. |
| 93 | `/teach` | Ensinar progressivamente. | Organiza conceito, intuição, exemplo, prática, erro comum e verificação de aprendizado. |
| 94 | `/translate` | Traduzir preservando intenção. | Mantém significado, tom, termos técnicos e adapta apenas o necessário ao idioma-alvo. |
| 95 | `/rewrite` | Reescrever para objetivo específico. | Preserva conteúdo essencial e otimiza clareza, tom, persuasão ou concisão. |
| 96 | `/format` | Transformar formato. | Converte a mesma informação para tabela, JSON, checklist, memo, roteiro ou outro formato solicitado. |
| 97 | `/audience` | Adaptar à audiência. | Ajusta linguagem, exemplos, profundidade, objeções e chamada à ação para o público definido. |
| 98 | `/mode` | Definir modo global de operação. | Ativa um perfil persistente de comportamento para a execução atual, como conservador, exploratório ou executivo. |
| 99 | `/chain` | Encadear comandos. | Executa comandos em ordem explícita, passando a saída relevante de um para o próximo. |
| 100 | `/preset` | Invocar pacote de comandos. | Expande um nome curto para uma cadeia predefinida de comandos com parâmetros. |

## Composição recomendada

```text
# Decisão confiável
/research /truth /gaps /pushback /rank /decide

# Construção de produto
/market /customer /gaps /offer /MVP /prototype /eval

# Arquitetura de agente
/agent /tools /memory /guardrails /eval /integrate

# Execução de projeto
/blueprint /dependencies /priority /parallel /execute /monitor /review

# Tese de negócio
/truth /market /pushback /businessmodel /moat /growth /bet
```

## Estrutura interna sugerida para cada comando

```yaml
name: /truth
family: verification
version: 0.1
purpose: separar fatos, inferências, hipóteses e desconhecidos
inputs: [query, context]
tools: [search:auto]
rules:
  - verify unstable claims
  - never present inference as verified fact
output_schema:
  - verified_facts
  - inferences
  - unknowns
  - confidence
acceptance:
  - critical claims are supported
fallback:
  - state what could not be verified
```

## Próxima versão sugerida
A v0.2 deve acrescentar aliases, tipos de parâmetros, schemas de saída, precedência formal, níveis de permissão, políticas de uso de ferramentas, presets oficiais e testes de conformidade para cada comando.
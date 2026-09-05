# FALHAS — curso-inema-dsl

| data | o que quebrou | menor correção | prompt \| infra |
|---|---|---|---|
| 2026-09-05 | Modo claro do curso inteiro: caixas com fundo `bg-dark-*/NN` (Copie e rode, stats, painéis) ficavam cinza-escuro com texto ilegível — bloco light-mode só mapeava `/95` | Regras `html:not(.dark) .bg-dark-900\/70…` para todas as variantes de opacidade usadas, nas 19 páginas | prompt |
| 2026-09-05 | Curso publicado em 24/08 com 6 dos 12 módulos faltando (trilha4 só index; trilha5/6 vazias) — 6 links em 404 a partir da landing, sem ninguém notar por 12 dias | Gerar os 6 módulos + 2 índices a partir do shell dos existentes; **proteção que faltou**: checagem de `href` local antes do push (todo link do manifesto precisa existir em disco) | prompt |

# Roadmap de implementação do MELLITUS

| Campo | Valor |
|---|---|
| **ID** | MEL-ROADMAP-002 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | ROADMAP |
| **Fase** | F0 — Governação e requisitos |
| **Estado** | EM_REVISAO |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | 64dede56ecd6d40d8dd1986b683e8b422719b24c7b2d99506fd9e15516b40001 |
| **Commit de referência (versão anterior)** | [fe362c320b4f167d829503d5f27b2c288803ab34](https://github.com/carlos-andrade/MELLITUS/commit/fe362c320b4f167d829503d5f27b2c288803ab34) |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Responsável de projeto — a formalizar |
| **Aprovador** | Pendente de baseline formal |
| **Origem** | Plano diretor e inventário atual do repositório |
| **Autoridade superior** | [GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA); [plano diretor](../docs/PLANO_DIRETOR.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | STATUS.md; docs/PLANO_DIRETOR.md; docs/REQUISITOS.md; docs/MATRIZ_RASTREABILIDADE.md |

## Estado factual de partida

Verificação da branch `main` em 2026-10-15: repositório contém documentação base e prompt de especialista em diabetes. Não foi verificado código da aplicação nem testes funcionais executados. Implementação funcional comprovada: 0%.

## Plano por fases

| Fase | Entregáveis | Critérios de saída | Estado atual |
|---|---|---|---|
| P0 — Baseline e governação | Inventário, requisitos, responsáveis, decisões, cabeçalhos/integridade | G0/G1 formalmente aceites | EM_CURSO |
| P1 — Evidência editorial | Catálogo de fontes e 2–3 artigos piloto revistos | Aprovação clínica editorial registada | PROPOSTO |
| P2 — Arquitetura e proteção | Stack, modelo de dados, ameaça, privacidade, arquitetura | G2 aceite por decisores competentes | PROPOSTO |
| P3 — Fundação técnica | Estrutura de código, configuração, testes básicos, CI | Build e testes reproduzíveis | PROPOSTO |
| P4 — MVP educativo | UI responsiva, conteúdo, pesquisa, fontes, fluxo editorial | Requisitos MVP testados e revisão de conteúdo | PROPOSTO |
| P5 — Segurança e qualidade | Testes, revisão, acessibilidade, privacidade, correções | Sem bloqueios críticos; evidências guardadas | PROPOSTO |
| P6 — Prontidão operacional | Ambientes, backup/restore, observabilidade, runbook | G4 aceite e restauração testada | BLOQUEADO_ATÉ_P5 |
| P7 — Piloto e lançamento | Piloto limitado, feedback, rollback, autorização | G5 e autorização explícita | BLOQUEADO_ATÉ_G4 |
| P8 — Registos pessoais | Requisitos próprios, modelo de dados de saúde, avaliação de impacto | Novo G1/G2; autorização de privacidade/clínica | BLOQUEADO |
| P9 — Integrações/IA clínica | Estudo de finalidade e classificação, evidência e regulação | Aprovação específica e validação independente | BLOQUEADO |

## Regras de avanço

- Não avançar uma fase pelo decurso do tempo ou por adicionar ficheiros.
- Usar `PASS`, `WARN`, `FAIL`, `UNKNOWN` nos controlos de validação.
- Decisões críticas devem ter responsável, aprovador e evidência.
- As etapas P8/P9 ficam fora do MVP e não podem ser ativadas por inferência.
- Prazo e orçamento serão estabelecidos após estimativa técnica, recursos e dependências.
- Rever este roadmap ao concluir cada gate e atualizar o estado com evidência de commit, testes e aprovação.

## Próxima ação

A auditoria documental cruzada dos 36 Markdown está concluída. Próxima ação: formalizar responsáveis, aprovar âmbito e requisitos MVP e concluir G0/G1 na [issue #1](https://github.com/carlos-andrade/MELLITUS/issues/1); só depois iniciar G2 e a seleção da stack.


## Adenda de controlo — 2026-10-15

A issue #1 foi reaberta para corrigir o encerramento prematuro da checklist. O proprietário aceitou em princípio o âmbito educativo e as exclusões clínicas, mas a aprovação G0/G1 permanece pendente de evidência explícita para as restantes entradas. Não iniciar implementação funcional nem recolha de dados de saúde por inferência.

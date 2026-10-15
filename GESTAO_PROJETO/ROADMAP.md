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
| **SHA-256 (conteúdo canónico)** | 85151cf4096f98cca9d9a718f4434fc6fd67e8dabb6ba1100465c88aa6a027c5 |
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

## Evidência de viabilidade

A estimativa preliminar está em [ESTIMATIVA_VIABILIDADE_MVP.md](ESTIMATIVA_VIABILIDADE_MVP.md). Intervalo de esforço indicativo: 31–54 horas para o âmbito estático mínimo, sujeito a validação. Custo monetário, responsáveis e prazo permanecem por formalizar. O documento não aprova G0/G1 nem autoriza implementação.

## Plano por fases

| Fase | Entregáveis | Critérios de saída | Estado atual |
|---|---|---|---|
| P0 — Baseline e governação | Inventário, requisitos, responsáveis, decisões, estimativa de viabilidade, cabeçalhos/integridade | G0/G1 formalmente aceites | EM_CURSO |
| P1 — Catálogo de fontes oficiais | Catálogo de fontes oficiais, links verificados, metadados e aviso de fonte externa; sem artigos/resumos próprios | Ligações testadas e critérios do catálogo aprovados; âmbito ratificado em G0/G1 | PROPOSTO |
| P2 — Arquitetura e proteção | Stack, modelo de dados, ameaça, privacidade, arquitetura | G2 aceite por decisores competentes | PROPOSTO |
| P3 — Fundação técnica | Estrutura de código, configuração, testes básicos, CI | Build e testes reproduzíveis | PROPOSTO |
| P4 — MVP diretório educativo | UI responsiva, navegação/pesquisa de fontes oficiais, metadados e aviso de âmbito | Requisitos testados; sem conteúdo clínico próprio e sem dados pessoais de saúde | PROPOSTO |
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

A auditoria documental cruzada dos 36 Markdown foi concluída anteriormente. O proprietário declarou que não haverá revisor clínico; por isso, o MVP proposto foi reduzido a catálogo de ligações para fontes oficiais, sem conteúdo clínico próprio. Em 2026-10-15, a verificação do catálogo foi atualizada: SNS 24 responde com aplicação dependente de JavaScript; uma página oficial NICE NG28 foi localizada, mas o acesso automatizado ao portal-raiz devolveu 403. A issue #1 continua aberta; foram corrigidas caixas indevidamente assinaladas como concluídas. Faltam ratificação formal do âmbito, responsáveis nomeados, evidência de viabilidade e decisão G0/G1. Foi criada uma estimativa preliminar de viabilidade com alternativas e intervalo de esforço de 31–54 horas; permanece PROPOSTA, sem compromisso financeiro ou de prazo. Só depois preparar G2 e selecionar stack.


## Adenda de controlo — 2026-10-15

A issue #1 foi reaberta para corrigir o encerramento prematuro da checklist. O proprietário aceitou em princípio o âmbito educativo e as exclusões clínicas, mas a aprovação G0/G1 permanece pendente de evidência explícita para as restantes entradas. Não iniciar implementação funcional nem recolha de dados de saúde por inferência.


## Adenda — ausência de revisor clínico — 2026-10-15

A fase P1 passa a ser proposta como catálogo de fontes oficiais, com URL e metadados verificados. Artigos clínicos originais, resumos, traduções, interpretações e recomendações ficam fora do MVP porque o proprietário decidiu não nomear revisor clínico. Esta alteração reduz o risco, mas não constitui aprovação de G0/G1 ou G2. Registos pessoais, integrações e funções clínicas continuam bloqueados.

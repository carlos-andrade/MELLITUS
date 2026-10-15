# Registo de decisões — MELLITUS

| Campo | Valor |
|---|---|
| **ID** | MEL-DEC-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | REGISTO |
| **Fase** | F0 — Governação e requisitos |
| **Estado** | EM_REVISAO |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | PENDENTE_DE_CALCULO_VERIFICADO |
| **Commit de referência (versão anterior)** | N/A — documento inicial |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Responsável de projeto — a formalizar |
| **Aprovador** | Pendente de aprovação formal |
| **Origem** | Registo inicial do briefing e da governação central |
| **Autoridade superior** | [Constituição GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA/blob/main/CONSTITUICAO.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | README.md; docs/PLANO_DIRETOR.md; GOVERNANCA/GOVERNANCA.md |
| **Escopo** | Decisões materiais e decisões pendentes |
| **Objetivo** | Preservar razões das escolhas e evitar decisões implícitas |
| **Dependências** | Revisão periódica e atualização com as alterações |

## Decisões registadas

| ID | Data | Decisão/orientação | Estado | Justificação | Próximo passo/evidência |
|---|---|---|---|---|---|
| MEL-D001 | 2026-10-15 | Repositório oficial: `carlos-andrade/MELLITUS`. | EM_CURSO | Fonte central do código e documentação. | Confirmar alterações no repositório. |
| MEL-D002 | 2026-10-15 | Público-alvo inicial: público em geral. | EM_REVISAO | Definição inicial do projeto. | Formalizar no gate G0. |
| MEL-D003 | 2026-10-15 | Objetivo: plataforma de informação e acompanhamento da diabetes. | EM_REVISAO | Definição inicial do projeto. | Aprovar âmbito e limites. |
| MEL-D004 | 2026-10-15 | Seguir as regras do repositório GOVERNANCA. | EM_CURSO | Instrução explícita do proprietário do projeto. | Validar artefactos e registar exceções. |
| MEL-D005 | 2026-10-15 | Priorizar conteúdo educativo; módulo de acompanhamento fica para fase própria. | PROPOSTO | Reduz complexidade inicial e dependência de dados de saúde. | Aprovar na especificação do MVP. |
| MEL-D006 | 2026-10-15 | Excluir diagnóstico, prescrição e ajustes autónomos de medicação do MVP. | PROPOSTO | Limite essencial de segurança. | Integrar em requisitos e testes. |
| MEL-D007 | 2026-10-15 | Usar cabeçalho Markdown padrão da GOVERNANCA. | EM_CURSO | Norma documental superior. | Calcular/validar SHA-256 e referências de commit. |
| MEL-D008 | 2026-10-15 | Aplicar gates G0–G6 e estados controlados. | EM_CURSO | Constituição GOVERNANCA. | Criar matriz de gates e aprovações. |

## Decisões pendentes

| ID | Questão | Responsável | Critério de encerramento |
|---|---|---|---|
| MEL-P001 | Quem assume formalmente produto/projeto? | Patrocinador/proprietário | Nomeação registada |
| MEL-P002 | Quem fará a revisão clínica? | Responsável de projeto | Revisor qualificado e fluxo identificados |
| MEL-P003 | Qual é o MVP aprovado? | Responsável de produto | Requisitos ratificados |
| MEL-P004 | Qual a estratégia de privacidade e necessidade de AIPD/DPIA? | Privacidade/jurídico | Avaliação documentada |
| MEL-P005 | Qual a classificação regulatória das funções planeadas? | Conformidade com apoio especializado | Avaliação da finalidade e funcionalidades concretas |
| MEL-P006 | Como adotar e testar WATCHDOG no MELLITUS? | Técnico/operações | Inventário, critérios, teste de falha e evidência |

## Regra de atualização

Cada decisão material deve incluir ID único, data, contexto, alternativas relevantes, decisão, estado, responsável, aprovador quando necessário e evidência. Não apagar decisões históricas; registar reversões como novas decisões ligadas à original.

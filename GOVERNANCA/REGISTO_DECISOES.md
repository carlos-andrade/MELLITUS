# Registo de decisões — MELLITUS

| Campo | Valor |
|---|---|
| **ID** | MEL-DEC-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | REGISTO |
| **Fase** | F0 — Governação e requisitos |
| **Estado** | EM_REVISAO — decisões G2 propostas; ratificação pendente |
| **Versão** | 1.1.0 |
| **SHA-256 (conteúdo canónico)** | d331e8d81e9c890341b137d3fbab79fb2f43d68dc54473fde2d9e14384a4b559 |
| **Commit de referência (versão anterior)** | Histórico Git preservado; SHA do commit anterior não verificado nesta atualização |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Carlos Andrade — patrocinador/responsável de produto |
| **Aprovador** | G0/G1 aprovados; G2 pendente |
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

| MEL-D009 | 2026-10-15 | Definir uma estrutura modular para o produto com documentação separada de arquitetura, segurança, qualidade, operações e produto. | EM_REVISAO | Necessidade de preparar desenvolvimento governado e evitar confundir planeamento com implementação. | Revisar ESTRUTURA_PROJETO.md e aprovar por gate aplicável. |
| MEL-D010 | 2026-10-15 | Criar a matriz de rastreabilidade e abrir issue para formalizar decisões G0/G1. | EM_CURSO | Requisitos devem ligar-se a riscos, evidências, testes e gates; aprovações não podem ser presumidas. | docs/MATRIZ_RASTREABILIDADE.md; https://github.com/carlos-andrade/MELLITUS/issues/1 |

## Decisões pendentes

| ID | Questão | Responsável | Critério de encerramento |
|---|---|---|---|
| MEL-P001 | Quem assume formalmente produto/projeto? | Patrocinador/proprietário | RESOLVIDO — Carlos Andrade confirmado na aprovação D1–D8 da issue #1 |
| MEL-P002 | Ratificar formalmente o âmbito reduzido sem revisão clínica: apenas catálogo de fontes oficiais, sem conteúdo clínico próprio. | Carlos Andrade | RESOLVIDO — D1–D8 aprovadas; G0/G1 aprovados na issue #1 |
| MEL-P003 | Qual é o MVP aprovado? | Carlos Andrade | RESOLVIDO — diretório estático de links oficiais e metadados; sem conteúdo clínico próprio ou dados de saúde |
| MEL-P004 | Qual a estratégia de privacidade e necessidade de AIPD/DPIA? | Privacidade/jurídico | Avaliação documentada |
| MEL-P005 | Qual a classificação regulatória das funções planeadas? | Conformidade com apoio especializado | Avaliação da finalidade e funcionalidades concretas |
| MEL-P006 | Como adotar e testar WATCHDOG no MELLITUS? | Técnico/operações | Inventário, critérios, teste de falha e evidência |

## Regra de atualização

Cada decisão material deve incluir ID único, data, contexto, alternativas relevantes, decisão, estado, responsável, aprovador quando necessário e evidência. Não apagar decisões históricas; registar reversões como novas decisões ligadas à original.


| MEL-D011 | 2026-10-15 | O proprietário aprovou explicitamente D1–D8, confirmou Carlos Andrade como patrocinador/responsável de produto, aceitou a estimativa preliminar de 31–54 horas e autorizou apenas preparação/avaliação G2. | APROVADO — G0/G1 | Aprovação explícita registada na issue #1; custo monetário permanece UNKNOWN e não há autorização de implementação. | G2 rastreado na issue #2; fechar alojamento/privacidade e obter decisão formal G2 antes de G3. |

| MEL-D012 | 2026-10-15 | O proprietário declarou: “NÃO TEREMOS REVISOR.” | ACEITE | Não será nomeado revisor clínico; o risco de publicar conteúdo clínico próprio sem revisão não é aceite como controlado. | Excluir artigos, resumos, traduções, interpretações e recomendações clínicas próprias; âmbito reduzido aprovado em docs/REQUISITOS.md e issue #1. |
| MEL-D013 | 2026-10-15 | MVP limitado a diretório de fontes oficiais, com ligações diretas, metadados e data de verificação; sem dados pessoais de saúde. | APROVADO — G0/G1 | Mitigação proporcional à decisão de não nomear revisor clínico. Não equivale a validação clínica das páginas externas. | Preservar âmbito; alterações exigem nova decisão. G2 continua pendente. |


## Decisões G2 — propostas, não aprovadas

| ID | Data | Decisão/orientação | Estado | Justificação | Próximo passo/evidência |
|---|---|---|---|---|---|
| MEL-D-G2-001 | 2026-10-15 | Recomendar arquitetura estática versionada em Git, sem backend, base de dados, contas ou dados de saúde no MVP. | PROPOSTO | Reduz superfície de ataque e minimiza dados. | Ratificar pacote G2 e ADR-001 após fechar pendências de alojamento/privacidade. |
| MEL-D-G2-002 | 2026-10-15 | Excluir analytics, trackers, cookies próprios, formulários e recursos remotos de terceiros no desenho-base. | PROPOSTO | Minimização e prevenção de rastreamento desnecessário. | Validar tecnicamente numa build autorizada. |
| MEL-D-G2-003 | 2026-10-15 | Manter fornecedor/região de alojamento por decidir até avaliar termos, logs, retenção, subprocessadores e custos. | PENDENTE | A escolha afeta privacidade e não há orçamento autorizado. | Avaliação documentada e decisão explícita. |
| MEL-D-G2-004 | 2026-10-15 | Não concluir ainda se AIPD é necessária; executar triagem face ao tratamento real e regras CNPD/RGPD. | PENDENTE | A decisão depende do fornecedor e dos fluxos efetivos. | Registar decisão fundamentada antes da publicação. |

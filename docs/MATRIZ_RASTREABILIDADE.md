# Matriz de rastreabilidade — MELLITUS

| Campo | Valor |
|---|---|
| **ID** | MEL-TRACE-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | MATRIZ_RASTREABILIDADE |
| **Fase** | F0 — Governação e requisitos |
| **Estado** | EM_REVISAO |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | PENDENTE_DE_CALCULO |
| **Commit de referência (versão anterior)** | N/A — documento inicial |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Responsável de projeto/produto — a formalizar |
| **Aprovador** | Pendente de aprovação G0/G1 |
| **Origem** | docs/REQUISITOS.md; docs/RISCOS.md; docs/VALIDACAO.md |
| **Autoridade superior** | [GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA); [norma de cabeçalho](https://github.com/carlos-andrade/GOVERNANCA/blob/main/CABE%C3%87ALHO/NORMA-CABECALHO-PADRAO.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | docs/REQUISITOS.md; docs/RISCOS.md; docs/VALIDACAO.md; GESTAO_PROJETO/ROADMAP.md |

## 1. Objetivo

Ligar os requisitos iniciais a riscos, evidências, testes e gates. A matriz representa o estado documental observado, não aprovação dos requisitos nem execução dos testes.

## 2. Matriz inicial

| Requisito | Risco relacionado | Evidência/artefacto exigido | Teste/validação exigida | Gate | Estado atual |
|---|---|---|---|---|---|
| MEL-FR-001 — conteúdo educativo | MEL-R-001, MEL-R-002 | Artigo com fontes rastreáveis e revisão adequada | Revisão editorial/clínica do artigo e verificação das fontes | G1/G2/G3 | UNKNOWN — artigo piloto não aprovado |
| MEL-FR-002 — fontes e data de revisão | MEL-R-001, MEL-R-008 | Ficha de fontes, versão, data de consulta/revisão | Verificar links, versão, afirmações suportadas e data | G2/G3 | UNKNOWN — catálogo ainda por validar |
| MEL-FR-003 — navegação e pesquisa | MEL-R-007, MEL-R-008 | Implementação e critérios de aceitação | Testes funcionais de pesquisa e navegação | G2/G3 | UNKNOWN — aplicação não implementada |
| MEL-FR-004 — limites educativos | MEL-R-002 | Avisos de âmbito e encaminhamento adequado | Revisão de conteúdo e teste de visibilidade/compreensão | G2/G3 | UNKNOWN — aplicação não implementada |
| MEL-FR-005 — responsividade | MEL-R-007 | Matriz de browsers/ecrãs suportados | Testes funcionais e acessibilidade nos ambientes definidos | G2/G3 | UNKNOWN — aplicação não implementada |
| MEL-FR-006 — workflow editorial | MEL-R-001, MEL-R-008 | Estados, histórico de versões, autoria e revisão | Testar criação, revisão, publicação, correção e retirada | G2/G3 | UNKNOWN — workflow não implementado |
| MEL-FR-101 a 104 — registos pessoais | MEL-R-003, MEL-R-004, MEL-R-009 | Requisitos próprios, modelo de dados, avaliação de privacidade e autorização | Testes de isolamento, exportação/eliminação e segurança, se aprovados | Novo G1/G2 | BLOQUEADO — fora do MVP |
| MEL-NFR-001 — segurança | MEL-R-003, MEL-R-009 | Modelo de ameaças e controlos implementados | Testes de autorização, injeção, XSS, CSRF, segredos e dependências | G2/G3/G4 | UNKNOWN — não implementado |
| MEL-NFR-002 — privacidade | MEL-R-004, MEL-R-009 | Inventário de dados, finalidade, base legal, retenção e direitos | Revisão especializada; AIPD/DPIA quando aplicável | G1/G2/G4 | UNKNOWN — avaliação por fazer |
| MEL-NFR-003 — auditoria | MEL-R-008 | Política de eventos e minimização de logs | Verificar eventos críticos e ausência de segredos/dados excessivos | G2/G3/G4 | UNKNOWN — não implementado |
| MEL-NFR-004 — acessibilidade | MEL-R-007 | Critérios de acessibilidade aprovados | Ferramentas automáticas e revisão manual com teclado/leitor de ecrã | G2/G3 | UNKNOWN — não executado |
| MEL-NFR-005 — recuperação | MEL-R-006 | Política de backup, RPO/RTO, runbook e rollback | Ensaio real de restauração e rollback com evidência | G4 | UNKNOWN — não executado |
| MEL-NFR-006 — observabilidade | MEL-R-006, MEL-R-008 | Inventário WATCHDOG, critérios, responsáveis e alertas | Injetar cenário de falha e confirmar alerta/escalonamento | G2/G4 | UNKNOWN — MELLITUS sem monitorização ativa demonstrada |
| MEL-NFR-007 — integridade científica | MEL-R-001, MEL-R-002 | Matriz afirmação-fonte e registo de revisão | Auditoria amostral de afirmações e referências | G1/G3 | UNKNOWN — conteúdo clínico não aprovado |
| MEL-NFR-008 — portabilidade | MEL-R-004 | Formato de exportação e limites documentados, se aplicável | Validar integridade, autorização e ausência de dados de terceiros | Novo G1/G2 | BLOQUEADO — depende do módulo pessoal |

## 3. Regras de estado

- PASS: critério demonstrado com evidência verificável.
- WARN: limitação conhecida, explicitada e aceite por autoridade competente.
- FAIL: critério não cumprido.
- UNKNOWN: não executado ou evidência insuficiente.
- Requisitos em PROPOSTO ou EM_REVISAO não constituem baseline aprovada.
- Nenhum estado UNKNOWN pode ser promovido a PASS por inferência ou pela existência de documentação.
- A matriz deve ser atualizada quando um requisito mudar, um teste for executado ou um gate for decidido.

## 4. Pendências para G0/G1

1. Formalizar patrocinador, responsável de projeto/produto e autoridade de aprovação.
2. Confirmar beneficiários, problema e resultado mensurável.
3. Aprovar o MVP educativo e as exclusões clínicas.
4. Nomear revisor clínico qualificado e definir o nível de revisão por risco.
5. Estimar alternativas, custo, capacidade, riscos e dependências.
6. Registar a decisão G0/G1 com aprovador e evidência.
7. Só então preparar o gate G2 para arquitetura e privacidade.

## 5. Resultado da validação

Estado inicial: UNKNOWN para implementação e testes; baseline funcional ainda não aprovada. Esta matriz melhora a rastreabilidade, mas não aprova qualquer gate.

## 6. Próxima ação

Concluir revisão F0 e obter decisão formal G0/G1. Não iniciar implementação funcional nem recolha de dados pessoais de saúde antes dos gates aplicáveis.

# Operação, implantação e WATCHDOG — MELLITUS

| Campo | Valor |
|---|---|
| **ID** | MEL-OPS-README-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | PLANO_OPERACOES |
| **Fase** | F4 — Prontidão operacional |
| **Estado** | PROPOSTO |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | 105c4c3696f359cdcba44419de2dffca8d71137ce9c8256f29970a0d75611590 |
| **Commit de referência (versão anterior)** | N/A — documento inicial |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Responsável de operações — a formalizar |
| **Aprovador** | Pendente de prontidão operacional |
| **Origem** | Governação e requisitos MELLITUS |
| **Autoridade superior** | [GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA); [governação MELLITUS](../GOVERNANCA/GOVERNANCA.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | docs/RISCOS.md; docs/VALIDACAO.md; SEGURANCA/README.md |

## 1. Objetivo e estado

Definir as condições para operar e manter o produto. A pasta é planeamento; nenhum alojamento, alarme, backup, deploy ou monitorização MELLITUS é declarado ativo por existir este documento.

## 2. Ambientes propostos

- Desenvolvimento local.
- Integração contínua e testes.
- Staging com configuração semelhante à produção e dados sintéticos.
- Produção, apenas após gates e autorização.
- Segredos, bases de dados e permissões separados por ambiente.

## 3. Implantação

O processo deve ter artefacto versionado, revisão, migrações controladas, validações pré/pós-deploy, estratégia de rollback e responsável identificável. Proibir alteração manual não rastreada em produção, salvo procedimento de emergência documentado.

## 4. WATCHDOG

Adotar o padrão WATCHDOG da GOVERNANCA para inventário e estado dos controlos. Por integração, registar identificador, ativo, criticidade, verificação, frequência adequada, última execução, resultado, evidência, responsável, escalonamento e procedimento de recuperação. Usar `PASS`, `WARN`, `FAIL` ou `UNKNOWN`; ausência de telemetria não significa sucesso.

A disponibilidade do próprio monitor deve ser detetável por meio independente quando o risco o exigir. Remediação automática fica desativada por defeito e requer autorização explícita, limites, logs e rollback. Nenhum controlo é anunciado como ativo antes de ser implementado e testado.

## 5. Backups e recuperação

Definir RPO/RTO com o proprietário de produto, política de cópias, encriptação, permissões, retenção, proteção contra eliminação maliciosa e periodicidade de ensaios. Testar restauração integral e consistência dos dados. Não incluir cópias com dados pessoais fora da política aprovada.

## 6. Suporte e incidentes

Definir canal de contacto, severidade, responsáveis, horários, procedimentos de escalonamento, análise de causa, comunicação e pós-incidente. A disponibilidade de serviço ou tempos de resposta só serão prometidos depois de capacidade operacional demonstrada.

## 7. Critérios mínimos antes de produção

- Aprovação G4/G5.
- Revisão de segurança e privacidade concluída.
- Conteúdo clínico aprovado conforme política.
- Alertas e logs testados sem recolher dados excessivos.
- Backup restaurado com evidência.
- Runbook, rollback e responsável disponíveis.
- Plano para incidentes e correções de conteúdo definido.

## 8. Próxima ação

Definir requisitos operacionais, alojamento, custo, suporte e recuperação; implementar monitorização e demonstrar os controlos antes de solicitar G4.

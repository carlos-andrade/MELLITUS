# Governação do projeto MELLITUS

| Campo | Valor |
|---|---|
| **ID** | MEL-GOV-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | POLITICA |
| **Fase** | F0 — Governação e requisitos |
| **Estado** | EM_REVISAO |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | 30a76d0df40aaeca4c77d150fb6b23385ca34b9d |
| **Commit de referência (versão anterior)** | N/A — documento inicial |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Responsável de projeto — a formalizar |
| **Aprovador** | Pendente de aprovação formal |
| **Origem** | Adoção das regras do repositório central GOVERNANCA |
| **Autoridade superior** | [Constituição](https://github.com/carlos-andrade/GOVERNANCA/blob/main/CONSTITUICAO.md); [Norma de cabeçalho](https://github.com/carlos-andrade/GOVERNANCA/blob/main/CABE%C3%87ALHO/NORMA-CABECALHO-PADRAO.md); [README](https://github.com/carlos-andrade/GOVERNANCA/blob/main/README.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | README.md; docs/PLANO_DIRETOR.md; GOVERNANCA/REGISTO_DECISOES.md |
| **Escopo** | Documentos, dados, software, workflows, releases e operações MELLITUS |
| **Objetivo** | Aplicar a governança superior com controlos proporcionais ao risco de saúde |
| **Dependências** | Aprovação formal da baseline e definição de responsáveis |

## 1. Autoridade e precedência

O MELLITUS adota o sistema de governação em [carlos-andrade/GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA). Em caso de conflito, aplica-se a hierarquia da Constituição: (1) lei aplicável; (2) contratos vinculativos; (3) políticas formalmente aprovadas; (4) padrões e procedimentos; (5) recomendações e exemplos. Conflitos devem ser registados e escalados. Este documento adapta as regras ao contexto de saúde, sem substituir nem alterar a governação mestre.

## 2. Princípios obrigatórios

- Propósito verificável e beneficiários identificados.
- Responsável explícito para resultados, riscos e decisões.
- Controlos proporcionais ao impacto e às obrigações.
- Segurança e privacidade desde a conceção.
- Evidência antes de declarar execução ou conclusão.
- Rastreabilidade entre requisitos, decisões, alterações, versões, incidentes e releases.
- Critérios mensuráveis antes da aceitação.
- Revisão humana quando o impacto clínico o exige.
- Reversibilidade de mudanças de maior impacto.
- Origem, qualidade, acesso, retenção e eliminação de dados explícitos.
- Nenhuma aprovação presumida.

## 3. Cadeia de autoridade

Aplicar a cadeia documental exigida pela GOVERNANCA: `PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO`. Documentar a correspondência dos artefactos MELLITUS; esta sequência não autoriza implementação sem requisitos, desenho e gates aplicáveis.

## 4. Gates G0–G6

- **G0 — Entrada:** problema, beneficiários, patrocinador/owner e resultado identificados.
- **G1 — Viabilidade:** valor, alternativas, custos, riscos, dependências e capacidade revistos.
- **G2 — Desenho:** requisitos, arquitetura, dados, ameaças, aceitação e testes definidos.
- **G3 — Construção validada:** revisão, testes, artefactos e documentação apresentados.
- **G4 — Prontidão operacional:** segurança, recuperação, observabilidade, suporte e rollback avaliados.
- **G5 — Lançamento:** autorização explícita, plano de implantação, observação e rollback.
- **G6 — Encerramento:** aceitação, transferência, pendências, arquivo/eliminação e lições registados.

Cada gate requer decisor autorizado e evidência verificável. Simplificação exige justificação escrita e não pode remover controlos legais ou críticos.

## 5. Estados controlados

Usar os estados da GOVERNANCA: `PROPOSTO`, `EM_CURSO`, `BLOQUEADO`, `EM_REVISAO`, `APROVADO`, `REJEITADO`, `CONCLUIDO`, `DEPRECADO`. Para controlos de monitorização, usar `PASS`, `WARN`, `FAIL` e `UNKNOWN`. Ausência de evidência nunca equivale a sucesso. Distinguir estado documental, estado de implementação e estado operacional.

## 6. Cabeçalhos e integridade

Todos os documentos Markdown começam com título H1 e tabela Markdown conforme [NORMA-CABECALHO-PADRAO.md](https://github.com/carlos-andrade/GOVERNANCA/blob/main/CABE%C3%87ALHO/NORMA-CABECALHO-PADRAO.md). Os campos de SHA-256 canónico e commit de referência seguem a norma. Nesta gravação inicial estão pendentes de validação; calcular e verificar antes de declarar conformidade total.

## 7. Segurança clínica

- Conteúdo clínico publicado deve ter fontes rastreáveis e revisão adequada.
- Não oferecer diagnóstico, prescrição ou ajuste autónomo de medicação.
- Mudança de finalidade ou funcionalidade com potencial clínico exige reavaliação de risco.
- Possível enquadramento como dispositivo médico ou IA regulada deve ser avaliado segundo a finalidade e as funções reais.
- Eventos potencialmente perigosos exigem triagem, correção e escalonamento documentados.

## 8. Privacidade e dados

Antes de recolher dados de saúde, documentar finalidade, base legal, minimização, consentimento quando aplicável, acesso, retenção, eliminação, exportação, resposta a incidentes e necessidade de AIPD/DPIA. Não usar dados reais em testes sem base legal e controlos apropriados.

## 9. WATCHDOG

Avaliar o padrão WATCHDOG da GOVERNANCA nos workflows e sistemas relevantes. Registar inventário, controlos, limiares, evidências e responsáveis. Não alegar monitorização contínua, alerta ativo ou supervisão independente sem integração implementada, teste de falha e evidência operacional. Estados: `PASS`, `WARN`, `FAIL`, `UNKNOWN`.

## 10. Exceções

Registar regra afetada, motivo, risco, controlos compensatórios, aprovador, validade, responsável e condição de revogação. Exceções não dispensam leis, contratos ou requisitos críticos de segurança clínica.

## 11. Revisão e auditoria

Rever após alterações materiais, incidentes, alterações legais, integrações clínicas ou novas classes de dados. Auditar conteúdo e evidências, não apenas presença de ficheiros. A implementação dos cabeçalhos, gates ou WATCHDOG só pode ser considerada conforme após validações próprias.

## 12. Próxima ação

Verificar cabeçalhos, calcular SHA-256 segundo a norma, estabelecer matriz requisito/gate e registar decisão G0. Não declarar fases concluídas antes da validação.

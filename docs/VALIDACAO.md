# Plano de validação — MELLITUS

| Campo | Valor |
|---|---|
| **ID** | MEL-QA-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | PLANO_VALIDACAO |
| **Fase** | F0 — Governação e requisitos |
| **Estado** | EM_REVISAO |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | 7c45e02958091c15d477595b643029fe1cf2ba16e117cec21028d8b9018bbb99 |
| **Commit de referência (versão anterior)** | N/A — documento inicial |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Responsável de qualidade — a formalizar |
| **Aprovador** | Pendente de aprovação formal |
| **Origem** | Plano inicial alinhado com os gates da GOVERNANCA |
| **Autoridade superior** | [Constituição GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA/blob/main/CONSTITUICAO.md); [Ciclo de vida e gates](https://github.com/carlos-andrade/GOVERNANCA/blob/main/docs/02-ciclo-de-vida/ciclo-de-vida-e-gates.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | docs/REQUISITOS.md; docs/RISCOS.md; docs/PLANO_DIRETOR.md |
| **Escopo** | Validação documental, clínica, funcional, segurança, privacidade, acessibilidade e operação |
| **Objetivo** | Definir evidência necessária antes de aceitar requisitos e gates |
| **Dependências** | Casos de teste, ambientes controlados e revisores competentes |

## 1. Princípios

- Definir critérios antes de testar.
- Registar versão, ambiente, método, resultado, limitações e evidência.
- Falta de teste ou dados gera `UNKNOWN`, não `PASS`.
- Separar validação documental, técnica, clínica, legal e operacional.
- A revisão independente é proporcional ao risco.
- Critérios propostos precisam de aprovação e operacionalização.

## 2. Gates de qualidade

| ID | Critério | Evidência obrigatória | Bloqueia lançamento? |
|---|---|---|---|
| MEL-GQ-01 | Requisitos críticos rastreados a testes | Matriz e resultados | Sim |
| MEL-GQ-02 | Conteúdo clínico com fontes e revisão apropriada | Registo editorial, fonte, data e aprovação | Sim |
| MEL-GQ-03 | Nenhuma vulnerabilidade crítica/alta conhecida fica sem tratamento aprovado | Relatório de segurança e remediações | Sim |
| MEL-GQ-04 | Fluxos críticos funcionam e defeitos bloqueadores estão resolvidos | Resultados de testes funcionais | Sim |
| MEL-GQ-05 | Privacidade e tratamento de dados documentados | Finalidade, base legal, acessos, retenção, direitos e AIPD/DPIA quando aplicável | Sim antes de dados reais |
| MEL-GQ-06 | Acessibilidade/usabilidade avaliadas | Auditoria e testes manuais | Conforme âmbito/risco |
| MEL-GQ-07 | Backup/restauro, observabilidade, suporte e rollback testados | Evidências datadas e runbooks | Sim antes de produção |
| MEL-GQ-08 | Aprovação formal do gate registada | Decisão por responsável autorizado | Sim |

## 3. Tipos de teste

- Testes unitários e de integração.
- Testes de API, autenticação, autorização e isolamento entre utilizadores.
- Testes de validação de entradas e tratamento de erros.
- Testes de acessibilidade automatizados e manuais.
- Testes de usabilidade e compreensão dos avisos.
- Revisão clínica do conteúdo.
- Auditoria de dependências e segurança.
- Testes de backup, restauro, logging, alertas e rollback.
- Testes de exportação/eliminação se esses módulos forem implementados.

## 4. Cobertura e resultados

Cobertura de linhas não é a única medida de qualidade. Combinar cobertura com requisitos críticos testados, condições de erro, revisão de código, riscos e evidências. Qualquer meta numérica requer aprovação após desenho da arquitetura e requisitos.

Estados:
- `PASS`: critérios demonstrados para o âmbito do teste.
- `WARN`: desvio ou limitação explicitada, aceite por autoridade adequada.
- `FAIL`: critério não satisfeito.
- `UNKNOWN`: evidência insuficiente ou teste não executado.

Um gate não pode ser aceite com `FAIL` num controlo crítico. `UNKNOWN` num controlo obrigatório impede a alegação de conformidade até resolução.

## 5. Relatório mínimo

Registar ID, requisito/risco, versão, ambiente, data, executor/revisor, passos, resultado esperado e observado, evidência, defeitos, limitações e decisão. Não incluir credenciais, tokens ou dados de saúde reais nos relatórios versionados.

## 6. Próxima ação

Criar matriz de rastreabilidade quando os requisitos forem aprovados e executar testes apenas sobre artefactos concretos. Não existem resultados de teste de produto declarados como concluídos neste momento.

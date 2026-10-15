# Estratégia de qualidade e testes — MELLITUS

| Campo | Valor |
|---|---|
| **ID** | MEL-QA-README-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | PLANO_TESTES |
| **Fase** | F2 — Arquitetura e proteção de dados |
| **Estado** | EM_REVISAO |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | 8895c665d24d8abc641b7707c52e31d942fbb4bb1e54666140615a69898d6835 |
| **Commit de referência (versão anterior)** | N/A — documento inicial |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Responsável de qualidade — a formalizar |
| **Aprovador** | Pendente de critérios e ambiente de teste |
| **Origem** | Requisitos MELLITUS e plano de validação |
| **Autoridade superior** | [GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA); [governação MELLITUS](../GOVERNANCA/GOVERNANCA.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | docs/REQUISITOS.md; docs/VALIDACAO.md; docs/RISCOS.md |

## 1. Objetivo

Definir uma estratégia que permita avaliar a aplicação por evidência. Nenhum teste é considerado executado até existirem execução, ambiente, comando/versão, resultado e artefacto verificável.

## 2. Camadas de testes

- **Unitários:** regras de domínio, validação, filtros e transformações.
- **Integração:** persistência, transações, serviços e APIs aprovadas.
- **Ponta a ponta:** percurso de pesquisa, leitura de artigos e fluxo editorial.
- **Regressão:** reprodução de defeitos confirmados.
- **Segurança:** autorização, sessões, CSRF, XSS, injeção, abuso de autenticação, segredos e permissões.
- **Acessibilidade:** automatização mais avaliação manual com teclado e leitor de ecrã.
- **Compatibilidade:** browsers e ecrãs suportados definidos pelo produto.
- **Performance:** métricas definidas antes do teste e testadas em ambiente comparável.
- **Resiliência:** backup, restauração, rollback, falha de dependência e recuperação.
- **Conteúdo clínico:** rastreabilidade de afirmações, revisão e validação de links/fontes.
- **Privacidade:** exportação/eliminação se implementadas, segregação e ausência de dados sensíveis nos logs.

## 3. Gates de qualidade

- Nenhuma falha crítica ou alta sem decisão formal de tratamento antes do lançamento.
- Todos os requisitos selecionados para o MVP ligados a casos de teste.
- Conteúdo clínico sujeito a revisão conforme o risco antes de publicação.
- Testes executados em ambiente identificado e reproduzível.
- Resultados e defeitos registados e rastreáveis.
- Cobertura de código é métrica auxiliar, não prova suficiente de qualidade.
- A restauração de backup deve ser demonstrada, não apenas configurada.

## 4. Evidência mínima por execução

Registar ID de teste, requisito relacionado, commit/versão, sistema e configuração, data, comando/procedimento, resultado esperado/obtido, logs ou relatório, defeitos, responsável e decisão.

Estados válidos do controlo: `PASS`, `WARN`, `FAIL`, `UNKNOWN`. Um teste não executado ou sem evidência é `UNKNOWN`, não `PASS`.

## 5. Pipeline CI proposto

Depois de a stack ser aprovada, criar pipeline para validação de sintaxe, análise estática, testes automatizados, verificação de dependências, deteção de segredos e construção reproduzível. Não adicionar workflows que aleguem sucesso antes da implementação e do teste. Segredos devem ficar nas definições seguras do GitHub, nunca nos ficheiros do repositório.

## 6. Próxima ação

Aprovar stack e critérios de aceitação, criar a primeira matriz requisito-teste e executar os testes apenas quando existir aplicação identificável.

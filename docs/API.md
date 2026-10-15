# MELLITUS — Contrato de API e política de integração

| Campo | Valor |
|---|---|
| **ID** | MEL-API-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | ESPECIFICACAO_API |
| **Fase** | F2 — Arquitetura e proteção de dados |
| **Estado** | PROPOSTO |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | eb1484bb6b5dcad8aa9d43d3effb0c34b64b567225c81c795e2e8cab221828b6 |
| **Commit de referência (versão anterior)** | N/A — documento inicial |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Responsável técnico — a formalizar |
| **Aprovador** | Pendente de decisão G2 |
| **Origem** | docs/ARQUITETURA.md e docs/REQUISITOS.md |
| **Autoridade superior** | [GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA); [docs/ARQUITETURA.md](ARQUITETURA.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |

## 1. Estado

Não existe contrato de API implementado ou aprovado. O MVP pode não precisar de API pública separada. Este documento define princípios para o caso de ser necessária.

## 2. Princípios

- Não expor API sem requisito e decisão arquitetural.
- Definir endpoints, métodos, schemas, erros, autenticação, autorização, limites e versão antes de implementar.
- Validar dados no servidor e aplicar autorização por recurso.
- Não expor dados pessoais/de saúde no MVP.
- Documentar origem, licenciamento e fundamento das integrações externas.
- Usar TLS, timeouts, limites e monitorização.
- Não registar segredos ou conteúdo clínico identificável.
- Evitar integrações com dispositivos antes de avaliação regulatória e de risco.

## 3. Contrato por endpoint

Definir ID do requisito, finalidade, método/caminho, autenticação, autorização, schema, validação, erros, limites/timeouts, idempotência, classificação de dados, retenção, logging, testes e versão/depreciação.

## 4. Próxima ação

Confirmar se há requisito para API externa. Se não, não construir API por defeito.

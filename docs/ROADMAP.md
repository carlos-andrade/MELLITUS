# MELLITUS — Roadmap de execução

| Campo | Valor |
|---|---|
| **ID** | MEL-ROADMAP-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | ROADMAP |
| **Fase** | F0 — Governação e requisitos |
| **Estado** | EM_REVISAO |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | d184673b097dc2a9d86d899c49461d90e78300398c5b92b133b72fe208209f3c |
| **Commit de referência (versão anterior)** | [ae991e6d0c633ec6905d2177f57a3f006d0860d0](https://github.com/carlos-andrade/MELLITUS/commit/ae991e6d0c633ec6905d2177f57a3f006d0860d0) |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Responsável de projeto — a formalizar |
| **Aprovador** | Pendente de baseline e gates formais |
| **Origem** | Plano diretor, requisitos e arquitetura proposta |
| **Autoridade superior** | [GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA); [Plano diretor](PLANO_DIRETOR.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | docs/PLANO_DIRETOR.md; docs/REQUISITOS.md; docs/ARQUITETURA.md; STATUS.md |

## Autoridade do roadmap

Este ficheiro é uma versão auxiliar/legada do plano de fases. A fonte canónica do roadmap é [GESTAO_PROJETO/ROADMAP.md](../GESTAO_PROJETO/ROADMAP.md). Em caso de divergência, prevalece a fonte canónica e o estado confirmado em STATUS.md. O conteúdo abaixo é preservado como histórico de planeamento e não deve ser usado para inferir aprovação de gate.

## 1. Estado atual verificável

A documentação base foi consultada no branch `main`. Não foi apresentada evidência de código funcional, CI executada, testes de aplicação, deployment, revisão clínica formal ou monitorização em produção. O projeto não pode ser descrito como aplicação implementada.

## 2. Fases

| Fase | Estado | Trabalho | Evidência de saída |
|---|---|---|---|
| F0 — Governação | EM_CURSO | Propósito, âmbito, owner, autoridade, decisões e baseline | G0/G1 registados e documentação revista |
| F1 — Conteúdo científico | PROPOSTO | Fontes primárias, matriz de afirmações e artigos piloto | Conteúdo com revisão identificável |
| F2 — Arquitetura e privacidade | PROPOSTO | Stack, fluxos, ameaças, classificação e retenção | Desenho aprovado em G2 |
| F3 — MVP educativo | BLOQUEADO | Artigos, pesquisa, fontes e acessibilidade após G2 | Build reprodutível e testes aprovados |
| F4 — Dados pessoais opcionais | BLOQUEADO | Apenas após avaliação e aprovação próprias | Requisitos, segurança, privacidade e UX aprovados |
| F5 — Qualidade e segurança | PROPOSTO | Testes, acessibilidade, revisão clínica e segurança | Relatórios e defeitos críticos tratados |
| F6 — Piloto/lançamento | BLOQUEADO | Operações, suporte, recuperação e autorização | G4/G5 aprovados e piloto registado |
| F7 — Evolução | FUTURO | Integrações e capacidades avançadas avaliadas separadamente | Novo G1/G2 por capacidade |

## 3. Sequência imediata

1. Confirmar finalidade e público do MVP.
2. Formalizar responsáveis técnico, editorial/clínico e de privacidade.
3. Completar requisitos com IDs e critérios mensuráveis.
4. Decidir entre conteúdo estático versionado e aplicação PHP/framework.
5. Desenhar fluxos de dados, fronteiras de confiança, ameaças e testes.
6. Registar decisão e aprovação G2 antes de escrever código funcional.

## 4. Regras de progresso

Documento não equivale a implementação; diretório não equivale a componente operacional; teste planeado não equivale a teste executado; workflow não equivale a CI validada; fase não está concluída sem evidência e decisão formal. Bloqueios ficam visíveis em STATUS.md.

## 5. Próxima ação

Fechar F0 e criar matriz requisito → componente → teste → gate. Até então, a implementação funcional permanece bloqueada.

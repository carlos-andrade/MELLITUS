# ADR-001 — Arquitetura estática para o MVP MELLITUS

| Campo | Valor |
|---|---|
| **ID** | MEL-ADR-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | ADR |
| **Fase** | G2 — Arquitetura e privacidade |
| **Estado** | PROPOSTO — decisão pronta para ratificação, não aprovada |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | 1aeb43ada667ba7213e2aed75b54a2eeb2be629931f8a4ca270eea0228cd24ff |
| **Commit de referência (versão anterior)** | N/A — documento inicial G2 |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Carlos Andrade — responsável de produto; responsável técnico a designar |
| **Aprovador** | Pendente de aprovação G2 |
| **Origem** | G0/G1 aprovados; autorização limitada para preparação e avaliação de G2 |
| **Autoridade superior** | [GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA); [Constituição](https://github.com/carlos-andrade/GOVERNANCA/blob/main/CONSTITUICAO.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | [arquitetura](../ARQUITETURA.md); [ameaças](../AMEACAS.md); [triagem de privacidade](../AVALIACAO_PRIVACIDADE_MVP.md) |

## Estado

Proposta. Este ADR regista uma recomendação, não autorização para implementar, escolher fornecedor ou publicar.

## Contexto

O MVP aprovado em D1–D8 é um diretório estático de links oficiais, sem conteúdo clínico próprio, contas, perfis ou dados de saúde. O orçamento permanece UNKNOWN e não há autorização para compromissos financeiros.

## Decisão proposta

Adotar páginas estáticas geradas a partir de catálogo versionado em Git, com HTML semântico, CSS responsivo e JavaScript mínimo para pesquisa local. Não usar backend, API, base de dados, autenticação, uploads, formulários, analytics, cookies próprios, publicidade, pixels ou recursos remotos de terceiros no MVP-base.

O fornecedor de alojamento não é decidido neste ADR. A escolha exige análise de termos, logs, localização, subprocessadores, segurança, recuperação e custos. Publicação e CI/CD ficam fora do mandato atual.

## Alternativas

| Alternativa | Vantagens | Desvantagens/riscos | Resultado |
|---|---|---|---|
| Site estático versionado | Menor superfície de ataque; sem dados submetidos; alterações rastreáveis; fácil exportação | Logs do alojamento ainda por avaliar | Preferida para avaliação |
| Aplicação com backend e base de dados | Flexibilidade dinâmica | Mais componentes, atualizações, segurança, logs e risco sem necessidade demonstrada | Não justificada |
| CMS alojado | Edição amigável | Plugins, superfície de ataque, cookies/telemetria e dependência variável | Não justificada |

## Consequências

Catálogo estruturado e versionado; pesquisa local se necessária; nenhuma recolha de dados de saúde ou perfis; apenas metadados e links oficiais; testes de links, domínios, avisos, acessibilidade e ausência de trackers antes do lançamento. Alojamento e análise de logs/privacidade continuam bloqueadores. G2 não é aprovado por este documento; não há autorização de construção.

## Condições para ratificação

1. Fechar PR-01 a PR-03 em docs/AVALIACAO_PRIVACIDADE_MVP.md.
2. Confirmar modelo de publicação sem assumir custos não autorizados.
3. Ratificar explicitamente este ADR e o pacote G2.
4. Só depois abrir/autorizar G3 por decisão própria.

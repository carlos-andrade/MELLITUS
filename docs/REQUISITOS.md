# Requisitos iniciais — MELLITUS

| Campo | Valor |
|---|---|
| **ID** | MEL-REQ-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | ESPECIFICACAO |
| **Fase** | F0 — Governação e requisitos |
| **Estado** | APROVADO — baseline funcional do MVP estático (G0/G1) |
| **Versão** | 1.2.0 |
| **SHA-256 (conteúdo canónico)** | fe6b1e124f439993f0d66f948adededd9d6cd8bdfa321fc977d4c5346cc16830 |
| **Commit de referência (versão anterior)** | Histórico Git preservado; SHA do commit anterior não verificado nesta atualização |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Carlos Andrade — patrocinador e responsável de produto/projeto |
| **Aprovador** | Carlos Andrade — aprovação D1–D8 na issue #1 |
| **Origem** | Briefing inicial, sujeito a validação de viabilidade |
| **Autoridade superior** | [Constituição GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA/blob/main/CONSTITUICAO.md); [Norma de cabeçalho](https://github.com/carlos-andrade/GOVERNANCA/blob/main/CABE%C3%87ALHO/NORMA-CABECALHO-PADRAO.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | docs/PLANO_DIRETOR.md; docs/VALIDACAO.md; docs/RISCOS.md |
| **Escopo** | Requisitos funcionais, não funcionais e restrições |
| **Objetivo** | Construir uma baseline testável para o MVP e fases futuras |
| **Dependências** | Verificação de links/fontes, arquitetura e avaliação de privacidade aplicável |

## 1. Regras

Cada requisito recebe ID único. O estado inicial é proposta, não requisito aprovado. Requisitos críticos devem ser ligados a testes e evidências antes da aceitação.

## 2. Requisitos funcionais — MVP educativo

| ID | Requisito | Prioridade | Critério de aceitação | Estado |
|---|---|---|---|---|
| MEL-FR-001 | Disponibilizar catálogo navegável de ligações para páginas oficiais sobre diabetes, sem produzir conteúdo clínico próprio. | Alta | Cada registo aponta para página de entidade oficial e identifica a fonte externa. | APROVADO — baseline G0/G1 |
| MEL-FR-002 | Apresentar entidade, título, URL, jurisdição/idioma e data de verificação de cada ligação externa. | Alta | Metadados preenchidos e ligação testada, com data registada. | PROPOSTO |
| MEL-FR-003 | Permitir navegação por temas e pesquisa de conteúdo. | Alta | Testes funcionais de navegação e pesquisa aprovados. | PROPOSTO |
| MEL-FR-004 | Explicar que o MELLITUS é um diretório de fontes externas e não valida nem substitui aconselhamento clínico. | Alta | Aviso visível na página inicial e junto dos resultados; teste de presença aprovado. | PROPOSTO |
| MEL-FR-005 | Permitir consulta em ecrãs móveis e desktop. | Alta | Testes nos ecrãs suportados sem bloqueios críticos. | PROPOSTO |
| MEL-FR-006 | Permitir manutenção, correção e remoção rastreável de registos de fontes e ligações. | Alta | Alterações de registos com histórico, autor e data. | PROPOSTO |

## 3. Requisitos de acompanhamento — fase futura

| ID | Requisito | Prioridade | Critério de aceitação | Estado |
|---|---|---|---|---|
| MEL-FR-101 | Permitir registo voluntário de medições e observações aprovadas no âmbito. | Alta | Permissões, validação e testes demonstrados antes do piloto. | BLOQUEADO — fora do MVP; nova decisão G1/G2 exigida |
| MEL-FR-102 | Mostrar histórico e gráficos sem alegações diagnósticas automáticas. | Alta | Resultados conferem com dados de teste e limites são visíveis. | BLOQUEADO_ATÉ_G2 |
| MEL-FR-103 | Permitir exportar os próprios dados num formato documentado. | Média | Exportação validada e autorizada, sem dados de terceiros. | BLOQUEADO_ATÉ_G2 |
| MEL-FR-104 | Permitir pedido de eliminação quando aplicável, considerando políticas de retenção e cópias de segurança. | Alta | Fluxo documentado e testado. | BLOQUEADO_ATÉ_G2 |

## 4. Requisitos não funcionais

| ID | Domínio | Requisito | Critério de aceitação | Estado |
|---|---|---|---|---|
| MEL-NFR-001 | Segurança | Autorização no servidor e princípio do menor privilégio. | Testes de acesso não autorizado passam. | PROPOSTO |
| MEL-NFR-002 | Privacidade | Definir finalidade, base legal, minimização, retenção e direitos. | Avaliação documentada antes de recolher dados de saúde. | PROPOSTO |
| MEL-NFR-003 | Auditoria | Alterações relevantes e acessos administrativos são rastreáveis. | Logs úteis sem segredos ou excesso de dados pessoais. | PROPOSTO |
| MEL-NFR-004 | Acessibilidade | Avaliar WCAG 2.2 AA como objetivo de desenho, sujeito à aplicabilidade legal. | Auditoria automática e manual documentadas. | PROPOSTO |
| MEL-NFR-005 | Resiliência | Definir backups, recuperação e rollback antes de produção. | Recuperação testada e resultados registados. | PROPOSTO |
| MEL-NFR-006 | Observabilidade | Métricas, logs e alertas proporcionais ao risco. | Cenários de falha testados; ausência de monitorização não conta como sucesso. | PROPOSTO |
| MEL-NFR-007 | Proveniência de fontes | Distinguir informação do catálogo de conteúdo externo; não produzir afirmações clínicas próprias. | Auditoria confirma fonte identificada, link e ausência de texto clínico editorial próprio. | PROPOSTO |
| MEL-NFR-008 | Portabilidade | Permitir exportação de dados pessoais quando aplicável. | Formato e limitações documentados. | PROPOSTO |

## 5. Exclusões explícitas

- Diagnóstico automático.
- Recomendação autónoma de doses ou ajuste de medicação.
- Afirmar que uma medição isolada confirma ou exclui doença.
- Uso de dados reais de saúde em testes sem base legal e controlos apropriados.
- Redação, resumo, tradução, interpretação ou recomendação clínica própria enquanto não existir revisor clínico.
- Reprodução extensa de conteúdo de terceiros; o MVP deve ligar diretamente às páginas de origem.

## 6. Rastreabilidade e próxima ação

Ligar cada requisito a riscos, decisões, implementação e testes. Não reutilizar IDs eliminados. Após triagem G0/G1, aprovar o âmbito do MVP e converter os requisitos selecionados em casos de teste. Até lá, os requisitos ficam em proposta ou revisão.


## 7. Restrição de escopo decorrente da decisão de não nomear revisor clínico — 2026-10-15

O proprietário declarou que não haverá revisor clínico. Como consequência de segurança, a baseline proposta para o MVP limita-se a um diretório de páginas de entidades oficiais, com ligações diretas e metadados de origem. O projeto não redigirá, resumirá, traduzirá, interpretará nem recomendará conteúdo clínico. A inclusão no catálogo não equivale a validação clínica da página externa. Cada ligação deverá ter data de verificação. Esta alteração de âmbito permanece proposta até ratificação formal G0/G1. Os requisitos de registos pessoais continuam bloqueados e fora do MVP.


## 7. Adenda G2 — 2026-10-15

A baseline aprovada para o MVP é um diretório estático de links e metadados oficiais. Requisitos de acompanhamento pessoal (MEL-FR-101 a MEL-FR-104) continuam bloqueados e não são autorizados pela aprovação G2 de arquitetura. O desenho não prevê contas, formulários, backend, base de dados, analytics ou recolha de dados de saúde. Ver [pacote G2](../GESTAO_PROJETO/PACOTE_G2_ARQUITETURA_PRIVACIDADE.md).

# Requisitos iniciais — MELLITUS

| Campo | Valor |
|---|---|
| **ID** | MEL-REQ-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | ESPECIFICACAO |
| **Fase** | F0 — Governação e requisitos |
| **Estado** | EM_REVISAO |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | PENDENTE_DE_CALCULO_VERIFICADO |
| **Commit de referência (versão anterior)** | N/A — documento inicial |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Responsável de produto — a formalizar |
| **Aprovador** | Pendente de aprovação formal |
| **Origem** | Briefing inicial, sujeito a validação de viabilidade |
| **Autoridade superior** | [Constituição GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA/blob/main/CONSTITUICAO.md); [Norma de cabeçalho](https://github.com/carlos-andrade/GOVERNANCA/blob/main/CABE%C3%87ALHO/NORMA-CABECALHO-PADRAO.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | docs/PLANO_DIRETOR.md; docs/VALIDACAO.md; docs/RISCOS.md |
| **Escopo** | Requisitos funcionais, não funcionais e restrições |
| **Objetivo** | Construir uma baseline testável para o MVP e fases futuras |
| **Dependências** | Revisão clínica, arquitetura e avaliação de privacidade |

## 1. Regras

Cada requisito recebe ID único. O estado inicial é proposta, não requisito aprovado. Requisitos críticos devem ser ligados a testes e evidências antes da aceitação.

## 2. Requisitos funcionais — MVP educativo

| ID | Requisito | Prioridade | Critério de aceitação | Estado |
|---|---|---|---|---|
| MEL-FR-001 | Apresentar conteúdo educativo sobre diabetes em linguagem adequada ao público geral. | Alta | Conteúdo piloto revisto e aceite por revisor qualificado. | PROPOSTO |
| MEL-FR-002 | Mostrar fontes verificáveis e data de revisão em cada artigo publicado. | Alta | Artigos piloto com referências e metadados completos. | PROPOSTO |
| MEL-FR-003 | Permitir navegação por temas e pesquisa de conteúdo. | Alta | Testes funcionais de navegação e pesquisa aprovados. | PROPOSTO |
| MEL-FR-004 | Mostrar limites da plataforma e aviso de que não substitui aconselhamento clínico. | Alta | Aviso visível nos pontos relevantes e verificado por teste. | PROPOSTO |
| MEL-FR-005 | Permitir consulta em ecrãs móveis e desktop. | Alta | Testes nos ecrãs suportados sem bloqueios críticos. | PROPOSTO |
| MEL-FR-006 | Permitir correção, atualização, despublicação e revisão editorial rastreáveis. | Alta | Fluxo demonstrado com versões e auditoria. | PROPOSTO |

## 3. Requisitos de acompanhamento — fase futura

| ID | Requisito | Prioridade | Critério de aceitação | Estado |
|---|---|---|---|---|
| MEL-FR-101 | Permitir registo voluntário de medições e observações aprovadas no âmbito. | Alta | Permissões, validação e testes demonstrados antes do piloto. | BLOQUEADO_ATÉ_G2 |
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
| MEL-NFR-007 | Integridade científica | Ligar conteúdo clínico a fontes e revisão datada. | Auditoria de amostra sem afirmações críticas sem suporte. | PROPOSTO |
| MEL-NFR-008 | Portabilidade | Permitir exportação de dados pessoais quando aplicável. | Formato e limitações documentados. | PROPOSTO |

## 5. Exclusões explícitas

- Diagnóstico automático.
- Recomendação autónoma de doses ou ajuste de medicação.
- Afirmar que uma medição isolada confirma ou exclui doença.
- Uso de dados reais de saúde em testes sem base legal e controlos apropriados.
- Publicação de conteúdo clínico sem fonte e revisão necessárias.

## 6. Rastreabilidade e próxima ação

Ligar cada requisito a riscos, decisões, implementação e testes. Não reutilizar IDs eliminados. Após triagem G0/G1, aprovar o âmbito do MVP e converter os requisitos selecionados em casos de teste. Até lá, os requisitos ficam em proposta ou revisão.

# Registo de riscos — MELLITUS

| Campo | Valor |
|---|---|
| **ID** | MEL-RSK-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | REGISTO_RISCOS |
| **Fase** | F0 — Governação e requisitos |
| **Estado** | EM_REVISAO |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | aa725ccef21bf5972506562ca3bd42560332601cab27010020f623f629481162 |
| **Commit de referência (versão anterior)** | N/A — documento inicial |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Responsável de risco — a formalizar |
| **Aprovador** | Pendente de aprovação formal |
| **Origem** | Triagem preliminar do domínio saúde digital; não substitui avaliação formal |
| **Autoridade superior** | [Constituição GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA/blob/main/CONSTITUICAO.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | docs/PLANO_DIRETOR.md; docs/REQUISITOS.md; docs/VALIDACAO.md |
| **Escopo** | Riscos clínicos, dados, software, operação e conformidade |
| **Objetivo** | Identificar riscos e exigir tratamento antes dos gates aplicáveis |
| **Dependências** | Avaliação clínica, técnica e de privacidade |

## Escala preliminar

Probabilidade e impacto são qualitativos e provisórios. Devem ser revistos após análise contextual. Risco residual não se presume aceitável sem responsável e decisão documentada.

| ID | Risco | Probabilidade | Impacto | Tratamento inicial | Responsável | Estado |
|---|---|---|---|---|---|---|
| MEL-R-001 | Conteúdo incorreto ou desatualizado pode atrasar procura de cuidados. | Média | Crítico | Fontes rastreáveis, revisão clínica, datas e processo de correção/retirada. | Revisor clínico a nomear | ABERTO |
| MEL-R-002 | Utilizador interpreta conteúdo como diagnóstico ou prescrição. | Média | Crítico | Limites explícitos, UX clara, testes de compreensão e exclusão de prescrição automática. | Produto + clínico | ABERTO |
| MEL-R-003 | Exposição de dados de saúde por falha de acesso ou configuração. | Média | Crítico | Minimização, autorização, cifragem apropriada, revisão de ameaças e resposta a incidentes. | Segurança/privacidade a nomear | ABERTO |
| MEL-R-004 | Falta de base legal, transparência ou gestão dos direitos dos titulares. | Média | Alto | Avaliação jurídica, política clara e análise da necessidade de AIPD/DPIA. | Privacidade/jurídico | ABERTO |
| MEL-R-005 | Funções futuras podem ser enquadradas como dispositivo médico ou IA regulada sem avaliação. | Média | Alto | Avaliar finalidade e funções antes de desenvolver/publicar. | Conformidade a nomear | ABERTO |
| MEL-R-006 | Falha de backup, recuperação, monitorização ou resposta operacional. | Média | Alto | Runbooks, restauro testado, alertas com confirmação e supervisão independente quando justificada. | Operações a nomear | ABERTO |
| MEL-R-007 | Conteúdo estigmatizante, inacessível ou incompreensível. | Média | Médio | Revisão editorial, linguagem inclusiva, testes com utilizadores e acessibilidade. | Editorial/UX | ABERTO |
| MEL-R-008 | Progresso ou conformidade declarados sem evidência. | Média | Alto | Estados controlados, rastreabilidade, gates e auditoria conforme GOVERNANCA. | Responsável de projeto | MITIGAÇÃO_PROPOSTA |
| MEL-R-009 | Dados de testes expõem pessoas ou são reutilizados indevidamente. | Baixa a média | Crítico | Dados sintéticos por defeito; aprovação antes de dados reais. | Segurança/privacidade | ABERTO |
| MEL-R-010 | Dependências externas ou APIs mudam ou ficam indisponíveis. | Média | Médio | Inventário, versões, contratos, fallback e testes. | Responsável técnico | ABERTO |

## Regras de tratamento

Riscos críticos não podem ser ignorados em lançamento. A aceitação de risco residual exige dono, justificação, controlos, validade e autoridade competente. Exceções não dispensam obrigações legais ou contratuais. Reavaliar após incidentes, novas classes de dados, integrações ou mudanças de finalidade.

## Próxima ação

Nomear responsáveis, rever classificação e ligar cada risco a requisitos, testes e gates.

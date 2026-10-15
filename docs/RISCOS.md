# Registo de riscos — MELLITUS

| Campo | Valor |
|---|---|
| **ID** | MEL-RSK-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | REGISTO_RISCOS |
| **Fase** | F0 — Governação e requisitos |
| **Estado** | EM_REVISAO — riscos G2 atualizados; aceitação residual pendente |
| **Versão** | 1.1.0 |
| **SHA-256 (conteúdo canónico)** | 2da982d8e31e9a07466a7c8b69adebbf73094cb17ecdc9a77d0bb4e4d5005590 |
| **Commit de referência (versão anterior)** | Histórico Git preservado; SHA do commit anterior não verificado nesta atualização |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Carlos Andrade — responsável de produto; responsáveis técnicos especializados a designar |
| **Aprovador** | Pendente de decisão G2 |
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
| MEL-R-001 | Ligações externas desatualizadas, quebradas ou encaminhadas para fonte inadequada podem induzir confiança indevida. | Média | Alto | Catálogo restrito a entidades oficiais, verificação de domínio/destino, data de verificação, remoção rápida e aviso de fonte externa; sem validação clínica própria. | Responsável pelo catálogo — a formalizar | ABERTO |
| MEL-R-002 | Utilizador interpreta o diretório como recomendação médica ou validação clínica das fontes externas. | Média | Alto | Aviso visível de que o catálogo não presta aconselhamento nem valida o conteúdo externo; não produzir artigos, resumos ou recomendações clínicas próprias. | Produto — responsável a formalizar | ABERTO |
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


## Restrição de âmbito — 2026-10-15

O proprietário decidiu que não haverá revisor clínico. O risco associado à ausência de revisão não é aceite para produção de conteúdo clínico próprio; a mitigação proposta é excluir esse conteúdo do MVP e limitar o produto a ligações diretas para fontes oficiais com metadados e data de verificação. A decisão não dispensa avaliação legal, segurança, privacidade nem os gates aplicáveis. A ratificação do âmbito reduzido continua pendente.


## Adenda G2 — 2026-10-15

Foram detalhados riscos em [docs/AMEACAS.md](AMEACAS.md) e [docs/AVALIACAO_PRIVACIDADE_MVP.md](AVALIACAO_PRIVACIDADE_MVP.md). Novo bloqueador: fornecedor/região de alojamento e respetivo tratamento de logs ainda desconhecidos; não se pode fechar a avaliação de privacidade nem aceitar risco residual antes de analisar termos, retenção, subprocessadores e transferências. O desenho sem dados de saúde de visitantes, sem contas e sem analytics reduz o risco, mas não elimina o possível tratamento de dados técnicos pelo alojamento. Riscos residuais não foram aceites.

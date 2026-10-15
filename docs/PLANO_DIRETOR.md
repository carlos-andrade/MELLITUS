# MELLITUS — Plano diretor do projeto

| Campo | Valor |
|---|---|
| **ID** | MEL-PLANO-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | PLANO |
| **Fase** | F0 — Governação e requisitos |
| **Estado** | EM_REVISAO |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | 249ca1313923f40e669c685659bf51509a9caca3d41bdfcc40aea99f35879dbd |
| **Commit de referência (versão anterior)** | N/A — documento inicial |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Responsável de projeto — a formalizar |
| **Aprovador** | Pendente de aprovação formal |
| **Origem** | Definições iniciais do projeto; sujeitas a gate formal |
| **Autoridade superior** | [Constituição GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA/blob/main/CONSTITUICAO.md); [Norma de cabeçalho](https://github.com/carlos-andrade/GOVERNANCA/blob/main/CABE%C3%87ALHO/NORMA-CABECALHO-PADRAO.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | README.md; GOVERNANCA/REGISTO_DECISOES.md; docs/REQUISITOS.md; docs/RISCOS.md; docs/VALIDACAO.md |
| **Escopo** | Plataforma educativa pública; acompanhamento pessoal futuro sob controlos específicos |
| **Objetivo** | Definir visão, entregáveis, fases, responsabilidades e critérios de passagem |
| **Dependências** | Fontes clínicas, revisor clínico, avaliação legal e de privacidade, equipa técnica |

## 1. Contexto e estado

O projeto pretende criar uma plataforma de informação e acompanhamento da diabetes para o público em geral. Este documento é uma proposta de baseline inicial, ainda em revisão; não prova equipa constituída, revisão clínica realizada, conformidade regulatória ou produto implementado.

## 2. Objetivos

1. Criar biblioteca educativa clara, referenciada e rastreável.
2. Explicar tipos de diabetes, sintomas, prevenção de complicações e opções de tratamento sem substituir uma consulta.
3. Estabelecer política editorial com fontes, datas de revisão, correções e retirada de conteúdo.
4. Avaliar registos pessoais opcionais apenas após análise de requisitos, minimização de dados, segurança e privacidade.
5. Disponibilizar meios adequados para consultar, exportar e, quando aplicável, eliminar dados.
6. Manter rastreabilidade entre requisitos, riscos, decisões, implementação, testes, versões e incidentes.

## 3. Princípios

- Evidência verificável antes de alegações.
- Segurança, privacidade e acessibilidade desde a conceção.
- Minimização de dados e separação de conteúdo público e dados pessoais.
- Revisão humana proporcional ao risco.
- Funcionalidades clínicas não entram em produção sem avaliação clínica e regulatória apropriada.
- Monitorização proporcional ao risco conforme o padrão WATCHDOG da GOVERNANCA; integração exige testes próprios.

## 4. Escopo inicial

### Incluído no planeamento

- Website educativo responsivo.
- Estrutura editorial e catálogo de fontes.
- Pesquisa e navegação.
- Referências por artigo e data de revisão.
- Avaliação posterior de registo pessoal opcional.
- Documentação, testes, segurança, privacidade, recuperação e operação.

### Excluído do MVP

- Diagnóstico ou triagem autónoma conclusiva.
- Prescrição ou ajuste autónomo de insulina ou outra medicação.
- Decisões terapêuticas automatizadas.
- Alegações clínicas preditivas sem evidência adequada.
- Integração com dispositivos antes de validar finalidade, compatibilidade e segurança.
- Dados reais de saúde em testes sem base legal e controlos adequados.

## 5. Roadmap e gates

| Fase | Atividades | Entregáveis | Gate de saída |
|---|---|---|---|
| F0 — Governação e requisitos | Charter, âmbito, donos, requisitos, riscos, dependências | Documentos fundacionais | G0/G1 aceites; responsáveis e critérios explícitos |
| F1 — Evidência clínica | Selecionar fontes, matriz de afirmações, política de revisão | Catálogo de fontes e conteúdos piloto revistos | Conteúdo piloto com referências e revisão identificável |
| F2 — Arquitetura e privacidade | Modelo de dados, ameaças, acessos, retenção, backups | Arquitetura e avaliação de riscos | G2 aceite; bloqueios identificados |
| F3 — MVP educativo | Páginas, navegação, pesquisa, referências, acessibilidade | Versão educativa testável | G3 aceite; requisitos críticos testados |
| F4 — Acompanhamento pessoal | Registo, histórico, visualizações e exportação | Módulo isolado e documentado | Aprovação de privacidade, segurança e usabilidade |
| F5 — Qualidade e validação | Testes funcionais, segurança, acessibilidade, revisão clínica | Relatórios e registo de defeitos | Sem bloqueios críticos; exceções formalizadas |
| F6 — Piloto e lançamento | Piloto limitado, suporte, observabilidade, rollback | Relatório de piloto e autorização | G4/G5 aprovados |
| F7 — Evolução e investigação | Estudo de dispositivos e funcionalidades avançadas | Estudo de viabilidade e avaliação de risco | Novo G1/G2 para cada capacidade material |

A GOVERNANCA define os gates G0–G6. Combinar gates requer justificação e não elimina obrigações legais ou controlos críticos.

## 6. Entregáveis

Cada entregável terá ID único, título, versão, estado, responsável, origem, autoridade, data, rastreabilidade, critérios de aceitação, evidências, histórico e aprovador quando exigido. Documentos Markdown seguem a norma de cabeçalho da GOVERNANCA.

## 7. Medição de progresso

O progresso é calculado com tarefas e evidências verificáveis. Documento redigido não equivale a fase aprovada; código não equivale a funcionalidade validada; workflow definido não equivale a monitorização operacional ativa. Ausência de dados deve ser `UNKNOWN`, não sucesso.

## 8. Critérios de aceitação

- Requisitos críticos rastreados a testes ou evidências.
- Conteúdo clínico com fonte verificável e revisão adequada.
- Testes críticos aprovados e defeitos bloqueadores resolvidos.
- Sem vulnerabilidades críticas/altas conhecidas sem tratamento aprovado na versão de lançamento.
- Privacidade, base legal, acesso, retenção e direitos documentados.
- Acessibilidade e usabilidade avaliadas.
- Recuperação, suporte, observabilidade e rollback testados antes de produção.
- Aprovação explícita para cada gate aplicável.

## 9. Riscos

Ver [docs/RISCOS.md](RISCOS.md). Riscos clínicos, de privacidade, cibersegurança e qualidade de fontes têm prioridade elevada.

## 10. Próxima ação

Completar F0: confirmar responsável e revisores, aprovar requisitos, classificar a iniciativa segundo GOVERNANCA e formalizar G0/G1. F0 permanece em curso até haver evidência e decisão registadas.

## 11. Histórico de alterações

| Versão | Data | Alteração | Responsável | Evidência |
|---|---|---|---|---|
| 1.0.0 | 2026-10-15 | Criação do plano diretor inicial | Responsável — a formalizar | Commit GitHub de criação |

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
| **SHA-256 (conteúdo canónico)** | 7cb4d722b4f51146ae6880d74a7fa3b0ef9998d75080edc14e9399d5f7c302e0 |
| **Commit de referência (versão anterior)** | [88f5fae105e4cd1a70c2fcff9d3d961ffd594ccc](https://github.com/carlos-andrade/MELLITUS/commit/88f5fae105e4cd1a70c2fcff9d3d961ffd594ccc) |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Responsável de qualidade — a formalizar |
| **Aprovador** | Pendente de aprovação formal |
| **Origem** | Plano inicial alinhado com os gates da GOVERNANCA |
| **Autoridade superior** | [Constituição GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA/blob/main/CONSTITUICAO.md); [Ciclo de vida e gates](https://github.com/carlos-andrade/GOVERNANCA/blob/main/docs/02-ciclo-de-vida/ciclo-de-vida-e-gates.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | docs/REQUISITOS.md; docs/RISCOS.md; docs/PLANO_DIRETOR.md; docs/MATRIZ_RASTREABILIDADE.md |
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
| MEL-GQ-02 | Catálogo de fontes oficiais com metadados e links verificados; ausência de conteúdo clínico próprio | Registos de fonte, data de verificação, teste de links e auditoria de texto publicado | Sim; conteúdo clínico próprio fica bloqueado sem revisão apropriada |
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
- Testes de links externos, domínios oficiais, metadados, datas e avisos de âmbito.
- Verificação de que o MVP não contém artigos, resumos, traduções, interpretações ou recomendações clínicas produzidas pelo projeto.
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


## 7. Auditoria documental F0

- Inventário do branch main: 36 ficheiros Markdown identificados.
- Os 36 ficheiros começam com título H1 e incluem os campos obrigatórios da norma.
- Os 36 hashes SHA-256 canónicos foram comparados com recálculo independente após normalização UTF-8/LF e exclusão das duas linhas de controlo; todos coincidem.
- Não foram encontrados campos de hash pendentes nem destinos inexistentes nos links relativos analisados.
- Os IDs documentais examinados são únicos.
- Matriz de rastreabilidade criada: docs/MATRIZ_RASTREABILIDADE.md.
- Issue de decisão G0/G1 reaberta após verificação: https://github.com/carlos-andrade/MELLITUS/issues/1. O comentário do proprietário regista aceitação geral, mas não supre evidência de responsáveis, revisão clínica qualificada, viabilidade ou decisão formal do gate.
- Nenhum gate G0–G6 é declarado aprovado; a implementação funcional permanece não demonstrada.


## 8. Verificação da issue G0/G1 — 2026-10-15

A issue #1 encontrava-se fechada com checklist integralmente assinalada, embora o corpo ainda declarasse G0/G1 pendente. O único comentário disponível era uma aceitação geral do proprietário. Para manter a integridade dos estados, a issue foi reaberta, a aceitação do âmbito foi registada separadamente e as pendências sem evidência foram desmarcadas. Resultado: aceitação parcial do âmbito; G0/G1 NÃO APROVADO. Esta verificação não altera o resultado de auditoria documental anterior nem demonstra implementação funcional.


## 9. Restrição de validação sem revisor clínico — 2026-10-15

O proprietário decidiu que não haverá revisor clínico. Assim, não se executará nem se alegará validação clínica de conteúdo próprio. A proposta de MVP limita-se a organizar ligações para fontes oficiais e metadados; os testes deverão verificar destino/entidade, data de verificação, aviso de fonte externa e ausência de conteúdo clínico editorial próprio. A validade clínica das páginas externas não é certificada pelo MELLITUS. A ratificação de âmbito e G0/G1 continuam pendentes.


## 10. Reauditoria após restrição de âmbito — 2026-10-15

A árvore atual contém 41 ficheiros (blobs), incluindo 37 Markdown. Comparação da árvore atual com a baseline auditada: 24 dos 36 Markdown anteriores permanecem inalterados; 12 Markdown foram alterados e um novo documento foi criado. Os 13 documentos alterados/criados foram submetidos a recálculo independente de SHA-256 canónico, com 13/13 correspondências. Os restantes 24 documentos mantêm os mesmos blobs da baseline cuja auditoria anterior confirmou os hashes. A decisão do proprietário de não nomear revisor clínico foi registada; o âmbito reduzido para catálogo de fontes oficiais permanece PROPOSTO, G0/G1 continua NÃO APROVADO e a implementação funcional continua não demonstrada.


## 11. Verificação inicial de portais oficiais — 2026-10-15

Foi feita verificação técnica dos oito portais candidatos listados em CLINICA/CATALOGO_FONTES.md. Resultado observado: 6 PASS, 1 WARN (SNS 24 sem conteúdo textual extraído) e 1 UNKNOWN (NICE não confirmado nesta execução). Esta verificação limita-se ao acesso aos portais-raiz; não valida páginas temáticas, conteúdo clínico, atualidade científica nem a adequação das fontes para afirmações específicas. A implementação funcional continua não demonstrada e G0/G1 permanece pendente.


## Execução adicional — verificação de fontes e controlo de governação — 2026-10-15

- SNS 24: PASS técnico para resposta do portal; a interface indica dependência de JavaScript. A verificação não atesta conteúdo clínico.
- NICE: UNKNOWN para validação direta do portal-raiz, porque a consulta automatizada recebeu HTTP 403. Não inferir indisponibilidade. Página oficial temática NG28 localizada; título, URL e última atualização indicada (18-02-2026) registados no catálogo. Também foram localizadas páginas oficiais temáticas da DGS (Diabetes; Relatórios e Publicações) e ADA (About Diabetes), com títulos e URLs registados.
- Catálogo: estado técnico consolidado de 7 PASS, 0 WARN e 1 UNKNOWN para oito portais-raiz. A página temática NICE é uma evidência separada e não altera o estado do portal-raiz.
- Issue #1: corrigidas seis caixas indevidamente assinaladas como concluídas. Mantêm-se pendentes aprovação do âmbito, baseline aprovada, nomeação de responsáveis, viabilidade/custos/riscos, decisão formal G0/G1 e decisão de passagem a G2.
- Resultado: correção documental executada; G0/G1 continuam NÃO APROVADOS; implementação funcional comprovada permanece 0%. Não foram executados testes de runtime porque não há aplicação funcional verificada.
# Catálogo de fontes oficiais — MELLITUS

| Campo | Valor |
|---|---|
| **ID** | MEL-CLIN-SOURCES-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | CATALOGO_FONTES |
| **Fase** | F1 — Catálogo de fontes oficiais |
| **Estado** | PROPOSTO |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | e84258edf7fa71cc1c0aacc46db10c1d79a3b9ffb4af3791a2a2d3463891481d |
| **Commit de referência (versão anterior)** | N/A — documento inicial |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Responsável pelo catálogo — a formalizar |
| **Aprovador** | Pendente de ratificação G0/G1 |
| **Origem** | Plano diretor e política editorial |
| **Autoridade superior** | [GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA); [política editorial](FONTES_E_REVISAO.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |

## Finalidade

Organizar ligações diretas para páginas de entidades oficiais. O catálogo não certifica validade clínica, atualidade científica ou adequação individual do conteúdo externo.

## Entidades candidatas

| Entidade | Portal oficial | Aplicação pretendida |
|---|---|---|
| Direção-Geral da Saúde (DGS) | https://www.dgs.pt/ | Recomendações nacionais e normas |
| SNS 24 | https://www.sns24.gov.pt/ | Informação pública de saúde em Portugal |
| INFARMED | https://www.infarmed.pt/ | Informação regulamentar e medicamentos em Portugal |
| Agência Europeia de Medicamentos (EMA) | https://www.ema.europa.eu/ | Autorizações e documentação europeia |
| Organização Mundial da Saúde (OMS) | https://www.who.int/ | Orientações globais |
| International Diabetes Federation (IDF) | https://idf.org/ | Relatórios e consensos |
| American Diabetes Association (ADA) | https://diabetes.org/ | Standards of Care e informação |
| European Association for the Study of Diabetes (EASD) | https://www.easd.org/ | Diretrizes e consensos |
| National Institute for Health and Care Excellence (NICE) | https://www.nice.org.uk/ | Diretrizes e avaliação de tecnologias |

### Verificação técnica dos portais-raiz — 2026-10-15

Esta verificação avalia apenas o acesso ao portal-raiz, não o conteúdo clínico nem páginas temáticas específicas.

| Portal | Resultado observado | Estado |
|---|---|---|
| DGS | Página carregada; navegação inclui área/programa de Diabetes | PASS — portal acessível |
| SNS 24 | Título identificado, mas conteúdo textual não foi extraído | WARN — confirmar manualmente |
| INFARMED | Página institucional carregada | PASS — portal acessível |
| EMA | Redirecionou para /en/homepage | PASS — redirecionamento funcional |
| OMS/WHO | Página institucional carregada | PASS — portal acessível |
| IDF | Página institucional carregada | PASS — portal acessível |
| EASD | Redirecionou para /home/ | PASS — redirecionamento funcional |
| NICE | Erro interno na ferramenta de consulta; resposta não confirmada | UNKNOWN — não marcar como validado |

Resumo: 6 PASS, 1 WARN, 1 UNKNOWN. Confirmar manualmente SNS 24 e NICE e verificar URLs temáticas individuais antes de as publicar no catálogo. Um portal acessível não prova atualidade nem correção clínica.

## Metadados mínimos por registo

Guardar ID estável, entidade, título, URL, domínio, tema de navegação, jurisdição/idioma, data de verificação, estado técnico, aviso de fonte externa e histórico de alterações. Não incluir alegações clínicas próprias nem campo de aprovação por revisor clínico.

## Limites

O proprietário declarou que não haverá revisor clínico. Ficam excluídos do MVP artigos, resumos, traduções, interpretações e recomendações clínicas próprias, bem como dados pessoais de saúde. A presença de uma URL nesta lista não significa que uma página específica tenha sido verificada. Links ativos não comprovam atualidade ou correção clínica.

## Próxima ação

Ratificar o âmbito reduzido em G0/G1 e, depois, verificar URLs individuais com evidência datada. Não declarar F1 concluída apenas por existir esta lista.

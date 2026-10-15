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
| **SHA-256 (conteúdo canónico)** | 5693f5e04b17a9422e8df1f674c600754d8ee79736cbf65ce4f5b10f3cd6938b |
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
| SNS 24 | Portal oficial respondeu; a página inicial indica que é uma aplicação web que requer JavaScript; o índice de pesquisa também apresenta a página oficial | PASS — acesso técnico confirmado, renderização depende de JavaScript |
| INFARMED | Página institucional carregada | PASS — portal acessível |
| EMA | Redirecionou para /en/homepage | PASS — redirecionamento funcional |
| OMS/WHO | Página institucional carregada | PASS — portal acessível |
| IDF | Página institucional carregada | PASS — portal acessível |
| EASD | Redirecionou para /home/ | PASS — redirecionamento funcional |
| NICE | O acesso automatizado ao portal-raiz devolveu HTTP 403; não prova indisponibilidade. Página oficial temática NG28 localizada e indexada, atualizada em 18-02-2026 | UNKNOWN — portal-raiz não validado diretamente; página temática localizada |

Resumo atualizado: 7 PASS, 0 WARN, 1 UNKNOWN. O SNS 24 responde, mas a interface exige JavaScript. Para o NICE, a raiz não pôde ser validada diretamente por consulta automatizada; isso não significa que esteja indisponível. Uma página temática oficial foi localizada abaixo. Um portal acessível não prova atualidade nem correção clínica.

## Páginas temáticas localizadas — 2026-10-15

As páginas abaixo foram localizadas em pesquisa e identificadas como pertencentes ao domínio oficial. A verificação é técnica/editorial (existência, título, URL e data indicada pela entidade); não é revisão clínica, validação de recomendações ou confirmação de adequação individual.

| Entidade | Título publicado pela entidade | URL direta | Evidência observada | Estado |
|---|---|---|---|---|
| NICE | Type 2 diabetes in adults: management — Blood glucose management (NG28) | https://www.nice.org.uk/guidance/ng28/chapter/Blood-glucose-management | Página oficial indexada; data de publicação indicada: 02-12-2015; última atualização indicada: 18-02-2026 | PASS — existência e metadados técnicos confirmados |
| DGS | Diabetes | https://www.dgs.pt/paginas-de-sistema/saude-de-a-a-z/diabetes.aspx | Página oficial indexada com título “Diabetes” e referência ao Programa Nacional para a Diabetes | PASS — existência e metadados técnicos confirmados |
| DGS | Programa Nacional para a Diabetes — Relatórios e Publicações | https://www.dgs.pt/programa-nacional-para-a-diabetes/relatorios-e-publicacoes.aspx | Página oficial indexada; lista relatórios e publicações, incluindo material de 2025 e 2024 | PASS — existência e metadados técnicos confirmados |
| ADA | About Diabetes | https://diabetes.org/about-diabetes | Página oficial indexada; título “About Diabetes” e conteúdo introdutório identificado | PASS — existência e metadados técnicos confirmados |

Não foi ainda localizada uma página temática individual do SNS 24 sobre diabetes com evidência suficiente para registo. Não preencher por inferência.

## Metadados mínimos por registo

Guardar ID estável, entidade, título, URL, domínio, tema de navegação, jurisdição/idioma, data de verificação, estado técnico, aviso de fonte externa e histórico de alterações. Não incluir alegações clínicas próprias nem campo de aprovação por revisor clínico.

## Limites

O proprietário declarou que não haverá revisor clínico. Ficam excluídos do MVP artigos, resumos, traduções, interpretações e recomendações clínicas próprias, bem como dados pessoais de saúde. A presença de uma URL nesta lista não significa que uma página específica tenha sido verificada. Links ativos não comprovam atualidade ou correção clínica.

## Próxima ação

Ratificar o âmbito reduzido em G0/G1 e, depois, verificar URLs individuais com evidência datada. Não declarar F1 concluída apenas por existir esta lista.

# MELLITUS

| Campo | Valor |
|---|---|
| **ID** | MEL-README-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | README |
| **Fase** | F0 — Governação e requisitos |
| **Estado** | EM_REVISAO |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | fa4dada48acb3a4a88149aff1c828152c81bf1f2a93abe419e5eb61db26ff4bb |
| **Commit de referência (versão anterior)** | [462c618f239e31d351723ac06d899fc5ca8f4d24](https://github.com/carlos-andrade/MELLITUS/commit/462c618f239e31d351723ac06d899fc5ca8f4d24) |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Responsável do projeto — a formalizar |
| **Aprovador** | Pendente de aprovação formal |
| **Origem** | Briefing inicial e plano diretor do projeto |
| **Autoridade superior** | [Constituição GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA/blob/main/CONSTITUICAO.md); [Norma de cabeçalho](https://github.com/carlos-andrade/GOVERNANCA/blob/main/CABE%C3%87ALHO/NORMA-CABECALHO-PADRAO.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | docs/PLANO_DIRETOR.md; GOVERNANCA/REGISTO_DECISOES.md; STATUS.md |
| **Escopo** | MVP proposto: diretório de fontes oficiais sobre diabetes; sem conteúdo clínico próprio nem dados pessoais de saúde |
| **Objetivo** | Criar uma plataforma acessível, segura e auditável apoiada em fontes clínicas rastreáveis |
| **Dependências** | Verificação de links/fontes, avaliação de privacidade aplicável, responsabilidades e aprovação G0/G1 |

## Visão

O MELLITUS está a ser preparado como diretório digital de fontes oficiais sobre diabetes, com pesquisa, navegação, ligações diretas e metadados. O proprietário decidiu que não haverá revisor clínico; por isso, o MVP proposto não produzirá artigos, resumos, traduções, interpretações ou recomendações clínicas próprias. O acompanhamento pessoal permanece fora do MVP e bloqueado até gates próprios.

## Objetivos

- Facilitar a descoberta de páginas de entidades oficiais sobre diabetes.
- Identificar entidade, título, URL, jurisdição/idioma e data de verificação do link.
- Não produzir conteúdo clínico próprio nem apresentar páginas externas como validadas pelo MELLITUS.
- Avaliar registos pessoais apenas depois de definidos requisitos, riscos e controlos próprios.
- Permitir controlo adequado dos dados pessoais, incluindo acesso, exportação e eliminação conforme aplicável.
- Manter decisões, versões, testes, incidentes e aprovações auditáveis.

## Limites de segurança

- O MELLITUS não substitui profissionais de saúde nem serviços de emergência.
- Não diagnostica nem exclui a possibilidade de doença.
- Não prescreve nem recomenda alterações autónomas de doses de insulina ou de outra medicação.
- O MVP não produzirá conteúdo clínico próprio, resumos, traduções, interpretações ou recomendações, porque não haverá revisor clínico.
- As ligações externas são fontes de terceiros; a inclusão no catálogo não constitui validação clínica pelo MELLITUS.
- Funcionalidades potencialmente enquadradas como dispositivo médico ou sistema de IA regulado ficam bloqueadas até avaliação adequada.

## Roadmap

| Fase | Nome | Resultado esperado |
|---|---|---|
| F0 | Governação e requisitos | Charter, âmbito, responsáveis, riscos, requisitos e gates |
| F1 | Catálogo de fontes oficiais | Links e metadados verificados; sem conteúdo clínico próprio |
| F2 | Arquitetura e proteção de dados | Arquitetura, modelo de dados, ameaças e controlos |
| F3 | MVP diretório de fontes | Pesquisa, navegação acessível, links oficiais e metadados |
| F4 | Acompanhamento pessoal | Registos opcionais, histórico, tendências e exportação |
| F5 | Testes e validação | Evidências de qualidade, links, acessibilidade, privacidade e segurança |
| F6 | Piloto e lançamento | Piloto, correções e autorização de publicação |
| F7 | Evolução e investigação | Avaliação de integrações e funcionalidades avançadas |

Prazos só serão definidos como baseline após avaliação de recursos, dependências, requisitos e aprovações.

## Governação obrigatória

O MELLITUS adota as regras do repositório [GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA), incluindo a Constituição, a norma de cabeçalho documental, os estados controlados, a cadeia de autoridade, os gates G0–G6, a evidência antes de alegação e o padrão WATCHDOG proporcional ao risco.

Este conjunto documental está em revisão. A sua existência não demonstra aprovação formal, conformidade legal, controlos técnicos ativos nem monitorização contínua.

## Documentação

- [Plano diretor e roadmap](docs/PLANO_DIRETOR.md)
- [Estrutura completa do projeto](ESTRUTURA_PROJETO.md)
- [Roadmap de implementação](GESTAO_PROJETO/ROADMAP.md)
- [Especificação funcional do produto](PRODUTO/README.md)
- [Arquitetura da aplicação](ARQUITETURA/README.md)
- [Modelo conceptual de dados](ARQUITETURA/MODELO_DE_DADOS.md)
- [Governação específica MELLITUS](GOVERNANCA/GOVERNANCA.md)
- [Registo de decisões](GOVERNANCA/REGISTO_DECISOES.md)
- [Requisitos](docs/REQUISITOS.md)
- [Registo de riscos](docs/RISCOS.md)
- [Segurança, privacidade e conformidade](SEGURANCA/README.md)
- [Estratégia de qualidade e testes](QUALIDADE_TESTES/README.md)
- [Operações, implantação e WATCHDOG](OPERACOES/README.md)
- [Plano de validação](docs/VALIDACAO.md)
- [Matriz de rastreabilidade](docs/MATRIZ_RASTREABILIDADE.md)
- [Pendências de decisão G0/G1](https://github.com/carlos-andrade/MELLITUS/issues/1)
- [Fontes clínicas e política editorial](CLINICA/FONTES_E_REVISAO.md)
- [Catálogo de fontes clínicas](CLINICA/CATALOGO_FONTES.md)
- [Prompts do projeto](PROMPT/README.md)
- [Estado do projeto](STATUS.md)

## Gates e lançamento

Nenhuma fase se considera concluída apenas por existir código ou documentação. Exigem-se entregáveis verificáveis, evidências de validação, riscos tratados ou aceites por autoridade competente e decisão explícita de passagem de fase. Obrigações legais e controlos críticos não são dispensáveis.

## Aviso

O conteúdo destina-se à educação em saúde e não constitui diagnóstico, aconselhamento clínico individualizado ou prescrição. Em caso de sintomas preocupantes ou emergência, deve procurar-se assistência médica adequada.

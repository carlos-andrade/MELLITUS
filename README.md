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
| **SHA-256 (conteúdo canónico)** | b284e3e7588b021fd94ef9785b7f6d6ab65d8be9a20c26c77ee427cceb1f5086 |
| **Commit de referência (versão anterior)** | N/A — baseline documental inicial |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Responsável do projeto — a formalizar |
| **Aprovador** | Pendente de aprovação formal |
| **Origem** | Briefing inicial e plano diretor do projeto |
| **Autoridade superior** | [Constituição GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA/blob/main/CONSTITUICAO.md); [Norma de cabeçalho](https://github.com/carlos-andrade/GOVERNANCA/blob/main/CABE%C3%87ALHO/NORMA-CABECALHO-PADRAO.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | docs/PLANO_DIRETOR.md; GOVERNANCA/REGISTO_DECISOES.md; STATUS.md |
| **Escopo** | Educação pública sobre diabetes e acompanhamento pessoal futuro; diagnóstico e prescrição excluídos |
| **Objetivo** | Criar uma plataforma acessível, segura e auditável apoiada em fontes clínicas rastreáveis |
| **Dependências** | Revisão clínica qualificada, avaliação de privacidade e requisitos legais aplicáveis |

## Visão

O MELLITUS é uma plataforma digital de informação, educação e, numa fase posterior, acompanhamento pessoal de registos relacionados com diabetes. Será desenvolvido por fases, com controlo de âmbito, decisões rastreáveis, validação científica, privacidade e segurança desde a conceção.

## Objetivos

- Disponibilizar conteúdos compreensíveis e apoiados por fontes rastreáveis.
- Explicar os tipos de diabetes, sintomas, prevenção de complicações e opções de tratamento com revisão profissional adequada.
- Avaliar registos pessoais opcionais apenas depois de definidos requisitos, riscos e controlos.
- Permitir controlo adequado dos dados pessoais, incluindo acesso, exportação e eliminação conforme aplicável.
- Manter decisões, versões, testes, incidentes e aprovações auditáveis.

## Limites de segurança

- O MELLITUS não substitui profissionais de saúde nem serviços de emergência.
- Não diagnostica nem exclui a possibilidade de doença.
- Não prescreve nem recomenda alterações autónomas de doses de insulina ou de outra medicação.
- Nenhum conteúdo clínico deve ser publicado como validado sem fontes verificáveis e revisão apropriada.
- Funcionalidades potencialmente enquadradas como dispositivo médico ou sistema de IA regulado ficam bloqueadas até avaliação adequada.

## Roadmap

| Fase | Nome | Resultado esperado |
|---|---|---|
| F0 | Governação e requisitos | Charter, âmbito, responsáveis, riscos, requisitos e gates |
| F1 | Investigação clínica e científica | Catálogo de fontes e fluxo de revisão editorial |
| F2 | Arquitetura e proteção de dados | Arquitetura, modelo de dados, ameaças e controlos |
| F3 | MVP educativo | Conteúdo pesquisável, navegação acessível e referências |
| F4 | Acompanhamento pessoal | Registos opcionais, histórico, tendências e exportação |
| F5 | Testes e validação | Evidências de qualidade, revisão clínica, privacidade e segurança |
| F6 | Piloto e lançamento | Piloto, correções e autorização de publicação |
| F7 | Evolução e investigação | Avaliação de integrações e funcionalidades avançadas |

Prazos só serão definidos como baseline após avaliação de recursos, dependências, requisitos e aprovações.

## Governação obrigatória

O MELLITUS adota as regras do repositório [GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA), incluindo a Constituição, a norma de cabeçalho documental, os estados controlados, a cadeia de autoridade, os gates G0–G6, a evidência antes de alegação e o padrão WATCHDOG proporcional ao risco.

Este conjunto documental está em revisão. A sua existência não demonstra aprovação formal, conformidade legal, controlos técnicos ativos nem monitorização contínua.

## Documentação

- [Plano diretor e roadmap](docs/PLANO_DIRETOR.md)
- [Governação específica MELLITUS](GOVERNANCA/GOVERNANCA.md)
- [Registo de decisões](GOVERNANCA/REGISTO_DECISOES.md)
- [Requisitos](docs/REQUISITOS.md)
- [Registo de riscos](docs/RISCOS.md)
- [Plano de validação](docs/VALIDACAO.md)
- [Fontes clínicas e política editorial](CLINICA/FONTES_E_REVISAO.md)
- [Estado do projeto](STATUS.md)
- [Estrutura completa do repositório](docs/ESTRUTURA_REPOSITORIO.md)
- [Arquitetura técnica proposta](docs/ARQUITETURA.md)
- [Modelo conceptual de dados](docs/MODELO_DADOS.md)
- [Plano de segurança e privacidade](docs/SEGURANCA_PRIVACIDADE.md)
- [Plano de operações e recuperação](docs/OPERACOES.md)
- [Roadmap de execução](docs/ROADMAP.md)
- [Contrato de API e política de integração](docs/API.md)
- [Registo de decisões arquiteturais](docs/ADR/README.md)
- [Política de contribuição](CONTRIBUTING.md)
- [Política de segurança](SECURITY.md)
- [Catálogo de fontes clínicas](CLINICA/CATALOGO_FONTES.md)
- [Testes previstos para os prompts](PROMPT/testes/README.md)

## Gates e lançamento

Nenhuma fase se considera concluída apenas por existir código ou documentação. Exigem-se entregáveis verificáveis, evidências de validação, riscos tratados ou aceites por autoridade competente e decisão explícita de passagem de fase. Obrigações legais e controlos críticos não são dispensáveis.

## Aviso

O conteúdo destina-se à educação em saúde e não constitui diagnóstico, aconselhamento clínico individualizado ou prescrição. Em caso de sintomas preocupantes ou emergência, deve procurar-se assistência médica adequada.

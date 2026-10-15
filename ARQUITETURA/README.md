# Arquitetura da aplicação MELLITUS

| Campo | Valor |
|---|---|
| **ID** | MEL-ARCH-README-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | ARQUITETURA |
| **Fase** | F2 — Arquitetura e proteção de dados |
| **Estado** | EM_REVISAO |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | PENDENTE_CALCULO |
| **Commit de referência (versão anterior)** | N/A — documento inicial |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Responsável técnico — a formalizar |
| **Aprovador** | Pendente de aprovação de G2 |
| **Origem** | Plano diretor, requisitos e análise inicial do repositório |
| **Autoridade superior** | [GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA); [governação MELLITUS](../GOVERNANCA/GOVERNANCA.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | docs/PLANO_DIRETOR.md; docs/REQUISITOS.md; docs/RISCOS.md; docs/VALIDACAO.md |

## 1. Objetivo e estado

Este documento define uma proposta de arquitetura modular para uma plataforma educativa de diabetes mellitus. A estrutura é um desenho inicial, não uma declaração de que a aplicação ou os controlos já existem. A seleção tecnológica final exige comparação documentada, validação de requisitos e aprovação G2.

## 2. Arquitetura lógica proposta

- **Interface web responsiva:** páginas públicas, pesquisa, navegação, avisos e acessibilidade.
- **Camada de aplicação:** casos de uso, validação, autorização e coordenação dos módulos.
- **Domínio:** artigos, fontes, versões editoriais, taxonomia e, numa fase posterior, registos pessoais.
- **Persistência:** base de dados relacional para metadados e dados operacionais; conteúdo editorial versionado.
- **Integrações:** apenas as necessárias, aprovadas, documentadas e com limites de confiança explícitos.
- **Operação:** logs minimizados, métricas técnicas, alertas, backups, restauração e rollback.

## 3. Stack tecnológica — proposta, não decisão final

Avaliar uma aplicação PHP suportada por uma versão com suporte de segurança, um framework mantido (por exemplo, Laravel ou Symfony), base de dados relacional (por exemplo, PostgreSQL ou MySQL/MariaDB), testes automatizados e pipeline CI. A escolha deve considerar competências, suporte, segurança, custo, manutenção, portabilidade e alojamento. Não fixar versões até consultar fontes oficiais e validar compatibilidade.

Evitar microserviços no MVP sem necessidade demonstrada. Preferir monólito modular e fronteiras de domínio explícitas enquanto a complexidade se mantiver proporcional.

## 4. Módulos

1. Conteúdo educativo e pesquisa.
2. Catálogo de fontes e rastreabilidade clínica.
3. Workflow editorial e versões.
4. Identidade e permissões administrativas, se houver áreas protegidas.
5. Privacidade, pedidos de direitos e gestão de consentimento quando aplicável.
6. Observabilidade, auditoria e resposta a incidentes.
7. Acompanhamento pessoal: módulo futuro, desativado até aprovação G2 própria.
8. Integrações com dispositivos ou serviços externos: estudo separado, sem ligação por defeito.

## 5. Separação de dados

Manter conteúdo público separado dos dados pessoais. Se for aprovado um módulo pessoal, definir isolamento por utilizador, controlo de acesso no servidor, minimização, encriptação adequada, retenção, exportação, eliminação, trilho de auditoria e política de backup. Não recolher dados de saúde no MVP educativo sem necessidade demonstrada e avaliação legal/privacidade.

## 6. Segurança por desenho

Definir modelo de ameaças, classificação de dados, fronteiras de confiança, gestão de segredos, atualizações de dependências, proteção contra injeção, XSS, CSRF, abuso de autenticação, escalada de privilégios e fuga de dados. Não guardar tokens ou palavras-passe em código ou repositório. Privacidade e segurança devem ser verificadas antes de produção.

## 7. Requisitos de qualidade

- Testes unitários, integração, ponta a ponta e migração conforme o módulo.
- Revisão de código e análise estática.
- Testes de dependências e vulnerabilidades.
- Testes de acessibilidade automatizados e manuais.
- Backups com ensaio de restauração.
- Logs sem dados de saúde desnecessários.
- Deploy repetível, rollback e documentação de operação.
- Rastreabilidade de requisito para implementação e teste.

## 8. Fluxo de decisão

Antes de implementar: requisitos selecionados e aprovados, desenho de dados, ameaça, critérios de aceitação, estratégia de testes e gates aplicáveis. Alterações de finalidade clínica ou recolha de dados pessoais de saúde exigem reavaliação formal.

## 9. Próxima ação

Comparar stack e opções de alojamento, completar o modelo de ameaças e a arquitetura de dados e obter aprovação G2. Até esse momento, a arquitetura permanece proposta.

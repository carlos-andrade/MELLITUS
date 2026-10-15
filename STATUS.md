# Estado do projeto MELLITUS

| Campo | Valor |
|---|---|
| **ID** | MEL-STATUS-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | ESTADO_PROJETO |
| **Fase** | F0 — Governação e requisitos |
| **Estado** | EM_CURSO |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | 2785833645a6f5c6794c5a21a2b7e807ed226ff116d2c00160ae1ee98bf5f086 |
| **Commit de referência (versão anterior)** | N/A — documento inicial |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Responsável de projeto — a formalizar |
| **Aprovador** | Pendente de aprovação formal |
| **Origem** | Roadmap inicial do MELLITUS |
| **Autoridade superior** | [Constituição GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA/blob/main/CONSTITUICAO.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | README.md; docs/PLANO_DIRETOR.md; GOVERNANCA/REGISTO_DECISOES.md |
| **Escopo** | Estado confirmado de documentação, requisitos e gates |
| **Objetivo** | Comunicar estado sem confundir trabalho planeado com execução comprovada |
| **Dependências** | Evidências e decisões formais dos gates |

## Barra de progresso

**Implementação funcional do produto comprovada: 0%.** Nenhuma funcionalidade da aplicação foi verificada. Foi adicionada uma estrutura documental de arquitetura, produto, segurança, testes, operações e roadmap; estes documentos não equivalem à implementação.

`[░░░░░░░░░░] 0% — implementação funcional comprovada`

A documentação inicial não equivale a produto implementado, conteúdo validado clinicamente, aprovação regulatória ou publicação.

## Estado por fase

| Fase | Estado | Evidência disponível | Próximo critério |
|---|---|---|---|
| F0 — Governação e requisitos | EM_CURSO | Documentos iniciais; hashes/cabeçalhos por validar | Confirmar responsáveis, aprovar âmbito e registar G0/G1 |
| F1 — Evidência clínica | PROPOSTO | Política editorial proposta; revisão clínica por fazer | Fontes verificadas e revisor identificado |
| F2 — Arquitetura e privacidade | EM_REVISAO | Proposta em ARQUITETURA/ e SEGURANCA/; ainda sem aprovação | Validar stack, modelo de ameaças, privacidade e G2 |
| F3 — MVP educativo | PROPOSTO | Especificação funcional documentada em PRODUTO/; sem aplicação funcional verificada | Implementar e demonstrar testes após G2 |
| F4 — Acompanhamento pessoal | BLOQUEADO | Requisitos e desenho para dados pessoais de saúde ainda não aprovados | Aprovação G2 e controlos de privacidade |
| F5 — Testes e validação | PROPOSTO | Plano de validação documental | Executar testes numa versão concreta |
| F6 — Piloto e lançamento | BLOQUEADO | Produto ainda não validado | Gates G3/G4/G5 e autorização formal |
| F7 — Evolução e investigação | PROPOSTO | Conceitos sem estudo concluído | Viabilidade e análise de risco novas |

## Bloqueios conhecidos

- Responsável de projeto/produto por formalizar.
- Revisor clínico qualificado por identificar.
- Baseline funcional MVP por aprovar.
- Avaliação legal e de privacidade por realizar.
- Arquitetura documentada como proposta; aprovação G2 e implementação pendentes.
- Stack tecnológica ainda não selecionada.
- Código da aplicação e pipeline CI ainda não verificados.
- Conformidade final dos cabeçalhos e SHA-256 por verificar.
- Nenhum gate formal declarado aprovado.
- Monitorização operacional ativa MELLITUS não demonstrada.

## Auditoria da estrutura (2026-10-15)

A árvore `main` foi consultada após as alterações; os nove documentos estruturantes esperados estão presentes e os cabeçalhos possuem título H1 e campos principais. Os hashes SHA-256 canónicos dos nove documentos novos foram calculados segundo a norma e recalculados após gravação; os nove valores coincidem. Esta verificação não cobre automaticamente todos os documentos históricos do repositório. Não foi executada validação de runtime da aplicação, pois não há implementação funcional verificada.

## Documentos estruturantes adicionados nesta atualização

- `docs/ESTRUTURA_REPOSITORIO.md` — árvore real inicial versus árvore-alvo.
- `docs/ARQUITETURA.md` — arquitetura técnica proposta e fronteiras do MVP.
- `docs/MODELO_DADOS.md` — entidades editoriais e limites para futuros dados de saúde.
- `docs/SEGURANCA_PRIVACIDADE.md` — controlos propostos.
- `docs/OPERACOES.md` — monitorização, backups, recuperação e release.
- `docs/ROADMAP.md` — fases, estados e critérios de saída.
- `docs/API.md` e `docs/ADR/README.md` — integrações e decisões arquiteturais.
- `CARTAS/README.md`, `LAYOUT/README.md` e `GOVERNANCA/REGISTO_EXCECOES.md` — cadeia documental e governação.
- `CLINICA/CATALOGO_FONTES.md` e `PROMPT/testes/README.md` — fontes e validação de prompts.
- `CONTRIBUTING.md`, `SECURITY.md`, `.gitignore`, `.editorconfig`, `.env.example` e `CHANGELOG.md` — práticas do repositório.

Estes artefactos são propostas documentais. Os hashes canónicos dos nove documentos estruturantes desta atualização foram calculados e validados. A conformidade integral de todos os documentos preexistentes ainda requer auditoria própria.

## Próximas ações

1. Verificar cabeçalhos e calcular SHA-256 canónico segundo a norma.
2. Formalizar responsáveis e aprovar G0/G1.
3. Definir e aprovar requisitos do MVP.
4. Verificar normas, fontes e obrigações legais atuais.
5. Iniciar arquitetura apenas após aprovação de âmbito e riscos.

## Evidência

Commits no repositório demonstram a gravação documental, não a validação clínica, funcional ou regulatória.

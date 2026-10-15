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
| **SHA-256 (conteúdo canónico)** | 30d8e511ed96565ce653840d3c7060fe8b6c4dff9d7d360bbc662989f56be2c9 |
| **Commit de referência (versão anterior)** | [103ed03a3b509e33aa2cba9313b1056a2ac0a5e4](https://github.com/carlos-andrade/MELLITUS/commit/103ed03a3b509e33aa2cba9313b1056a2ac0a5e4) |
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
| F0 — Governação e requisitos | EM_CURSO | Documentação inicial, matriz de rastreabilidade e issue #1 para decisão G0/G1 | Formalizar responsáveis, aprovar âmbito e registar decisão autorizada |
| F1 — Catálogo de fontes oficiais | PROPOSTO | Verificação técnica dos oito portais-raiz: 7 PASS, 0 WARN, 1 UNKNOWN; SNS 24 requer JavaScript; raiz NICE sem validação direta; página temática NICE NG28 localizada | Confirmar WARN/UNKNOWN, verificar URLs temáticas e metadados; sem conteúdo clínico próprio |
| F2 — Arquitetura e privacidade | EM_REVISAO | Proposta em ARQUITETURA/ e SEGURANCA/; ainda sem aprovação | Validar stack, modelo de ameaças, privacidade e G2 |
| F3 — MVP diretório de fontes | PROPOSTO | Especificação de catálogo externo em PRODUTO/; sem aplicação funcional verificada | Implementar e demonstrar testes após G2 |
| F4 — Acompanhamento pessoal | BLOQUEADO | Requisitos e desenho para dados pessoais de saúde ainda não aprovados | Aprovação G2 e controlos de privacidade |
| F5 — Testes e validação | PROPOSTO | Plano de validação documental | Executar testes numa versão concreta |
| F6 — Piloto e lançamento | BLOQUEADO | Produto ainda não validado | Gates G3/G4/G5 e autorização formal |
| F7 — Evolução e investigação | PROPOSTO | Conceitos sem estudo concluído | Viabilidade e análise de risco novas |

## Bloqueios conhecidos

- Responsável de projeto/produto por formalizar.
- O proprietário declarou que não haverá revisor clínico; conteúdo clínico próprio, resumos, traduções, interpretações e recomendações ficam excluídos do MVP proposto.
- Baseline funcional MVP por aprovar.
- Avaliação legal e de privacidade por realizar.
- Arquitetura documentada como proposta; aprovação G2 e implementação pendentes.
- Stack tecnológica ainda não selecionada.
- Código da aplicação e pipeline CI ainda não verificados.
- Auditoria cruzada dos 36 Markdown concluída anteriormente. Nesta atualização, os hashes canónicos dos quatro documentos alterados foram recalculados e verificados individualmente; os quatro coincidem com os valores declarados nos cabeçalhos.
- Nenhum gate formal declarado aprovado.
- Monitorização operacional ativa MELLITUS não demonstrada.

## Auditoria da estrutura (2026-10-15)

A árvore `main` foi comparada com a baseline auditada em `a865fb67477acaf225f90523b5442b8b5a51dbb6`: 41 ficheiros (blobs), dos quais 37 Markdown. Dos 36 Markdown da baseline, 24 permanecem byte-identicamente inalterados; 12 foram atualizados e tiveram o SHA-256 canónico recalculado. O novo documento de decisão também teve o hash recalculado. Os 13 documentos alterados/criados foram verificados individualmente: 13/13 hashes coincidem. A auditoria anterior dos 36 Markdown mantém-se válida para os 24 ficheiros inalterados. A validação de runtime da aplicação não foi executada, pois não há implementação funcional verificada.

## Rastreabilidade F0

- Matriz: [docs/MATRIZ_RASTREABILIDADE.md](docs/MATRIZ_RASTREABILIDADE.md).
- Decisão G0/G1: [issue #1](https://github.com/carlos-andrade/MELLITUS/issues/1), aberta; não equivale a aprovação.

## Documentos estruturantes adicionados nesta atualização

- `docs/ESTRUTURA_REPOSITORIO.md` — árvore real inicial versus árvore-alvo.
- `docs/MATRIZ_RASTREABILIDADE.md` — matriz de requisitos, riscos, testes e gates.
- `GESTAO_PROJETO/DECISAO_ESCOPO_SEM_REVISAO_CLINICA.md` — decisão de não nomear revisor e proposta de redução de âmbito.
- `docs/ARQUITETURA.md` — arquitetura técnica proposta e fronteiras do MVP.
- `docs/MODELO_DADOS.md` — entidades editoriais e limites para futuros dados de saúde.
- `docs/SEGURANCA_PRIVACIDADE.md` — controlos propostos.
- `docs/OPERACOES.md` — monitorização, backups, recuperação e release.
- `docs/ROADMAP.md` — roadmap auxiliar legado; a fonte canónica é `GESTAO_PROJETO/ROADMAP.md`.
- `docs/API.md` e `docs/ADR/README.md` — integrações e decisões arquiteturais.
- `CARTAS/README.md`, `LAYOUT/README.md` e `GOVERNANCA/REGISTO_EXCECOES.md` — cadeia documental e governação.
- `CLINICA/CATALOGO_FONTES.md` e `PROMPT/testes/README.md` — fontes e validação de prompts.
- `CONTRIBUTING.md`, `SECURITY.md`, `.gitignore`, `.editorconfig`, `.env.example` e `CHANGELOG.md` — práticas do repositório.

Estes artefactos são propostas documentais. A auditoria dos 36 ficheiros Markdown foi concluída: cabeçalhos e campos obrigatórios presentes, IDs únicos, hashes canónicos coincidentes e links relativos analisados sem destinos inexistentes. A aplicação continua sem implementação funcional verificada.

## Próximas ações

1. Formalizar responsáveis e aprovar âmbito e requisitos MVP.
2. Ratificar o âmbito reduzido proposto em [GESTAO_PROJETO/DECISAO_ESCOPO_SEM_REVISAO_CLINICA.md](GESTAO_PROJETO/DECISAO_ESCOPO_SEM_REVISAO_CLINICA.md) e concluir a issue #1.
3. Formalizar responsáveis e documentar viabilidade/custos/riscos com evidência.
4. Só após decisão G0/G1, preparar G2 para stack, arquitetura e privacidade.

## Evidência

Commits no repositório demonstram a gravação documental, não a validação clínica, funcional ou regulatória.


## Verificação de governação adicional — 2026-10-15

A issue #1 estava fechada com todas as caixas assinaladas, mas continha apenas o comentário geral do proprietário (“OK, DEI UM ACEITE PARA TODOS.”) e não apresentava evidência individual para nomeação de responsável/revisor clínico, viabilidade ou decisão formal G0/G1. A issue foi reaberta e as caixas foram alinhadas com a evidência observada. A aceitação do âmbito e das exclusões foi registada como parcial; não constitui aprovação de gate. Implementação funcional comprovada: 0%.


## Atualização de âmbito — 2026-10-15

O proprietário declarou explicitamente que não haverá revisor clínico. Para não apresentar conteúdo médico como validado, a alternativa proposta para o MVP é um diretório de fontes oficiais com ligações diretas e metadados; o projeto não redigirá, resumirá, traduzirá nem interpretará conteúdo clínico e não recolherá dados pessoais de saúde. O âmbito reduzido e a viabilidade ainda precisam de ratificação G0/G1. Implementação funcional comprovada permanece 0%.


A verificação técnica dos portais oficiais foi atualizada em 2026-10-15: 7 PASS, 0 WARN e 1 UNKNOWN. Foram localizadas páginas temáticas oficiais da NICE (NG28), DGS (Diabetes e Relatórios/Publicações) e ADA (About Diabetes); os metadados estão registados no catálogo. Isto não equivale a revisão clínica. A checklist da issue #1 foi corrigida: seis itens sem evidência individual voltaram a pendente. G0/G1 continuam não aprovados.

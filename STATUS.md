# Estado do projeto MELLITUS

| Campo | Valor |
|---|---|
| **ID** | MEL-STATUS-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | ESTADO_PROJETO |
| **Fase** | G2 — preparação e avaliação de arquitetura/privacidade |
| **Estado** | EM_CURSO — G0/G1 aprovados; G2 documentalmente preparado, aprovação pendente |
| **Versão** | 1.1.0 |
| **SHA-256 (conteúdo canónico)** | 7b7cec3a0d065f70f9565e37fb51d0ff2e1ca6bd336bc07b4269edb8a18c773e |
| **Commit de referência (versão anterior)** | Histórico Git preservado; SHA do commit anterior não verificado nesta atualização |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Carlos Andrade — patrocinador e responsável de produto/projeto |
| **Aprovador** | Carlos Andrade — D1–D8 aprovadas em 2026-10-15 |
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
| F0 — Governação e requisitos | CONCLUÍDA (D1–D8 aprovadas) | Pacote de decisão v1.0.0 e comentário explícito do proprietário na issue #1 | Manter baseline e rastreabilidade; alterações de âmbito exigem nova decisão |
| F1 — Catálogo de fontes oficiais | PROPOSTO | Verificação técnica dos oito portais-raiz: 7 PASS, 0 WARN, 1 UNKNOWN; SNS 24 requer JavaScript; raiz NICE sem validação direta; página temática NICE NG28 localizada | Confirmar WARN/UNKNOWN, verificar URLs temáticas e metadados; sem conteúdo clínico próprio |
| F2 — Arquitetura e privacidade | EM_REVISAO — pacote G2 preparado; aprovação pendente | Pacote G2, ADR-001, modelo de ameaças e triagem de privacidade publicados | Fechar avaliação de alojamento/logs, papéis RGPD e necessidade de AIPD; obter decisão formal G2 |
| F3 — MVP diretório de fontes | PROPOSTO | Especificação de catálogo externo em PRODUTO/; sem aplicação funcional verificada | Implementar e demonstrar testes após G2 |
| F4 — Acompanhamento pessoal | BLOQUEADO — fora do MVP | Dados pessoais de saúde excluídos da baseline aprovada | Nova decisão G1/G2, avaliação de privacidade e autorização explícita própria |
| F5 — Testes e validação | PROPOSTO | Plano de validação documental | Executar testes numa versão concreta |
| F6 — Piloto e lançamento | BLOQUEADO | Produto ainda não validado | Gates G3/G4/G5 e autorização formal |
| F7 — Evolução e investigação | PROPOSTO | Conceitos sem estudo concluído | Viabilidade e análise de risco novas |

## Bloqueios conhecidos

- Responsável de projeto/produto formalizado: Carlos Andrade (aprovação explícita na issue #1).
- O proprietário declarou que não haverá revisor clínico; conteúdo clínico próprio, resumos, traduções, interpretações e recomendações ficam excluídos do MVP proposto.
- Baseline do MVP estático aprovada em D1–D8; alterações de âmbito exigem nova decisão.
- G2 documentalmente preparado; fornecedor/região, logs, papéis RGPD e decisão sobre AIPD continuam UNKNOWN/PENDENTE.
- Arquitetura estática proposta; aprovação G2, implementação e publicação pendentes.
- Stack tecnológica ainda não selecionada.
- Código da aplicação e pipeline CI ainda não verificados.
- Auditoria cruzada dos 36 Markdown concluída anteriormente. Nesta atualização, os hashes canónicos dos quatro documentos alterados foram recalculados e verificados individualmente; os quatro coincidem com os valores declarados nos cabeçalhos.
- G0/G1 aprovados explicitamente em 2026-10-15; G2 não aprovado.
- Monitorização operacional ativa MELLITUS não demonstrada.

## Auditoria da estrutura (2026-10-15)

A árvore `main` foi comparada com a baseline auditada em `a865fb67477acaf225f90523b5442b8b5a51dbb6`: 41 ficheiros (blobs), dos quais 37 Markdown. Dos 36 Markdown da baseline, 24 permanecem byte-identicamente inalterados; 12 foram atualizados e tiveram o SHA-256 canónico recalculado. O novo documento de decisão também teve o hash recalculado. Os 13 documentos alterados/criados foram verificados individualmente: 13/13 hashes coincidem. A auditoria anterior dos 36 Markdown mantém-se válida para os 24 ficheiros inalterados. A validação de runtime da aplicação não foi executada, pois não há implementação funcional verificada.

## Rastreabilidade F0/G2

O pacote de decisão [GESTAO_PROJETO/PACOTE_DECISAO_F0_G0_G1.md](GESTAO_PROJETO/PACOTE_DECISAO_F0_G0_G1.md), versão 1.0.0, foi aprovado explicitamente pelo proprietário na [issue #1](https://github.com/carlos-andrade/MELLITUS/issues/1#issuecomment-6197870350). D1–D8 aprovadas; G0/G1 aprovados; G2 autorizado apenas para preparação e avaliação. Custo monetário UNKNOWN e sem orçamento autorizado. Implementação funcional permanece em 0% e bloqueada.

- Matriz: [docs/MATRIZ_RASTREABILIDADE.md](docs/MATRIZ_RASTREABILIDADE.md).
- Pacote G2: [GESTAO_PROJETO/PACOTE_G2_ARQUITETURA_PRIVACIDADE.md](GESTAO_PROJETO/PACOTE_G2_ARQUITETURA_PRIVACIDADE.md).
- Modelo de ameaças: [docs/AMEACAS.md](docs/AMEACAS.md).
- Triagem de privacidade: [docs/AVALIACAO_PRIVACIDADE_MVP.md](docs/AVALIACAO_PRIVACIDADE_MVP.md).
- ADR-001: [docs/ADR/ADR-001-ARQUITETURA-ESTATICA.md](docs/ADR/ADR-001-ARQUITETURA-ESTATICA.md).
- Decisão G0/G1: [issue #1](https://github.com/carlos-andrade/MELLITUS/issues/1), fechada após aprovação explícita D1–D8 em 2026-10-15.
- Pendências G2: [issue #2](https://github.com/carlos-andrade/MELLITUS/issues/2).

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

A issue #1 contém aprovação explícita D1–D8, confirmação do responsável de produto/projeto, aceitação da estimativa preliminar, custo monetário UNKNOWN e autorização limitada à preparação/avaliação G2. G0/G1 aprovados; G2 permanece pendente. Implementação funcional comprovada: 0%.


## Atualização de âmbito — 2026-10-15

O proprietário declarou explicitamente que não haverá revisor clínico. Para não apresentar conteúdo médico como validado, a alternativa proposta para o MVP é um diretório de fontes oficiais com ligações diretas e metadados; o projeto não redigirá, resumirá, traduzirá nem interpretará conteúdo clínico e não recolherá dados pessoais de saúde. O âmbito reduzido e a viabilidade ainda precisam de ratificação G0/G1. Implementação funcional comprovada permanece 0%.


A verificação técnica dos portais oficiais foi atualizada em 2026-10-15:

A verificação de páginas temáticas oficiais continua a ser evidência de pesquisa/metadados, não teste HTTP direto de todos os URLs nem revisão clínica. A aprovação formal D1–D8 na issue #1 concluiu F0 e aprovou G0/G1 em 2026-10-15. A issue #2 acompanha as pendências de G2; implementação funcional continua bloqueada.


## Adenda de auditoria G2 — 2026-10-15

Preparação documental concluída: pacote de decisão, ADR-001, modelo de ameaças e triagem de privacidade publicados; arquitetura, modelo de dados, riscos e matriz alinhados ao MVP estático. G2 permanece EM_REVISAO. Alojamento/região, tratamento de logs, papéis RGPD e determinação formal sobre AIPD continuam UNKNOWN/PENDENTE. Implementação funcional comprovada: 0%; sem autorização para construir, publicar, recolher dados ou assumir custos.


A avaliação de fornecedor identificou GitHub Pages como candidato tecnicamente compatível, não selecionado: a documentação oficial indica registo e armazenamento de IPs de visitantes para segurança. A avaliação de retenção, papéis RGPD e informação de privacidade continua pendente. Ver [issue #2](https://github.com/carlos-andrade/MELLITUS/issues/2).

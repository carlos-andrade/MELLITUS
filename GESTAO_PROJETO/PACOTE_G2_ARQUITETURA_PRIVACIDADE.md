# Pacote de decisão — G2 Arquitetura e privacidade

| Campo | Valor |
|---|---|
| **ID** | MEL-G2-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | PACOTE_DECISAO |
| **Fase** | G2 — Arquitetura e privacidade |
| **Estado** | EM_REVISAO — preparado para decisão; G2 não aprovado |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | 6a3588cd52e89df7dd3a194dc5c719cee19c283979b0dff90016798cfbc95562 |
| **Commit de referência (versão anterior)** | N/A — documento inicial G2 |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Carlos Andrade — patrocinador/responsável de produto; responsável técnico especializado não designado |
| **Aprovador** | Carlos Andrade — aprovação G2 pendente |
| **Origem** | G0/G1 aprovados; autorização limitada para preparação e avaliação de G2 |
| **Autoridade superior** | [GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA); [Constituição](https://github.com/carlos-andrade/GOVERNANCA/blob/main/CONSTITUICAO.md); [norma de cabeçalho](https://github.com/carlos-andrade/GOVERNANCA/blob/main/CABE%C3%87ALHO/NORMA-CABECALHO-PADRAO.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | [arquitetura](../docs/ARQUITETURA.md); [ameaças](../docs/AMEACAS.md); [triagem de privacidade](../docs/AVALIACAO_PRIVACIDADE_MVP.md); [modelo de dados](../docs/MODELO_DADOS.md); [riscos](../docs/RISCOS.md); [matriz](../docs/MATRIZ_RASTREABILIDADE.md) |

## 1. Decisão de arquitetura proposta

**Escolha recomendada:** site estático gerado a partir de ficheiros de catálogo versionados no Git; HTML semântico, CSS responsivo e JavaScript mínimo apenas para pesquisa local, se necessário.

**Excluídos:** backend, API própria, base de dados, autenticação, contas, perfis, formulários, analytics, cookies não essenciais, publicidade, pixels de terceiros, IA clínica e registo de utilizadores.

**Alojamento:** fornecedor e região ainda não selecionados. A escolha depende da análise dos termos, logs, localização, tratamento pelo fornecedor, recuperação e custo. Não assumir custos nem ativar publicação.

## 2. Modelo de dados do MVP

Apenas metadados editoriais: entidade/organização, título oficial, URL, temas, jurisdição/idioma quando conhecidos, data de verificação técnica e estado PASS/WARN/FAIL/UNKNOWN.

Não incluir resumos, afirmações clínicas próprias, recomendações, traduções, interpretação clínica, perfis, medições de glicemia, sintomas, medicação, contas ou identificadores de visitantes.

## 3. Fluxos e fronteiras

1. O responsável edita metadados no repositório.
2. A alteração fica registada no histórico Git.
3. Uma validação futura verifica campos obrigatórios, HTTPS, domínio e data.
4. Um processo de build futuro gera HTML estático.
5. O navegador recebe os ficheiros do fornecedor de alojamento.
6. Ao clicar num link, o utilizador passa para o site externo e fica sujeito às práticas desse destino.

Não há fluxo previsto de dados introduzidos por visitantes. O alojamento pode processar dados técnicos dos pedidos, como IP, timestamp e user-agent; este ponto depende do fornecedor e não está resolvido.

## 4. Ameaças e controlos

Ver [docs/AMEACAS.md](../docs/AMEACAS.md). Ameaças prioritárias: link malicioso/desatualizado; adulteração do catálogo; falsa impressão de validação clínica; rastreamento por terceiros; segredos no Git; indisponibilidade do fornecedor; falhas de acessibilidade.

Controlos propostos: domínios oficiais permitidos; revisão rastreável; ausência de scripts, analytics, fontes ou embeds de terceiros; HTTPS e cabeçalhos de segurança quando suportados; privilégios mínimos; aviso de fonte externa; correção/remoção de links; testes antes do lançamento. Estes controlos não estão implementados nem testados.

## 5. Triagem de privacidade

Ver [docs/AVALIACAO_PRIVACIDADE_MVP.md](../docs/AVALIACAO_PRIVACIDADE_MVP.md). Dados de saúde de visitantes, contas, perfis, formulários e analytics estão excluídos. Dados técnicos de acesso podem ser processados pelo fornecedor. Cookies próprios não estão previstos. A necessidade de AIPD não está formalmente determinada; depende do tratamento real, do alojamento e da análise das regras aplicáveis.

## 6. Decisões arquiteturais

| ID | Decisão | Estado |
|---|---|---|
| ADR-001 | Site estático sem backend/base de dados | Proposta pronta para ratificação |
| ADR-002 | Apenas metadados e links oficiais | Baseline aprovada em D1–D8 |
| ADR-003 | Sem analytics, trackers, cookies próprios ou recursos remotos de terceiros | Proposta de privacidade |
| ADR-004 | Fornecedor/região de alojamento | Pendente de análise |
| ADR-005 | Publicação e CI/CD | Fora da autorização atual |

Ver [ADR-001](../docs/ADR/ADR-001-ARQUITETURA-ESTATICA.md).

## 7. Critérios de saída G2

- [x] Âmbito sem dados pessoais de saúde e sem conteúdo clínico próprio confirmado.
- [x] Arquitetura estática proposta e fronteiras de confiança descritas.
- [x] Inventário preliminar de dados e fluxos documentado.
- [x] Modelo de ameaças e controlos propostos registados.
- [x] Riscos e testes de aceitação ligados à matriz de rastreabilidade.
- [ ] Escolher e avaliar alojamento, região, logs, subprocessadores e termos.
- [ ] Determinar formalmente papéis de privacidade e necessidade de AIPD.
- [ ] Ratificar explicitamente o desenho G2 após fechar os pontos anteriores.
- [ ] Autorizar G3/construção por decisão separada.

As caixas assinaladas indicam trabalho documental, não execução de testes de runtime.

## 8. Bloqueios

G2 permanece EM_REVISAO até fechar os pontos pendentes da secção 7. Não iniciar construção funcional, CI/CD de publicação, recolha de dados, compra de serviços ou lançamento. A ausência de revisor clínico mantém excluídos todos os conteúdos clínicos próprios.

## 9. Fontes oficiais de privacidade

- [CNPD — Avaliação de impacto](https://www.cnpd.pt/organizacoes/outras-obrigacoes/avaliacao-de-impacto/).
- [Diário da República — Regulamento n.º 798/2018 da CNPD](https://diariodarepublica.pt/dr/detalhe/regulamento/798-2018-117182365).
- [Comissão Europeia — categorias especiais de dados, incluindo dados de saúde](https://commission.europa.eu/law/law-topic/data-protection/information-individuals_en).

Estas fontes suportam a triagem, não constituem parecer jurídico para o projeto.

## 10. Resultado

**G2 preparado documentalmente, mas não aprovado.** Permanecem pendentes a avaliação do alojamento, a análise especializada de privacidade aplicável e a decisão formal do gate. A implementação funcional continua bloqueada.

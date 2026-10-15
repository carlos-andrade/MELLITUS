# MELLITUS — Plano de segurança e privacidade

| Campo | Valor |
|---|---|
| **ID** | MEL-SEC-PRIV-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | PLANO_CONTROLOS |
| **Fase** | F2 — Arquitetura e proteção de dados |
| **Estado** | EM_REVISAO — controlos propostos; avaliação do alojamento pendente |
| **Versão** | 1.2.0 |
| **SHA-256 (conteúdo canónico)** | ba3540afee72b1ba9eae8ea7d7b96035224f29f59843b0b49d8bb7b1fc57ee12 |
| **Commit de referência (versão anterior)** | Histórico Git preservado; SHA do commit anterior não verificado nesta atualização |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Carlos Andrade — responsável de produto; especialista de privacidade/jurídico não designado |
| **Aprovador** | Pendente de revisão especializada e decisão G2 |
| **Origem** | Governação MELLITUS e requisitos iniciais |
| **Autoridade superior** | [GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA); [Governação MELLITUS](../GOVERNANCA/GOVERNANCA.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | docs/REQUISITOS.md; docs/ARQUITETURA.md; docs/MODELO_DADOS.md; docs/RISCOS.md; docs/VALIDACAO.md |

## 1. Estado

Plano proposto; não é auditoria concluída, certificação, avaliação jurídica ou prova de controlos técnicos ativos.

## 2. Desenvolvimento seguro

- Rever dependências, licenças, vulnerabilidades e versões suportadas.
- Rever alterações e manter histórico rastreável.
- Guardar segredos fora do Git e verificar fugas acidentais.
- Aplicar privilégio mínimo e separar ambientes.
- Executar lint, testes e análise estática depois de configurar CI.
- Nunca copiar dados de produção para teste.
- Produzir releases rastreáveis com changelog e rollback.

## 3. Controlos aplicáveis ao MVP estático

- Não introduzir backend, autenticação, sessões, SQL, formulários ou uploads.
- Não carregar scripts, fontes, CDNs, analytics, pixels ou embeds remotos de terceiros.
- Validar esquema do catálogo, HTTPS e lista permitida de domínios antes de qualquer publicação.
- Usar HTTPS e cabeçalhos de segurança/CSP se suportados pelo alojamento selecionado.
- Não guardar segredos no repositório; limitar permissões de escrita e proteger credenciais de manutenção.
- Minimizar erros e logs; avaliar o que o fornecedor regista e durante quanto tempo.
- Tornar o aviso de fonte externa visível e testar a sua presença.
- Todos os controlos são PROPOSTOS; não declarar ativos sem teste e evidência.

## 4. Privacidade e dados

O MVP não recolhe dados de saúde, contas, perfis, formulários, cookies próprios ou analytics. A pesquisa, se existir, é local. O alojamento pode tratar IP, user-agent, timestamp ou logs técnicos; fornecedor, região, retenção, subprocessadores, transferências e papéis RGPD continuam desconhecidos.

A decisão sobre a necessidade de AIPD/DPIA não está concluída. Antes da publicação, analisar o tratamento real, as condições do fornecedor, o artigo 35.º do RGPD e a lista aplicável da CNPD, e registar a decisão fundamentada. Não alegar conformidade legal sem avaliação competente.

Ver [AVALIACAO_PRIVACIDADE_MVP.md](AVALIACAO_PRIVACIDADE_MVP.md).## 5. Conteúdo clínico e IA

Fontes rastreáveis e revisão humana antes da publicação. Não publicar automaticamente recomendações terapêuticas individualizadas. Não inserir dados identificáveis em ferramentas externas sem avaliação e autorização. Versionar prompts/testes e encaminhar respostas perigosas para revisão. Reavaliar finalidade e regulação antes de capacidades que influenciem decisões clínicas.

## 6. Incidentes e vulnerabilidades

Registar ID, data, gravidade, sistemas afetados, impacto, dados potencialmente envolvidos, contenção, análise, notificações, correção, evidências e lições. Definir canal e triagem antes do piloto; não publicar detalhes exploráveis.

## 7. Saída pré-produção

Sem segredos; dependências suportadas; testes críticos de segurança executados; HTTPS verificado; restauro e rollback testados; logs/alertas definidos; avaliação de privacidade e revisão clínica completas para o âmbito lançado; plano de incidente e autorização explícita registados.

## 8. Próxima ação

Executar modelação de ameaças e converter controlos em requisitos/testes. Não marcar controlos ativos sem evidência.


## 9. Adenda G2 — 2026-10-15

Foi criada a triagem [AVALIACAO_PRIVACIDADE_MVP.md](AVALIACAO_PRIVACIDADE_MVP.md) e o [modelo de ameaças](AMEACAS.md). O MVP não recolhe dados de saúde, não cria contas, formulários, analytics nem cookies próprios. O fornecedor pode tratar logs técnicos; região, retenção, subprocessadores, papéis RGPD e necessidade de AIPD permanecem UNKNOWN até escolha do alojamento e análise aplicável. Nenhum controlo descrito neste plano é considerado ativo sem teste. G2 permanece EM_REVISAO.

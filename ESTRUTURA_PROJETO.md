# Estrutura completa proposta do projeto MELLITUS

| Campo | Valor |
|---|---|
| **ID** | MEL-ESTRUTURA-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | ESTRUTURA_PROJETO |
| **Fase** | F0 — Governação e requisitos |
| **Estado** | EM_REVISAO |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | 66ee39236586dd89a8e19e45535f29d66e2d38c0679be0de5b02ea77ed76f16f |
| **Commit de referência (versão anterior)** | N/A — documento inicial |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Responsável de projeto — a formalizar |
| **Aprovador** | Pendente de baseline |
| **Origem** | Inventário atual e planeamento de desenvolvimento |
| **Autoridade superior** | [GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA); [governação MELLITUS](GOVERNANCA/GOVERNANCA.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | README.md; STATUS.md; GESTAO_PROJETO/ROADMAP.md; docs/PLANO_DIRETOR.md |

## 1. Princípio

A estrutura proposta separa documentação, código da aplicação, conteúdo clínico, testes e operações. Os diretórios de código abaixo são planeados, não implementados. A stack técnica e os nomes concretos dos diretórios `app/` devem ser confirmados em G2.

## 2. Árvore proposta

```text
MELLITUS/
├── README.md
├── STATUS.md
├── ESTRUTURA_PROJETO.md
├── LICENSE
├── CHANGELOG.md                         # quando existirem versões executáveis
├── .gitignore                            # validar antes de adicionar
├── .editorconfig                         # proposto
├── .env.example                          # sem valores secretos reais
├── GOVERNANCA/
│   ├── GOVERNANCA.md
│   └── REGISTO_DECISOES.md
├── PROMPT/
│   ├── README.md
│   └── PROMPT-ESPECIALISTA-DIABETES-MELLITUS.md
├── GESTAO_PROJETO/
│   └── ROADMAP.md
├── docs/
│   ├── PLANO_DIRETOR.md
│   ├── REQUISITOS.md
│   ├── RISCOS.md
│   ├── VALIDACAO.md
│   ├── ARQUITETURA/
│   ├── ADR/
│   └── RUNBOOKS/
├── ARQUITETURA/
│   ├── README.md
│   └── MODELO_DE_DADOS.md
├── PRODUTO/
│   └── README.md
├── CLINICA/
│   ├── FONTES_E_REVISAO.md
│   ├── CATALOGO_FONTES.md               # proposto
│   ├── ARTIGOS/                         # propostas com revisão
│   └── HISTORICO_CORRECOES.md           # proposto
├── SEGURANCA/
│   └── README.md
├── QUALIDADE_TESTES/
│   └── README.md
├── OPERACOES/
│   └── README.md
├── app/                                  # por criar após aprovação da stack
│   ├── Http/
│   ├── Application/
│   ├── Domain/
│   └── Infrastructure/
├── resources/                             # vistas, estilos, scripts, idiomas
├── routes/                                # rotas públicas e administrativas
├── database/
│   ├── migrations/
│   ├── seeders/                           # apenas dados fictícios ou públicos
│   └── factories/
├── tests/
│   ├── Unit/
│   ├── Integration/
│   ├── Feature/
│   ├── Security/
│   └── Accessibility/
├── public/                                # recursos públicos e entrypoint
├── storage/                               # nunca versionar dados/runtime sensíveis
└── .github/
    ├── workflows/                         # CI após decisão técnica
    ├── ISSUE_TEMPLATE/
    └── PULL_REQUEST_TEMPLATE.md
```

A estrutura é conceptual. Se Laravel, Symfony ou outra stack for selecionada, adotar a convenção nativa do framework e evitar pastas duplicadas. Não criar diretórios vazios só para aparentar implementação.

## 3. Conteúdo de cada área

- `GOVERNANCA/`: políticas locais, registo de decisões e dependências da norma superior.
- `PROMPT/`: prompts versionados com finalidade, limites, critérios de aceitação e estado.
- `GESTAO_PROJETO/`: roadmap, dependências, entregáveis e gates.
- `docs/`: requisitos, plano, riscos, validação, decisões técnicas e runbooks.
- `ARQUITETURA/`: arquitetura lógica, stack a aprovar, modelo de dados e fronteiras de confiança.
- `PRODUTO/`: âmbito, personas hipotéticas, jornadas e critérios de sucesso.
- `CLINICA/`: fontes primárias, matriz afirmação-fonte, revisão e histórico de correções.
- `SEGURANCA/`: ameaças, privacidade, resposta a incidentes e critérios de bloqueio.
- `QUALIDADE_TESTES/`: estratégia de testes e evidências por commit.
- `OPERACOES/`: ambientes, CI/CD, backups, restauração, monitorização e suporte.
- `app/`, `routes/`, `resources/`, `database/`: código, criados após G2 e decisão da stack.
- `tests/`: testes automatizados ligados a requisitos.
- `.github/`: automatizações e templates, sem segredos no código.

## 4. Ordem de construção

1. Completar e validar F0.
2. Construir catálogo de fontes e processo editorial em F1.
3. Aprovar stack, dados, segurança e privacidade em F2.
4. Criar fundação técnica e testes em P3.
5. Implementar apenas as funções do MVP aprovadas.
6. Validar segurança, clínica, acessibilidade e operação.
7. Executar piloto limitado e só lançar após aprovação formal.
8. Tratar módulos pessoais e integrações como fases independentes.

## 5. Regras de integridade

- Todos os documentos Markdown seguem o cabeçalho definido pela GOVERNANCA.
- Calcular SHA-256 canónico segundo a regra oficial, removendo somente as duas linhas de controlo especificadas; não deixar hashes fictícios.
- Não declarar esta estrutura como código implementado.
- Não guardar dados reais de saúde, credenciais, tokens, backups ou dumps no Git.
- Alterações críticas exigem revisão, testes e evidências.
- Atualizar estado e roadmap com factos verificáveis.

## 6. Próxima ação

Usar este documento como proposta de estrutura, validar contra a norma de cabeçalho e calcular hashes, atualizar `README.md`/`STATUS.md` e concluir o gate F0 antes de criar a aplicação funcional.

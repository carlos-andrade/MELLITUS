# MELLITUS — Estrutura completa do repositório

| Campo | Valor |
|---|---|
| **ID** | MEL-REPO-STRUCT-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | ESPECIFICACAO |
| **Fase** | F0 — Governação e requisitos |
| **Estado** | EM_REVISAO |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | PENDENTE_DE_CALCULO |
| **Commit de referência (versão anterior)** | N/A — documento inicial |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Responsável técnico — a formalizar |
| **Aprovador** | Pendente de aprovação formal |
| **Origem** | Pedido de estruturação completa do repositório MELLITUS |
| **Autoridade superior** | [GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA); [Governação MELLITUS](../GOVERNANCA/GOVERNANCA.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | README.md; docs/PLANO_DIRETOR.md; docs/ARQUITETURA.md; docs/REQUISITOS.md; docs/RISCOS.md |

## 1. Objetivo

Organizar o repositório distinguindo ficheiros existentes de estrutura futura. A existência desta especificação não declara a aplicação implementada.

## 2. Ficheiros existentes confirmados

No branch `main), durante a preparação foram confirmados:
- `README.md`, `STATUS.md`
- `docs/PLANO_DIRETOR.md`, `docs/REQUISITOS.md`, `docs/RISCOS.md`, `docs/VALIDACAO.md`
- `GOVERNANCA/GOVERNANCA.md`, `GOVERNANCA/REGISTO_DECISOES.md`
- `CLINICA/FONTES_E_REVISAO.md`
- `PROMPT/README.md`, `PROMPT/PROMPT-ESPECIALISTA-DIABETES-MELLITUS.md`

## 3. Estrutura-alvo recomendada

```text
MELLITUS/
├── README.md
├── STATUS.md
├── CHANGELOG.md
├── CONTRIBUTING.md
├── SECURITY.md
├── .gitignore
├── .editorconfig
├── .env.example
├── app/
│   ├── Domain/{Content,Sources,EditorialReview}/
│   ├── Application/{Content,Search,UseCase}/
│   ├── Infrastructure/{Persistence,Logging,Security}/
│   └── Presentation/Http/{Controllers,Middleware}/
├── config/
├── database/{migrations,seeds}/
├── public/{assets/css,assets/js,assets/images}/
├── resources/{views,content,locales/pt-PT}/
├── routes/
├── storage/{cache,logs}/
├── tests/{Unit,Integration,Feature,Security,Accessibility}/
├── scripts/
├── docs/{ADR/}
├── CLINICA/{FONTES_E_REVISAO.md,CATALOGO_FONTES.md,MATRIZ_AFIRMACOES.md,HISTORICO_REVISOES.md}
├── GOVERNANCA/{GOVERNANCA.md,REGISTO_DECISOES.md,REGISTO_EXCECOES.md,GATES/}
├── PROMPT/{README.md,testes/}
├── CARTAS/
├── LAYOUT/
├── .github/{ISSUE_TEMPLATE/,workflows/}
└── deploy/{examples/}
```

## 4. Regras

- Não criar diretórios vazios para simular implementação; usar README para explicar propósito e estado.
- Nunca versionar credenciais, ficheiros .env reais, dumps, backups ou dados de saúde identificáveis.
- `public/` é a única raiz exposta ao servidor web; código, configuração, logs e dependências ficam fora dela.
- Seeds e exemplos usam dados sintéticos.
- CLINICA mantém fontes, alegações, revisão e histórico rastreáveis.
- PROMPT, CARTAS e LAYOUT seguem a cadeia da GOVERNANCA.
- CI não faz deploy de produção sem aprovação explícita e ambiente protegido.
- Todos os Markdown seguem o cabeçalho normativo; o hash calcula-se após fechar o conteúdo.

## 5. Ordem de construção

1. Fechar F0: âmbito, responsáveis, critérios e gates.
2. Completar requisitos e matriz de rastreabilidade.
3. Aprovar arquitetura, modelo de dados e avaliação de riscos (G2).
4. Preparar código, convenções, testes e CI.
5. Implementar MVP educativo e fluxo editorial.
6. Validar acessibilidade, segurança, privacidade e conteúdo.
7. Executar piloto depois dos gates.
8. Avaliar isoladamente funções autenticadas ou dados de saúde.

## 6. Critérios de aceitação

Estrutura existente/proposta claramente diferenciadas; fronteiras claras; sem segredos ou dados indevidos; código fora de `public/`; rastreabilidade requisito/teste/gate; estados não confundem documentação com execução.

## 7. Próxima ação

Aprovar estrutura-alvo e criar pastas técnicas após decisão de stack e G2.

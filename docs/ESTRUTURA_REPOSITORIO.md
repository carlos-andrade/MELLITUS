# MELLITUS — Estrutura completa do repositório

| Campo | Valor |
|---|---|
| **ID** | MEL-REPO-STRUCT-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | ESPECIFICACAO |
| **Fase** | F0 — Governação e requisitos |
| **Estado** | EM_REVISAO |
| **Versão** | 1.0.1 |
| **SHA-256 (conteúdo canónico)** | PENDENTE_DE_CALCULO |
| **Commit de referência (versão anterior)** | N/A — versão inicial revista |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Responsável técnico — a formalizar |
| **Aprovador** | Pendente de aprovação formal |
| **Origem** | Pedido de estruturação completa do repositório MELLITUS |
| **Autoridade superior** | [GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA); [Governação MELLITUS](../GOVERNANCA/GOVERNANCA.md); [norma de cabeçalho](https://github.com/carlos-andrade/GOVERNANCA/blob/main/CABE%C3%87ALHO/NORMA-CABECALHO-PADRAO.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | README.md; docs/PLANO_DIRETOR.md; docs/ARQUITETURA.md; docs/REQUISITOS.md; docs/RISCOS.md; ESTRUTURA_PROJETO.md |

## 1. Objetivo

Organizar o repositório distinguindo ficheiros existentes, documentos de planeamento e código futuro. A existência desta especificação não declara a aplicação implementada.

## 2. Estado do inventário

O inventário Git consultado no branch `main` confirmou documentação de governação, requisitos, plano diretor, riscos, validação, fontes clínicas, prompts, cartas, layout, segurança, contribuição, changelog e estado, além de novas especificações de arquitetura, produto, testes e operações. Os caminhos devem voltar a ser confirmados antes de qualquer mudança em lote.

## 3. Árvore-alvo

```text
MELLITUS/
├── README.md
├── STATUS.md
├── ESTRUTURA_PROJETO.md
├── LICENSE
├── CHANGELOG.md
├── CONTRIBUTING.md
├── SECURITY.md
├── .editorconfig
├── .env.example
├── GOVERNANCA/
│   ├── GOVERNANCA.md
│   ├── REGISTO_DECISOES.md
│   └── REGISTO_EXCECOES.md
├── PROMPT/
│   ├── README.md
│   ├── PROMPT-ESPECIALISTA-DIABETES-MELLITUS.md
│   └── testes/
├── CARTAS/
├── LAYOUT/
├── GESTAO_PROJETO/
│   └── ROADMAP.md
├── PRODUTO/
│   └── README.md
├── ARQUITETURA/
│   ├── README.md
│   └── MODELO_DE_DADOS.md
├── CLINICA/
│   ├── FONTES_E_REVISAO.md
│   ├── CATALOGO_FONTES.md
│   ├── ARTIGOS/
│   └── HISTORICO_CORRECOES.md
├── SEGURANCA/
│   └── README.md
├── QUALIDADE_TESTES/
│   └── README.md
├── OPERACOES/
│   └── README.md
├── docs/
│   ├── PLANO_DIRETOR.md
│   ├── REQUISITOS.md
│   ├── RISCOS.md
│   ├── VALIDACAO.md
│   ├── ARQUITETURA.md
│   ├── MODELO_DADOS.md
│   ├── SEGURANCA_PRIVACIDADE.md
│   ├── OPERACOES.md
│   ├── ESTRUTURA_REPOSITORIO.md
│   ├── API.md
│   ├── ADR/
│   └── RUNBOOKS/
├── app/                    # código futuro após aprovação G2
│   ├── Domain/
│   ├── Application/
│   ├── Infrastructure/
│   └── Presentation/
├── config/                 # stack dependente de G2
├── database/
│   ├── migrations/
│   ├── seeds/              # apenas dados sintéticos/públicos
│   └── factories/
├── public/                 # única raiz exposta pelo servidor web
│   └── assets/
├── resources/
│   ├── views/
│   ├── content/
│   └── locales/pt-PT/
├── routes/
├── storage/                # runtime fora do Git
├── tests/
│   ├── Unit/
│   ├── Integration/
│   ├── Feature/
│   ├── Security/
│   └── Accessibility/
├── scripts/
├── deploy/                 # exemplos sem segredos
└── .github/
    ├── ISSUE_TEMPLATE/
    ├── PULL_REQUEST_TEMPLATE.md
    └── workflows/          # CI após decisão técnica
```

A árvore é um alvo de referência, não uma declaração de que todos os diretórios estejam criados ou de que o framework esteja escolhido. Se Laravel, Symfony ou outra stack for selecionada, adotar as convenções próprias e evitar pastas redundantes. Não criar diretórios vazios apenas para aparentar implementação.

## 4. Regras técnicas e de segurança

- Não versionar credenciais, `.env` real, dumps, backups ou dados de saúde identificáveis.
- `public/` deve ser a única raiz exposta pelo servidor web.
- Seeds, fixtures e exemplos usam dados fictícios, sintéticos ou públicos com uso permitido.
- CLINICA mantém fonte, afirmação sustentada, revisão, versão e histórico.
- PROMPT, CARTAS e LAYOUT preservam a cadeia documental da GOVERNANCA.
- CI não publica para produção sem ambiente protegido e autorização explícita.
- Todo o Markdown segue a norma de cabeçalho; o hash canónico só se declara após cálculo conforme a norma.
- Documento planeado não equivale a código executável nem a controlo implementado.
- Alterações materiais exigem revisão, testes, rastreabilidade e plano de reversão.

## 5. Ordem de construção

1. Fechar F0: âmbito, responsáveis, critérios de aceitação e gates.
2. Validar fontes e fluxo editorial em F1.
3. Aprovar stack, arquitetura, modelo de dados, ameaças e privacidade em G2.
4. Criar convenções de código, testes e CI.
5. Implementar apenas o MVP educativo aprovado.
6. Validar acessibilidade, segurança, privacidade e conteúdo.
7. Executar piloto após gates operacionais e autorização.
8. Avaliar separadamente contas, dados pessoais, dispositivos ou IA clínica.

## 6. Critérios de aceitação

- Inventário coerente com o repositório real.
- Documentos classificados e IDs únicos.
- Cabeçalhos e hashes verificados conforme a norma.
- Separação explícita entre planeamento e implementação.
- Ausência de segredos ou dados indevidos no Git.
- Rastreabilidade entre requisitos, riscos, testes e gates.
- Stack e modelo de dados sujeitos a decisão competente.

## 7. Próxima ação

Validar o inventário e os cabeçalhos dos documentos existentes, calcular hashes canónicos conforme a norma oficial e registar a decisão G0/G1 antes de criar código da aplicação.

# MELLITUS — Arquitetura técnica proposta

| Campo | Valor |
|---|---|
| **ID** | MEL-ARCH-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | ARQUITETURA |
| **Fase** | F2 — Arquitetura e proteção de dados |
| **Estado** | EM_REVISAO |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | PENDENTE_DE_CALCULO |
| **Commit de referência (versão anterior)** | N/A — documento inicial |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Responsável técnico — a formalizar |
| **Aprovador** | Pendente de aprovação do desenho (G2) |
| **Origem** | Plano diretor, requisitos iniciais e regras GOVERNANCA |
| **Autoridade superior** | [GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA); [Governação MELLITUS](../GOVERNANCA/GOVERNANCA.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | docs/PLANO_DIRETOR.md; docs/REQUISITOS.md; docs/RISCOS.md; docs/VALIDACAO.md |

## 1. Objetivo e estado

Arquitetura de referência proposta, não prova de implementação, aprovação G2, segurança testada ou prontidão de produção. A decisão final depende dos requisitos, custos, alojamento e avaliação de privacidade.

## 2. Princípios

- Começar por um MVP educativo de baixo risco, sem contas pessoais nem recolha de dados de saúde.
- Preferir aplicação modular simples a microserviços prematuros.
- Separar conteúdo editorial público de qualquer área autenticada futura.
- Manter domínio, serviços de aplicação, infraestrutura e apresentação separados.
- Incorporar segurança, privacidade, acessibilidade, observabilidade e recuperação desde a conceção.
- Manter dependências mínimas e suportadas; configuração por ambiente; segredos fora do repositório.
- Alterações persistentes devem ser migráveis, rastreáveis e recuperáveis.
- Funcionalidades clínicas personalizadas ficam fora do MVP e exigem nova avaliação de risco, finalidade e regulamentação.

## 3. Arquitetura lógica

```text
Navegador
  -> HTTPS e políticas de segurança
  -> Apresentação / controladores HTTP
  -> Validação de pedidos
  -> Serviços de aplicação
  -> Domínio: conteúdo, fontes, revisão, pesquisa
  -> Interfaces de repositório
  -> Persistência editorial (apenas se necessária)
  -> Logs minimizados, métricas e alertas
```

No MVP, páginas podem ser geradas a partir de conteúdo versionado se isso satisfizer pesquisa, publicação e revisão. Não introduzir uma base de dados sem necessidade documentada.

## 4. Stack técnica proposta a validar

- PHP numa versão suportada no momento da implementação.
- PHP modular; framework apenas após decisão arquitetural registada.
- HTML semântico, CSS responsivo e JavaScript mínimo.
- Markdown versionado ou sistema editorial aprovado.
- PostgreSQL ou MySQL/MariaDB apenas se requisitos justificarem persistência.
- Composer quando forem adotadas dependências PHP.
- GitHub Actions para lint, testes e análise estática depois de configurar e validar workflows.
- Alojamento por escolher com base em segurança, localização dos dados, recuperação e orçamento.

Nenhuma framework, versão ou fornecedor está selecionado até registo de decisão.

## 5. Estrutura-alvo de código

```text
app/
├── Domain/{Content,Sources,EditorialReview}/
├── Application/{Content,Search,UseCase}/
├── Infrastructure/{Persistence,Logging,Security}/
└── Presentation/Http/{Controllers,Middleware}/
config/
database/{migrations,seeds}/
public/{assets/css,assets/js,assets/images}/
resources/{views,content,locales/pt-PT}/
routes/
storage/{cache,logs}/
tests/{Unit,Integration,Feature,Security,Accessibility}/
scripts/
```

Esta estrutura é proposta; não significa que os componentes já existam.

## 6. Componentes e fronteiras

### MVP educativo
Página inicial, navegação, artigos, glossário, pesquisa, fonte e datas de revisão, fluxo editorial autorizado e acessibilidade. Sem perfil clínico, registo pessoal ou diagnóstico.

### Acompanhamento pessoal futuro
Exige aprovação separada de requisitos, privacidade, segurança, usabilidade e avaliação regulatória. Deve contemplar isolamento de dados por utilizador, controlo de acesso, auditoria, exportação, eliminação, retenção e resposta a incidentes. Diagnóstico, dosagem e alterações autónomas de tratamento permanecem fora do âmbito autorizado.

### Operação
Health checks sem dados sensíveis, logs minimizados, backups e restauro testados. WATCHDOG só pode ser declarado ativo após integração, testes ponta a ponta e evidência.

## 7. Segurança mínima

HTTPS; validação server-side; consultas parametrizadas se houver SQL; codificação contextual contra XSS; proteção CSRF em operações mutáveis; sessões e cookies seguros; autorização server-side; limitação de pedidos conforme risco; CSP e cabeçalhos de segurança; segredos fora do Git; dependências suportadas; erros públicos sem stack trace, segredos ou dados clínicos.

## 8. Privacidade e dados

O MVP deve evitar recolher dados de saúde identificáveis. Antes de qualquer recolha, documentar finalidade, base legal, minimização, transparência, acessos, partilha, transferências, retenção, eliminação, direitos dos titulares, incidentes e necessidade de AIPD/DPIA. Verificar obrigações aplicáveis em Portugal/UE com assessoria competente. Não alegar conformidade legal sem avaliação formal.

## 9. Decisões pendentes

- PHP modular ou framework.
- Markdown versionado ou CMS.
- Necessidade e motor da base de dados.
- Alojamento, região dos dados, recuperação e níveis de serviço.
- Autenticação, apenas se necessária.
- Plano de acessibilidade e critérios.
- CI, análise estática e testes de segurança.

Registar decisões em GOVERNANCA/REGISTO_DECISOES.md com alternativas, justificação, riscos, responsável e aprovador.

## 10. Critérios de aprovação G2

Requisitos aprovados; diagramas e fluxos de dados revistos; modelo e classificação de dados definidos; ameaças tratadas; stack e alojamento decididos; testes, recuperação e rollback planeados; revisão clínica/regulatória delimitada; decisão explícita do gate registada.

## 11. Próxima ação

Concluir requisitos e avaliar alternativas técnicas antes de criar componentes funcionais.

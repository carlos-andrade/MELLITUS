# MELLITUS — Arquitetura técnica proposta

| Campo | Valor |
|---|---|
| **ID** | MEL-ARCH-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | ARQUITETURA |
| **Fase** | F2 — Arquitetura e proteção de dados |
| **Estado** | EM_REVISAO — arquitetura estática proposta; G2 não aprovado |
| **Versão** | 1.2.0 |
| **SHA-256 (conteúdo canónico)** | 21be5ab9c3310657f9de8f2a7b7d2cd1e5f945e0c497ea216348fb695fc35cdf |
| **Commit de referência (versão anterior)** | Histórico Git preservado; SHA do commit anterior não verificado nesta atualização |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Carlos Andrade — patrocinador/responsável de produto; responsável técnico a designar |
| **Aprovador** | Pendente de decisão G2 |
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

## 3. Arquitetura lógica do MVP

Fluxo proposto:

Catálogo versionado no Git → validação futura dos metadados/URLs → geração de ficheiros estáticos → fornecedor de alojamento ainda por escolher → navegador do visitante → link externo aberto pelo visitante.

O navegador não envia formulários nem termos de pesquisa ao servidor. A pesquisa, se necessária, é local sobre os metadados já descarregados. Não há API, backend, base de dados ou sessão de utilizador no desenho-base.

## 4. Stack técnica proposta

- HTML semântico e CSS responsivo.
- JavaScript mínimo, sem bibliotecas remotas; pesquisa local apenas se necessária.
- Catálogo em JSON/CSV/Markdown versionado no Git, com esquema e validação a definir antes de construir.
- Sem framework de servidor, Composer, PHP, SQL ou CMS no MVP-base.
- CI e geração automatizada apenas após autorização G3; permissões mínimas e sem segredos de runtime.
- Fornecedor e região de alojamento ainda por selecionar. A escolha depende da análise de termos, logs, retenção, subprocessadores, localização, recuperação e custo.
- Não se assume qualquer custo ou compromisso financeiro.

## 5. Estrutura-alvo de conteúdo

- catálogo: registos SourceLink e temas de navegação;
- public: páginas HTML e ativos estáticos gerados;
- tests: validação de esquema, URLs/domínios, avisos, acessibilidade e ausência de recursos de terceiros;
- documentação: ADR, ameaças, triagem de privacidade, resultados de testes e decisões.

Esta estrutura é proposta; não significa que código ou pipeline já existam.

## 6. Componentes e fronteiras

### MVP estático

Página de entrada, navegação por temas, pesquisa local opcional, metadados de fontes oficiais, data/estado de verificação e aviso de fonte externa. Não publicar artigos clínicos próprios, resumos, traduções, interpretações ou recomendações.

### Fronteiras de confiança

- Repositório Git: integridade, controlo de alterações e identidade de colaboradores.
- Processo de build/publicação futuro: só depois de G3; não ativo.
- Fornecedor de alojamento: pode processar logs técnicos; avaliação pendente.
- Sites externos: fora do controlo direto do MELLITUS; o link não valida clinicamente o destino.

### Operação

Nenhum WATCHDOG, backup/restore, rollback ou observabilidade é declarado ativo. Estes controlos requerem escolha de alojamento, desenho operacional e evidência antes de produção.

## 7. Segurança e privacidade no desenho

- Sem contas, perfis, formulários, uploads, comentários ou dados de saúde.
- Sem analytics, cookies próprios, pixels publicitários ou recursos remotos de terceiros.
- Links HTTPS e domínios permitidos; data e estado técnico explícitos.
- Aviso visível de fonte externa e ausência de aconselhamento/validação clínica.
- Sem segredos no catálogo; histórico Git para alterações.
- Avaliar cabeçalhos de segurança e CSP conforme capacidades do fornecedor escolhido.
- Ver [modelo de ameaças](AMEACAS.md) e [triagem de privacidade](AVALIACAO_PRIVACIDADE_MVP.md).

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


## 12. Adenda G2 — 2026-10-15

A opção recomendada para o MVP é um site estático a partir de catálogo versionado, sem backend, base de dados, contas, formulários, analytics ou recursos remotos de terceiros. A pesquisa, se necessária, deve ser local no navegador. O fornecedor/região de alojamento permanece por decidir, pois logs, termos, subprocessadores, localização, recuperação e custos ainda não foram avaliados. Ver [pacote G2](../GESTAO_PROJETO/PACOTE_G2_ARQUITETURA_PRIVACIDADE.md), [ADR-001](ADR/ADR-001-ARQUITETURA-ESTATICA.md), [modelo de ameaças](AMEACAS.md) e [triagem de privacidade](AVALIACAO_PRIVACIDADE_MVP.md). Esta adenda é documental; não prova implementação nem aprova G2.

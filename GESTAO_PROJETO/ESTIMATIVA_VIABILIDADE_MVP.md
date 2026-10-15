# Estimativa preliminar de viabilidade — MVP diretório MELLITUS

| Campo | Valor |
|---|---|
| **ID** | MEL-FEAS-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | ESTIMATIVA_VIABILIDADE |
| **Fase** | F0 — Governação e requisitos |
| **Estado** | PROPOSTO — não aprovado |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | e117a89fdd88f51631b2304cb907d17cbe6ec4fc25e1725ec925cbbd6bd262b1 |
| **Commit de referência (versão anterior)** | N/A — documento inicial |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Responsável de projeto — a formalizar |
| **Aprovador** | Pendente de decisão G0/G1 |
| **Origem** | Requisitos atuais, âmbito proposto e inventário documental |
| **Autoridade superior** | [GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | [Roadmap](ROADMAP.md); [Requisitos](../docs/REQUISITOS.md); [Riscos](../docs/RISCOS.md); [issue #1](https://github.com/carlos-andrade/MELLITUS/issues/1) |

## 1. Finalidade e limites

Esta estimativa de ordem de grandeza apoia a decisão G0/G1. Não é orçamento comercial, compromisso de prazo, aprovação de arquitetura nem autorização para iniciar implementação.

O âmbito considerado é exclusivamente um diretório estático de ligações externas para páginas de entidades oficiais, com título, entidade, URL, tema, idioma/jurisdição, data da última verificação técnica e aviso de que o MELLITUS não valida o conteúdo externo. Não serão criados artigos, resumos, traduções, interpretações ou recomendações clínicas próprias. Não haverá contas de utilizador, perfis, recolha de dados pessoais de saúde, acompanhamento individual, diagnósticos nem decisões terapêuticas.

## 2. Hipóteses da estimativa

- MVP inicial com cerca de 20–30 ligações, sujeito a seleção e verificação individual.
- Idioma inicial: português; ligações para outras línguas serão identificadas explicitamente.
- Site responsivo, com navegação por temas e pesquisa textual simples.
- Dados do catálogo versionados no repositório; alterações rastreáveis por Git.
- Testes de navegação, links, acessibilidade básica, avisos de âmbito e visualização móvel/desktop.
- Sem back-end, autenticação, base de dados de pessoas, analytics invasivo ou integração clínica.
- O repositório MELLITUS é público. GitHub Pages é uma opção a avaliar, não uma decisão de arquitetura aprovada.
- Estimativas de esforço assumem uma pessoa técnica com acesso ao repositório e decisões tomadas sem longas esperas. Não incluem tempo de espera por decisões formais.

## 3. Estimativa preliminar de esforço

| Trabalho | Intervalo indicativo |
|---|---:|
| Fechar requisitos e estrutura do catálogo | 4–7 horas |
| Construir interface estática e navegação | 8–14 horas |
| Importar e validar 20–30 registos de fontes | 5–9 horas |
| Testes funcionais, acessibilidade básica e responsividade | 6–10 horas |
| CI, publicação técnica e instruções operacionais | 4–7 horas |
| Documentação, evidências e correções finais | 4–7 horas |
| **Total estimado** | **31–54 horas** |

Intervalo de planeamento indicativo: aproximadamente 4–7 dias úteis de trabalho concentrado. A duração de calendário pode aumentar devido a decisões, validação de URLs, falhas externas ou alterações de âmbito. O intervalo não é um prazo aprovado.

## 4. Custos e infraestrutura

| Item | Tratamento nesta fase |
|---|---|
| Alojamento estático | Potencialmente sem custo incremental com GitHub Pages num repositório público; confirmar limites e condições antes de decidir |
| Domínio próprio | Opcional; custo anual não cotado nesta estimativa |
| Backend e base de dados | Não necessários para o âmbito mínimo proposto |
| Monitorização automatizada de links | Fora do primeiro corte ou a avaliar como workflow de baixo risco |
| Trabalho técnico | Principal componente de custo; depende do custo/hora efetivo, ainda não fornecido |
| Manutenção | Revisão mensal inicial do catálogo é hipótese operacional, não compromisso aprovado |

Não se declara um custo monetário total enquanto o custo/hora, domínio pretendido e opção de alojamento não forem confirmados. Não instalar serviços pagos nem assumir compromissos financeiros com base neste documento.

## 5. Alternativas consideradas

| Alternativa | Vantagens | Limitações | Estado |
|---|---|---|---|
| A — Diretório estático no repositório | Simples, auditável, baixo custo, sem dados pessoais | Alterações exigem workflow editorial/Git; pesquisa limitada se crescer | Preferida para avaliação, não aprovada |
| B — CMS com back-end | Edição mais simples por utilizadores não técnicos | Mais superfície de ataque, atualizações, autenticação, operação e custos | Não preferida no MVP mínimo |
| C — Aplicação com perfis e acompanhamento pessoal | Possibilita funcionalidades individuais futuras | Introduz dados de saúde, risco de privacidade e requisitos adicionais; exige nova avaliação e gates | Excluída do MVP atual |

## 6. Critérios mensuráveis propostos

Estes critérios são propostas para ratificação, não compromissos já aprovados:

1. 100% dos registos publicados têm entidade, título, URL, tema, idioma/jurisdição e data de verificação.
2. 100% das ligações são verificadas tecnicamente no momento de publicação; falhas ficam em estado explícito e não são publicadas como PASS.
3. Cada página deixa claro que a ligação conduz a uma fonte externa e que o MELLITUS não presta aconselhamento médico nem valida clinicamente o conteúdo.
4. Zero campos, formulários ou eventos concebidos para recolher dados pessoais de saúde.
5. Testes básicos de navegação e layout móvel/desktop executados e guardados como evidência antes de qualquer piloto.
6. Cada alteração do catálogo tem histórico no Git.

## 7. Riscos, dependências e condições de paragem

- **Conteúdo externo alterado ou removido:** manter data de verificação e estado técnico; falha não pode ser mascarada como validação.
- **Ausência de revisão clínica:** restringir o produto a diretório de links e metadados; não resumir, traduzir, interpretar ou recomendar conteúdo médico.
- **Confusão sobre responsabilidade:** aviso visível junto do catálogo e dos resultados.
- **Âmbito expandido para dados pessoais de saúde:** parar a implementação dessa funcionalidade e exigir nova avaliação de privacidade, segurança e gates.
- **Responsáveis não formalizados:** não converter a estimativa em compromisso de entrega.
- **G0/G1 não aprovados:** não iniciar a implementação funcional com base nesta estimativa.

## 8. Decisão solicitada em G0/G1

A autoridade competente deverá decidir se aceita: (a) o âmbito reduzido; (b) os critérios mensuráveis; (c) a alternativa estática para avaliação; e (d) o intervalo de esforço de 31–54 horas como baseline de planeamento. A decisão deve identificar aprovador, data e evidências. Até lá, este documento permanece **PROPOSTO**.

## 9. Estado de execução

A estimativa foi documentada para tornar explícitas as hipóteses, alternativas, custos desconhecidos e riscos. Não foi executado código de produto nem assumido qualquer compromisso financeiro. G0/G1 continuam não aprovados.

# Pacote de decisão — F0 / gates G0 e G1

| Campo | Valor |
|---|---|
| **ID** | MEL-DEC-F0-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | PACOTE_DECISAO |
| **Fase** | F0 — Governação e requisitos |
| **Estado** | PRONTO_PARA_DECISAO — não aprovado |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | a05d28891f4042e00ef7678029414f4783c2fd494970f4651c30a4ebf0da5de5 |
| **Commit de referência (versão anterior)** | N/A — documento inicial |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Atribuição funcional proposta; confirmação pendente |
| **Aprovador** | Proprietário do projeto |
| **Origem** | Issue #1, requisitos, roadmap e estimativa de viabilidade |
| **Autoridade superior** | [GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA); [Constituição](https://github.com/carlos-andrade/GOVERNANCA/blob/main/CONSTITUICAO.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | [Issue #1](https://github.com/carlos-andrade/MELLITUS/issues/1); [requisitos](../docs/REQUISITOS.md); [estimativa](ESTIMATIVA_VIABILIDADE_MVP.md); [roadmap](ROADMAP.md) |

## 1. Factos confirmados e restrições

- O proprietário declarou: **não haverá revisor clínico**.
- A implementação funcional comprovada é 0%.
- O MVP proposto é um diretório estático de ligações para fontes oficiais, com metadados, pesquisa e navegação.
- Não serão redigidos, resumidos, traduzidos, interpretados nem recomendados conteúdos clínicos próprios.
- Não haverá contas, perfis, acompanhamento individual ou recolha de dados pessoais de saúde.
- Uma ligação para fonte externa não equivale a validação clínica.
- A estimativa preliminar é de 31–54 horas. Não constitui compromisso de prazo.
- Custo monetário real, custo/hora, domínio, capacidade e calendário continuam desconhecidos ou não aprovados.

## 2. Baseline proposta

**Problema:** a descoberta de fontes oficiais sobre diabetes está distribuída por vários portais e o utilizador pode não identificar facilmente a origem e a data de verificação de cada ligação.

**Beneficiário:** público que procura páginas oficiais, sem personalização nem aconselhamento clínico.

**Critérios mensuráveis propostos:**
1. Catálogo inicial de 20–30 ligações oficiais, cada uma com entidade, título, URL, tema, idioma/jurisdição e data de verificação.
2. 100% das ligações testadas tecnicamente antes da publicação; falhas identificadas como WARN/FAIL/UNKNOWN.
3. Aviso visível de fonte externa e ausência de validação clínica.
4. Zero recolha de dados pessoais de saúde; sem contas ou perfis.
5. Evidência guardada de testes de navegação, pesquisa, responsividade e acessibilidade antes de qualquer piloto.

A baseline só fica aprovada após decisão explícita do proprietário.

## 3. Papéis propostos

| Função | Proposta | Limite |
|---|---|---|
| Patrocinador e autoridade de âmbito/recursos | Carlos Andrade, proprietário do repositório | Requer confirmação explícita |
| Responsável de produto/projeto | Carlos Andrade, com acumulação de funções | Requer confirmação explícita |
| Execução técnica assistida | Assistente de IA, sob instruções do proprietário | Sem autoridade de gate, aprovação independente ou responsabilidade legal |
| Responsável de catálogo | Carlos Andrade, com apoio técnico assistido | Decisão editorial/publicação sob controlo do proprietário |
| Revisor clínico | Nenhum | Restrição explícita; conteúdo clínico próprio excluído |
| Privacidade/jurídico especializado | Não nomeado | Não recolher dados de saúde; expansão exige avaliação prévia |

Não se presume competência clínica, jurídica ou de segurança sem evidência.

## 4. Viabilidade e sensibilidade de custo

| Custo-hora hipotético | 31 horas | 54 horas |
|---:|---:|---:|
| €25/h | €775 | €1.350 |
| €50/h | €1.550 | €2.700 |
| €75/h | €2.325 | €4.050 |

Os valores são cenários aritméticos, não cotações nem custo real. Não incluem IVA, domínio, manutenção ou serviços pagos. O custo monetário permanece UNKNOWN até o proprietário indicar um custo/hora ou declarar custo laboral incremental zero. A alternativa preferida para avaliação é um diretório estático versionado em Git, sem backend ou dados pessoais.

## 5. Riscos e condições de paragem

- Links quebrados ou destinos alterados: data e estado técnico explícito; remover ou corrigir falhas.
- Confusão com aconselhamento médico: aviso visível; nenhum conteúdo clínico próprio.
- Inclusão futura de dados de saúde ou funções clínicas: parar e exigir nova avaliação e gates.
- Custo/prazo desconhecidos: não assumir compromisso financeiro nem prometer lançamento.
- Evidência ausente: UNKNOWN/pendente, nunca PASS por inferência.

## 6. Decisões necessárias para fechar F0

O proprietário deve confirmar explicitamente estas decisões na [issue #1](https://github.com/carlos-andrade/MELLITUS/issues/1), com referência a esta versão:

- [ ] **D1 — Âmbito:** aprovar o MVP reduzido e as exclusões clínicas e de dados pessoais de saúde.
- [ ] **D2 — Baseline:** aprovar problema, beneficiário e critérios mensuráveis da secção 2.
- [ ] **D3 — Papéis:** confirmar Carlos Andrade como patrocinador e responsável de produto/projeto; confirmar que o assistente de IA não aprova gates.
- [ ] **D4 — Esforço:** aceitar 31–54 horas como estimativa preliminar, sem compromisso de calendário.
- [ ] **D5 — Custo:** escolher um cenário de custo-hora, declarar custo laboral incremental zero ou manter custo monetário UNKNOWN e sem orçamento aprovado.
- [ ] **D6 — G0:** autorizar entrada do projeto com problema, beneficiário, patrocinador e responsável identificados.
- [ ] **D7 — G1:** aceitar a viabilidade preliminar e a alternativa estática, sem assumir custos não aprovados.
- [ ] **D8 — G2:** autorizar apenas preparar e avaliar arquitetura/privacidade; não autorizar construção, recolha de dados nem lançamento.

A aceitação geral anterior e a instrução “siga” não são tratadas como aprovação individual destas decisões.

## 7. Estado final da auditoria F0

**PRONTO PARA DECISÃO — NÃO CONCLUÍDO.** O pacote documental, os critérios propostos, os papéis candidatos e os cenários de custo estão consolidados. A autoridade decisória pertence ao proprietário. Até existir confirmação explícita de D1–D8, G0/G1 permanecem pendentes e a implementação funcional continua bloqueada.

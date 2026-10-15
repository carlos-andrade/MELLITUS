# Política de catálogo de fontes oficiais — MELLITUS

| Campo | Valor |
|---|---|
| **ID** | MEL-CLIN-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | POLITICA_FONTES |
| **Fase** | F1 — Catálogo de fontes oficiais |
| **Estado** | PROPOSTO |
| **Versão** | 1.1.0 |
| **SHA-256 (conteúdo canónico)** | c8404293318cf259f04e3831273e72bc61fe240e4c3f66dc0534c77a39ad38f6 |
| **Commit de referência (versão anterior)** | [a865fb67477acaf225f90523b5442b8b5a51dbb6](https://github.com/carlos-andrade/MELLITUS/commit/a865fb67477acaf225f90523b5442b8b5a51dbb6) |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Responsável pelo catálogo — a formalizar |
| **Aprovador** | Pendente de ratificação G0/G1 |
| **Origem** | Decisão explícita do proprietário de que não haverá revisor clínico |
| **Autoridade superior** | [Constituição GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA/blob/main/CONSTITUICAO.md); legislação aplicável |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | docs/REQUISITOS.md; docs/RISCOS.md; docs/VALIDACAO.md; issue #1 |
| **Escopo** | Catalogar fontes externas oficiais, sem validar clinicamente nem produzir conteúdo médico próprio |
| **Objetivo** | Facilitar acesso a fontes externas e manter ligações/metadados rastreáveis |
| **Dependências** | Lista de entidades elegíveis, verificação de URLs e responsável de catálogo |

## 1. Decisão de âmbito

O proprietário declarou que não haverá revisor clínico. Em consequência, o MVP proposto limita-se a um catálogo de ligações para páginas de entidades oficiais. O MELLITUS não redigirá, resumirá, traduzirá, interpretará nem recomendará conteúdo clínico próprio. A inclusão de uma página no catálogo não significa que o MELLITUS validou as suas afirmações clínicas.

## 2. Entidades candidatas

As entidades abaixo são candidatas para consulta; a presença nesta lista não significa que cada página tenha sido verificada ou aprovada para um tema específico.

- Direção-Geral da Saúde (DGS): https://www.dgs.pt/
- SNS 24: https://www.sns24.gov.pt/
- INFARMED: https://www.infarmed.pt/
- Agência Europeia de Medicamentos (EMA): https://www.ema.europa.eu/
- Organização Mundial da Saúde (OMS): https://www.who.int/
- International Diabetes Federation (IDF): https://idf.org/
- European Association for the Study of Diabetes (EASD): https://www.easd.org/
- National Institute for Health and Care Excellence (NICE): https://www.nice.org.uk/

A inclusão de outras entidades exige critério de elegibilidade explícito e identificação da natureza da fonte.

## 3. Metadados mínimos por registo

- ID estável do registo.
- Nome da entidade e título da página.
- URL canónica e domínio observado.
- Tema de navegação, sem inferência clínica.
- Jurisdição e idioma, quando verificáveis.
- Data de verificação da ligação.
- Estado técnico: PASS, WARN, FAIL ou UNKNOWN.
- Nota explícita: conteúdo externo, não validado clinicamente pelo MELLITUS.
- Histórico de correções e remoções.

Não guardar credenciais, dados de saúde nem informação pessoal desnecessária no catálogo.

## 4. Verificação operacional

1. Abrir a URL e confirmar que responde.
2. Confirmar que o domínio corresponde à entidade identificada.
3. Registar título, idioma, jurisdição e data de verificação.
4. Não inferir que uma ligação ativa significa que o conteúdo está atual ou clinicamente correto.
5. Marcar falhas ou incertezas como FAIL/UNKNOWN, sem as apresentar como fontes verificadas.
6. Remover ou desativar ligações quebradas ou cuja origem não possa ser confirmada.
7. Manter histórico de alterações.

## 5. Limites

Ficam fora do MVP: artigos clínicos originais, resumos, traduções, interpretações, recomendações personalizadas, triagem, diagnóstico, prescrição, ajuste de medicação e recolha de dados pessoais de saúde. A ausência de revisor clínico não dispensa avaliação legal, segurança, privacidade nem gates de governação. Qualquer mudança de âmbito exige nova avaliação formal.

## 6. Estado e próxima ação

Esta política é uma proposta alinhada com a decisão de não nomear revisor clínico. O catálogo e as ligações ainda não foram validados operacionalmente. Ratificar o âmbito reduzido e concluir G0/G1 antes de iniciar implementação funcional.

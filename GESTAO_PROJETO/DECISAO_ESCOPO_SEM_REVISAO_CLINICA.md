# Decisão de âmbito — ausência de revisor clínico

| Campo | Valor |
|---|---|
| **ID** | MEL-DEC-SCOPE-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | DECISAO_ESCOPO |
| **Fase** | F0 — Governação e requisitos |
| **Estado** | PROPOSTO |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | 7a4c1ebf8b246fde04a62b18f46ad319e7215727b114a60267e739a47e4991ed |
| **Commit de referência (versão anterior)** | N/A — documento inicial |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Responsável de projeto — a formalizar |
| **Aprovador** | Pendente de decisão G0/G1 |
| **Origem** | Comentário do proprietário na issue #1: “NÃO TEREMOS REVISOR.” |
| **Autoridade superior** | [GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | docs/REQUISITOS.md; docs/RISCOS.md; docs/MATRIZ_RASTREABILIDADE.md; GESTAO_PROJETO/ROADMAP.md; issue #1 |

## 1. Decisão explícita registada

O proprietário declarou que não será nomeado revisor clínico. Este documento regista essa restrição; não a transforma numa autorização para publicar conteúdo clínico sem revisão.

## 2. Consequência de segurança proposta

Propõe-se restringir o MVP a um diretório de fontes oficiais com pesquisa, navegação, ligações diretas e metadados. O MELLITUS não redigirá, resumirá, traduzirá, interpretará nem recomendará conteúdo clínico próprio. A inclusão de uma ligação não equivale a validação clínica da página externa. O MVP não recolherá dados pessoais de saúde.

## 3. Âmbito incluído na proposta

- Catálogo de entidades e páginas oficiais.
- Ligações diretas para a origem externa.
- Nome da entidade, título, URL, jurisdição/idioma e data de verificação.
- Pesquisa e navegação por metadados.
- Aviso visível de que o MELLITUS não valida clinicamente o conteúdo externo.
- Processo técnico rastreável para testar, corrigir e remover ligações.

## 4. Exclusões

- Conteúdo clínico escrito, resumido, traduzido ou interpretado pelo projeto.
- Diagnóstico, triagem conclusiva, prescrição, ajuste de medicação e aconselhamento personalizado.
- Registos, perfis ou histórico de dados pessoais de saúde.
- Alegação de validação clínica de páginas externas.

## 5. Controlos e riscos residuais

A verificação de URL/domínio confirma apenas aspetos técnicos e de proveniência; não certifica correção, atualidade ou adequação clínica. Os links devem ter data de verificação e estado PASS, WARN, FAIL ou UNKNOWN. A ausência de evidência não é sucesso. Continuam necessários avaliação legal e de privacidade aplicável, segurança, acessibilidade, testes e aprovação dos gates relevantes.

## 6. Estado e condição de avanço

**Estado: PROPOSTO, não aprovado.** O âmbito reduzido deve ser ratificado no G0/G1. Continuam pendentes a formalização do responsável de projeto/produto, a evidência de viabilidade e a decisão explícita do gate. Não iniciar implementação funcional nem recolha de dados pessoais de saúde por inferência.

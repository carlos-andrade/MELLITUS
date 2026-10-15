# MELLITUS — Modelo conceptual de dados

| Campo | Valor |
|---|---|
| **ID** | MEL-DATA-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | MODELO_DADOS |
| **Fase** | F2 — Arquitetura e proteção de dados |
| **Estado** | EM_REVISAO |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | 1453d1f1723ebc10858b15efd633bd577488fffe723591ccaac55496aff71431 |
| **Commit de referência (versão anterior)** | N/A — documento inicial |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Responsável de dados — a formalizar |
| **Aprovador** | Pendente de aprovação G2 |
| **Origem** | Plano diretor e requisitos MELLITUS |
| **Autoridade superior** | [GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA); [governação MELLITUS](../GOVERNANCA/GOVERNANCA.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | docs/REQUISITOS.md; docs/ARQUITETURA.md; docs/RISCOS.md |

## 1. Estado e minimização

Modelo conceptual, não esquema SQL implementado. O MVP educativo deve funcionar sem contas pessoais nem dados de saúde individualizados. Entidades pessoais futuras estão bloqueadas até aprovação própria de requisitos, privacidade e segurança.

## 2. Entidades editoriais propostas

**Article:** id, slug, title, summary, body, status, published_at, reviewed_at, review_due_at, locale, version.

**Source:** id, organisation, title, url, published_at, accessed_at, version, source_type.

**Claim:** id, afirmação clínica exata, artigo, fonte, síntese/limitações da evidência, estado de revisão, papel do revisor e data de revisão.

**EditorialReview:** id, artigo, tipo de revisão, resultado, data, papel do revisor e notas.

Estes registos devem demonstrar a revisão editorial sem expor dados pessoais desnecessários.

## 3. Extensão pessoal condicional

Entidades candidatas, bloqueadas até aprovação: Account, ConsentRecord, GlucoseRecord, HealthEntry, ExportJob e AccessAudit. Não implementar no MVP. Consentimento não substitui automaticamente a base legal; avaliar finalidade, necessidade e AIPD/DPIA com assessoria competente.

## 4. Classificação

| Categoria | Exemplo | Regra |
|---|---|---|
| Público | Conteúdo publicado, fontes públicas | Publicar após revisão/autorização |
| Interno | Rascunhos, decisões | Acesso por função |
| Confidencial operacional | Configuração e incidentes | Acesso mínimo |
| Dados pessoais | Identificador futuro de conta | Minimizar e definir retenção |
| Dados de saúde | Registos glicémicos | Não recolher no MVP |
| Segredos | Tokens e chaves | Nunca versionar |

## 5. Ciclo de vida

Definir unidades, validação, fuso horário, proveniência, retenção, eliminação incluindo backups, exportação segura, acessos e migrações. Não colocar dados de saúde em URLs, logs ou ferramentas analíticas. Testes usam dados sintéticos.

## 6. Critérios G2

Inventário e finalidades aprovados; fluxos e classificação revistos; acessos, retenção, exportação, eliminação e backups definidos; avaliação legal/privacidade documentada; sem dados reais nos exemplos.

## 7. Próxima ação

Confirmar âmbito educativo e método editorial antes de selecionar persistência ou esquema definitivo.

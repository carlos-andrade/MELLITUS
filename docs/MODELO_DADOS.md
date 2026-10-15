# MELLITUS — Modelo conceptual de dados

| Campo | Valor |
|---|---|
| **ID** | MEL-DATA-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | MODELO_DADOS |
| **Fase** | F2 — Arquitetura e proteção de dados |
| **Estado** | EM_REVISAO — modelo do MVP reduzido; G2 pendente |
| **Versão** | 1.1.0 |
| **SHA-256 (conteúdo canónico)** | 6671d5d738e54c09792197ae788bcee64d031d88753cb591b8eaae148d5440e9 |
| **Commit de referência (versão anterior)** | Histórico Git preservado; SHA do commit anterior não verificado nesta atualização |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Carlos Andrade — responsável de produto; responsável técnico/dados a designar |
| **Aprovador** | Pendente de ratificação G2 |
| **Origem** | Plano diretor e requisitos MELLITUS |
| **Autoridade superior** | [GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA); [governação MELLITUS](../GOVERNANCA/GOVERNANCA.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | docs/REQUISITOS.md; docs/ARQUITETURA.md; docs/RISCOS.md |

## 1. Estado e minimização

Modelo conceptual, não esquema SQL implementado. O MVP educativo deve funcionar sem contas pessoais nem dados de saúde individualizados. Entidades pessoais futuras estão bloqueadas até aprovação própria de requisitos, privacidade e segurança.

## 2. Modelo de dados proposto para o MVP estático

**SourceLink:** source_id estável, organização oficial, título oficial, URL HTTPS, tema(s), jurisdição, idioma, data de verificação técnica, estado técnico PASS/WARN/FAIL/UNKNOWN.

**Topic:** identificador e rótulo de navegação, sem descrição clínica própria.

O catálogo será versionado em ficheiros no Git; não há persistência em base de dados. Não criar Article, Claim ou EditorialReview no MVP, pois implicariam texto editorial ou revisão clínica fora do âmbito aprovado. O título deve refletir o título da página externa, não um resumo redigido pelo MELLITUS.

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


## 8. Adenda G2 — 2026-10-15

O modelo do MVP foi reduzido a SourceLink e Topic. A extensão pessoal (Account, ConsentRecord, GlucoseRecord, HealthEntry, ExportJob e AccessAudit) continua BLOQUEADA e não deve ser criada como parte do MVP. Nenhum dado de saúde individualizado será recolhido. Ver [pacote G2](../GESTAO_PROJETO/PACOTE_G2_ARQUITETURA_PRIVACIDADE.md).

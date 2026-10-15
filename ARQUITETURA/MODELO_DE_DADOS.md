# Modelo conceptual de dados — MELLITUS

| Campo | Valor |
|---|---|
| **ID** | MEL-ARCH-DADOS-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | MODELO_DADOS |
| **Fase** | F2 — Arquitetura e proteção de dados |
| **Estado** | EM_REVISAO |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | bb8180b906414127a840b0e0604978d8cc1ba9f9a8685630b3d436c028e57f3a |
| **Commit de referência (versão anterior)** | N/A — documento inicial |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Responsável técnico/dados — a formalizar |
| **Aprovador** | Pendente de aprovação G2 |
| **Origem** | Requisitos MELLITUS |
| **Autoridade superior** | [GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA); [governação MELLITUS](../GOVERNANCA/GOVERNANCA.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | docs/REQUISITOS.md; docs/RISCOS.md; ARQUITETURA/README.md |

## 1. Princípio

Este é um modelo conceptual para discussão. Não constitui esquema de base de dados implementado nem autoriza recolha de dados. O MVP deverá evitar dados de saúde identificáveis sempre que possível.

## 2. Entidades do MVP educativo

### Article
- `id`: identificador interno.
- `slug`: identificador público único.
- `title`, `summary`, `body`: conteúdo editorial.
- `status`: rascunho, em revisão, aprovado, publicado ou retirado.
- `version`: versão editorial.
- `published_at`, `reviewed_at`, `next_review_at`.
- `created_at`, `updated_at`.

### Source
- `id`, `title`, `publisher`, `url`.
- `publication_date`, `last_verified_at`, `version_or_revision`.
- `source_type`, `jurisdiction`, `accessed_at`.
- `status` e notas sobre limitações.

### ArticleSource
- Associação entre artigo, fonte e afirmação sustentada.
- Secção ou afirmação coberta, observações e versão do artigo.

### EditorialReview
- Artigo/versão, revisor autorizado, decisão, data, observações e ligações a evidências.
- Não deve guardar informação pessoal desnecessária.

### AuditEvent
- Ator técnico pseudónimo ou ID de conta quando necessário, ação, recurso, data, resultado e contexto técnico minimizado.
- Nunca colocar palavras-passe, tokens, conteúdo completo de registos de saúde ou segredos.

## 3. Entidades pessoais — bloqueadas até G2

Se e somente se forem aprovadas: `UserAccount`, `ConsentRecord` (quando necessário e validado), `HealthEntry` (valor, unidade, data/hora e origem), `ExportRequest`, `DeletionRequest` e `AccessAudit`. Estas entidades são alternativas de desenho, não autorização para recolher dados. Finalidade, base legal, necessidade de AIPD/DPIA, retenção e direitos exigem avaliação por responsáveis competentes.

## 4. Regras de integridade

- Usar IDs não adivinháveis nas superfícies públicas, quando adequado, sem substituir autorização.
- Garantir integridade referencial e restrições de domínio.
- Datas armazenadas em UTC e apresentadas em fuso explícito.
- Valores clínicos, se aprovados, exigem unidade, contexto de medição, origem e validação; não inferir diagnóstico.
- Eliminação lógica só se for justificada; documentar efeitos em cópias de segurança e obrigações de retenção.
- Nunca utilizar dados pessoais reais em fixtures, demonstrações ou testes automatizados.

## 5. Segurança e acesso

Todos os acessos a registos privados devem ser autorizados no servidor e delimitados ao titular ou a uma função explicitamente autorizada. Proibir pesquisa pública, indexação por motores de busca e analytics sobre registos pessoais. Acesso de suporte deve ser excecional, justificado, auditável e limitado.

## 6. Migrações e recuperação

Versionar migrações; testar atualização e rollback em ambientes descartáveis. Definir backup, encriptação, retenção e ensaios antes de armazenar dados pessoais. Testar restauração e documentar resultados.

## 7. Próxima ação

Converter o modelo conceptual em esquema lógico apenas depois de aprovar âmbito, classificação de dados, base legal, modelo de ameaças, estratégia de retenção e G2.

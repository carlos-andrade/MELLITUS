# Segurança, privacidade e conformidade — MELLITUS

| Campo | Valor |
|---|---|
| **ID** | MEL-SEC-README-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | PLANO_SEGURANCA |
| **Fase** | F2 — Arquitetura e proteção de dados |
| **Estado** | EM_REVISAO |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | PENDENTE_CALCULO |
| **Commit de referência (versão anterior)** | N/A — documento inicial |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Segurança/privacidade — a formalizar |
| **Aprovador** | Pendente de avaliação especializada |
| **Origem** | Governação e requisitos MELLITUS |
| **Autoridade superior** | [GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA); [governação MELLITUS](../GOVERNANCA/GOVERNANCA.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | docs/RISCOS.md; docs/VALIDACAO.md; ARQUITETURA/MODELO_DE_DADOS.md |

## 1. Estado

Este plano enumera controlos exigidos para avaliação. Não declara que estejam implementados, testados ou certificados. Responsáveis técnicos, de privacidade e conformidade ainda devem ser nomeados.

## 2. Controlos mínimos

- Identificar ativos, ameaças, fronteiras de confiança e impacto de falha.
- Definir inventário de dados, finalidade, classificação, base legal, acesso, retenção, eliminação e partilha.
- Minimizar dados pessoais e excluir dados de saúde do MVP quando não necessários.
- Autenticação robusta para áreas administrativas; autorização no servidor para cada recurso.
- Armazenar segredos em mecanismos de configuração seguros, nunca no Git.
- Validar e codificar entradas/saídas; consultas parametrizadas; proteção CSRF quando aplicável.
- Limitar tentativas e abusos sem criar bloqueios que coloquem utilizadores em risco.
- TLS, configuração de cookies segura e cabeçalhos HTTP adequados para o contexto.
- Dependências e imagens atualizadas com revisão de vulnerabilidades.
- Atualizações de segurança, backups, restauração, gestão de incidentes e rollback documentados.
- Logs com acesso controlado e minimização; nunca guardar palavras-passe, tokens ou dados clínicos completos desnecessários.
- Separação entre desenvolvimento, teste e produção; dados sintéticos em ambientes não produtivos.
- Revisão independente antes de tratamento de dados sensíveis ou exposição pública relevante.

## 3. Privacidade e dados de saúde

Antes de recolher dados de saúde, avaliar finalidade, necessidade, minimização, base legal e condição aplicável ao tratamento, transparência, direitos, processadores, transferências, prazos de retenção e necessidade de AIPD/DPIA. A avaliação deve ser feita por responsáveis competentes; este documento não substitui aconselhamento jurídico.

## 4. Segurança clínica

O conteúdo educativo necessita de origem rastreável, revisão adequada e fluxo de correção/retirada. Funções que façam diagnóstico, recomendação personalizada, dose, previsão ou suporte a decisões clínicas ficam fora do MVP e bloqueadas até avaliação de finalidade, evidência, risco e requisitos legais/regulatórios.

## 5. Modelo de ameaças

Analisar, no mínimo: acesso não autorizado, IDOR/BOLA, roubo de credenciais, injeção, XSS, CSRF, abuso de formulários, exposição de ficheiros/backups, dependências vulneráveis, configuração insegura, fuga de dados em logs, erro editorial clínico, indisponibilidade e falha de restauração.

Para cada ameaça, registar ativo, cenário, impacto, probabilidade, controlos preventivos/detetivos, risco residual, responsável e evidência de teste.

## 6. Resposta a incidentes

Definir canal de reporte, triagem, gravidade, contenção, preservação de evidências, comunicação interna/externa, obrigações legais, recuperação e lições aprendidas. Prazos e destinatários devem ser validados legalmente e não presumidos neste plano.

## 7. Critérios de bloqueio de lançamento

Bloquear lançamento se houver vulnerabilidade crítica sem tratamento, acesso não autorizado demonstrado, exposição de dados, backup sem restauração testada, conteúdo clínico de alto risco sem revisão ou responsabilidades operacionais não atribuídas. Exceções exigem registo formal e não podem dispensar obrigação legal.

## 8. Próxima ação

Completar avaliação de risco e privacidade, modelo de ameaças, plano de resposta a incidentes e evidência de controlos. Gate G2 não pode ser considerado aprovado apenas pela existência deste documento.

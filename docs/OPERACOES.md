# MELLITUS — Operação, observabilidade e recuperação

| Campo | Valor |
|---|---|
| **ID** | MEL-OPS-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | PLANO_OPERACIONAL |
| **Fase** | F2 — Arquitetura e proteção de dados |
| **Estado** | EM_REVISAO |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | 7b580b4647b54c2885b445e5ddf8e70444292f6c520396d5bdfe342e507f417b |
| **Commit de referência (versão anterior)** | N/A — documento inicial |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Responsável de operações — a formalizar |
| **Aprovador** | Pendente de aprovação G4 |
| **Origem** | Governação MELLITUS, roadmap e arquitetura proposta |
| **Autoridade superior** | [GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA); [governação MELLITUS](../GOVERNANCA/GOVERNANCA.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | docs/ARQUITETURA.md; docs/SEGURANCA_PRIVACIDADE.md; docs/VALIDACAO.md; docs/RISCOS.md |

## 1. Estado

Plano proposto. Não existe evidência de serviço implantado, métricas de produção, alertas ativos, backup executado ou SLA aprovado.

## 2. Ambientes

- Desenvolvimento: dados sintéticos e acessos de desenvolvimento.
- Teste: configuração próxima do destino; sem dados reais salvo autorização e controlos.
- Produção: configuração mínima, segredos geridos, acessos restritos, logs protegidos e mudanças aprovadas.

Não reutilizar credenciais entre ambientes.

## 3. Observabilidade

Quando implementado, monitorizar disponibilidade HTTP/latência, erros e dependências, capacidade, backups/restauros, certificados e eventos de segurança relevantes. Definir limiar, gravidade, destinatário, ação, escalonamento e encerramento. Nunca incluir valores glicémicos, nomes, tokens ou dados de saúde nos logs. Testar a falha do monitor nos âmbitos críticos. WATCHDOG só é ativo após integração, teste ponta a ponta e evidência.

## 4. Backup e recuperação

Antes do lançamento, definir RPO/RTO; inventário e frequência de backups; encriptação, acesso e retenção; proteção contra alteração; restauro completo testado; responsáveis e validação de integridade; rollback testado.

## 5. Publicação e mudança

Cada release exige versão, testes, changelog, decisão, plano de observação e rollback. CI não equivale a publicação. Não lançar produção sem aprovação e ambiente protegido. Fluxo: proposta → impacto → revisão → testes → aprovação → publicação → verificação → correção/rollback → evidências.

## 6. Critérios G4

Owner operacional e suporte definidos; alertas testados; backup/restauro e rollback demonstrados; vulnerabilidades bloqueadoras resolvidas; procedimento de incidente definido; controlos de privacidade, segurança e revisão clínica aceites; evidência operacional recente.

## 7. Próxima ação

Escolher ambiente e níveis de serviço após arquitetura; escrever runbooks e testar recuperação antes de G4.

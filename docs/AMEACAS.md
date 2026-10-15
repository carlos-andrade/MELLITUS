# Modelo de ameaças — MELLITUS MVP estático

| Campo | Valor |
|---|---|
| **ID** | MEL-THREAT-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | MODELO_AMEACAS |
| **Fase** | G2 — Arquitetura e privacidade |
| **Estado** | EM_REVISAO — modelo documental; sem teste técnico executado |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | f6725e4bf2d3d418b03c4768f077aaf644e14e4f7e98ce518fd46c643bccced4 |
| **Commit de referência (versão anterior)** | N/A — documento inicial G2 |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Carlos Andrade — responsável de produto; responsável técnico a designar |
| **Aprovador** | Pendente de ratificação G2 |
| **Origem** | G0/G1 aprovados; autorização limitada para preparação e avaliação de G2 |
| **Autoridade superior** | [GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA); [Constituição](https://github.com/carlos-andrade/GOVERNANCA/blob/main/CONSTITUICAO.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | [arquitetura](ARQUITETURA.md); [segurança e privacidade](SEGURANCA_PRIVACIDADE.md); [riscos](RISCOS.md); [validação](VALIDACAO.md) |

## 1. Objetivo e limites

Identificar ameaças plausíveis para um diretório público estático de links oficiais sobre diabetes. Não é teste de penetração nem certificação. Exclui contas, dados de saúde, backend, uploads, comentários, analytics e conteúdo clínico próprio.

## 2. Ativos e fronteiras

| Ativo | Classificação | Observação |
|---|---|---|
| Catálogo e interface | Público | Alterações rastreáveis |
| Repositório/permissões de escrita | Operacional | Integridade depende do controlo de alterações |
| Tokens de manutenção | Segredo | Nunca versionar |
| Reputação e clareza do MELLITUS | Integridade | Não induzir confiança clínica |
| Pedidos e logs do alojamento | Potencial dado pessoal | Fornecedor ainda por avaliar |
| Sites externos | Fora do controlo direto | Destinos e políticas podem mudar |

Fronteiras: colaborador para GitHub; repositório para processo futuro de publicação; navegador para alojamento; navegador para site externo. A publicação não está implementada nem validada.

## 3. Cenários de ameaça

| ID | Ameaça | Probabilidade | Impacto | Mitigação proposta | Evidência exigida | Estado |
|---|---|---|---|---|---|---|
| TM-01 | Link adulterado para phishing/domínio não oficial | Média | Alto | Lista permitida de domínios; validar HTTPS, host e destino; revisão de alterações | Testes de domínio e registos de link checks | PROPOSTO |
| TM-02 | Link deixa de ser oficial ou destino muda | Média | Alto | Data/estado de verificação; aviso de fonte externa; correção/remoção rápida | Relatório datado de links | PROPOSTO |
| TM-03 | Alteração maliciosa no repositório | Baixa–média | Alto | MFA, privilégio mínimo, revisão de alterações e proteção de branch quando configurada | Verificação da configuração real | UNKNOWN |
| TM-04 | Site confundido com aconselhamento ou validação clínica | Média | Alto | Aviso visível; sem resumos, interpretações ou recomendações próprias | Teste de presença, legibilidade e compreensão | PROPOSTO |
| TM-05 | Rastreamento por scripts, cookies, fontes ou embeds externos | Média | Médio–alto | Excluir analytics, trackers e recursos remotos de terceiros | Inspeção de rede/build antes do lançamento | PROPOSTO |
| TM-06 | Logs do host contêm IP/user-agent sem avaliação | Média | Médio–alto | Escolher host após analisar logs, retenção, subprocessadores, região e termos | Ficha de fornecedor e revisão de privacidade | BLOQUEADOR G2 |
| TM-07 | Segredo/token exposto no Git | Baixa | Alto | Não usar segredos de runtime; scan antes de release; revogar exposição | Resultado do scan e registo de remediação | PROPOSTO |
| TM-08 | Compromisso de dependência/build | Baixa–média | Alto | Dependências mínimas, versões fixas, permissões mínimas no CI futuro | Inventário e resultados de CI quando autorizados | PENDENTE |
| TM-09 | Indisponibilidade/defacement do alojamento | Média | Médio | Exportação, rollback e recuperação documentados | Ensaio antes de lançamento | PENDENTE |
| TM-10 | Falhas de acessibilidade/móvel | Média | Médio | HTML semântico, teclado, foco, contraste e teste manual | Relatório automático e manual | PENDENTE |

## 4. Controlos obrigatórios de desenho

1. Sem formulários, contas, perfis, uploads, comentários ou registos de saúde.
2. Sem analytics, pixels publicitários ou telemetria comportamental.
3. Sem scripts, fontes, CDNs ou embeds remotos de terceiros sem nova avaliação.
4. Links HTTPS, domínios permitidos e destino identificável; link não equivale a validação clínica.
5. Metadados com data e estado PASS/WARN/FAIL/UNKNOWN.
6. Histórico Git para alterações; credenciais nunca em texto claro no repositório.
7. Falta de teste nunca é PASS.
8. Aviso de âmbito obrigatório e testado.
9. Publicação bloqueada até aprovação G2 e autorização G3.
10. Qualquer dado pessoal, backend, analytics ou conteúdo clínico próprio reabre a avaliação.

## 5. Critérios de aceitação técnica futura

TA-01: URL não HTTPS ou domínio não permitido é rejeitado/sinalizado. TA-02: nenhum recurso de terceiros é carregado sem aprovação. TA-03: o código não recolhe nem envia dados introduzidos por visitantes. TA-04: aviso visível em desktop e móvel. TA-05: nenhum segredo conhecido e nenhuma vulnerabilidade crítica/alta sem tratamento aprovado. TA-06: navegação por teclado e revisão de acessibilidade sem bloqueios conhecidos. TA-07: rollback/recuperação testados antes de produção. TA-08: logs e retenção do fornecedor avaliados antes de publicar.

Todos os critérios permanecem UNKNOWN até teste numa implementação autorizada.

## 6. Decisão

Riscos residuais não são aceites por este documento. TM-06 bloqueia G2 até seleção e avaliação do alojamento. Os controlos são propostas, não prova de execução.


## 7. Evidência adicional de alojamento — 2026-10-15

GitHub Pages declara que regista e armazena o IP dos visitantes para fins de segurança ([documentação oficial](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages)). Esta evidência confirma que o risco TM-06 não pode ser marcado como inexistente, mesmo num site estático. Retenção, papéis e informação de privacidade continuam pendentes; GitHub Pages não está selecionado nem publicado.

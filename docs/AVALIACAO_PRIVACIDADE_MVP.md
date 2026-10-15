# Triagem de privacidade — MELLITUS MVP estático

| Campo | Valor |
|---|---|
| **ID** | MEL-PRIV-SCREEN-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | TRIAGEM_PRIVACIDADE |
| **Fase** | G2 — Arquitetura e privacidade |
| **Estado** | EM_REVISAO — triagem preliminar; não é parecer jurídico nem AIPD concluída |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | 2602f59c3e6957a0c1937cefc7ca205c1f20fb82750e127c93deb59b1e9ccfc5 |
| **Commit de referência (versão anterior)** | N/A — documento inicial G2 |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Carlos Andrade — responsável de produto; especialista de privacidade/jurídico não designado |
| **Aprovador** | Pendente de revisão especializada e ratificação G2 |
| **Origem** | G0/G1 aprovados; autorização limitada para preparação e avaliação de G2 |
| **Autoridade superior** | [GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA); [Constituição](https://github.com/carlos-andrade/GOVERNANCA/blob/main/CONSTITUICAO.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | [arquitetura](ARQUITETURA.md); [modelo de dados](MODELO_DADOS.md); [segurança e privacidade](SEGURANCA_PRIVACIDADE.md); [riscos](RISCOS.md) |

## 1. Finalidade e limitação

Triagem inicial do MVP: diretório estático de ligações oficiais. Não substitui parecer jurídico, determinação formal de papéis RGPD ou AIPD quando exigida. Não declara conformidade legal.

## 2. Tratamento previsto

| Elemento | Desenho MVP | Estado |
|---|---|---|
| Dados de saúde introduzidos por visitantes | Nenhum campo nem fluxo de entrada | EXCLUÍDO |
| Contas, perfis, autenticação | Não existentes | EXCLUÍDO |
| Medições, sintomas, medicação, histórico | Não recolhidos | EXCLUÍDO |
| Metadados de fontes oficiais | Título, entidade, URL, tema, jurisdição/idioma, data e estado técnico | NECESSÁRIO |
| Dados de autores/colaboradores | Identidade e histórico podem constar do GitHub | Dependente da plataforma |
| IP, user-agent, timestamp e logs | Podem ser processados pelo alojamento | UNKNOWN — fornecedor por selecionar |
| Cookies próprios | Nenhum previsto | EXCLUÍDO |
| Analytics, pixels e publicidade | Nenhum previsto | EXCLUÍDO |
| Navegação para sites externos | O visitante sai do MELLITUS ao clicar | Destino tem práticas próprias |

## 3. Necessidade e minimização

O catálogo não necessita de identificar visitantes. A opção de menor risco é servir conteúdo estático, não incluir formulários, evitar scripts externos e não criar telemetria. A pesquisa, se implementada, deve ocorrer localmente no navegador, sem enviar termos ao servidor.

O catálogo não deve incluir afirmações clínicas próprias, resumos, traduções, interpretações ou recomendações. Apenas metadados necessários para identificar fontes externas.

## 4. Finalidade, base legal e responsabilidade

O conteúdo público do catálogo não é, por si só, dado pessoal de saúde dos visitantes. Porém, pedidos HTTP, logs de segurança, contas de colaboradores e dados processados pelo fornecedor podem envolver dados pessoais. O responsável pelo tratamento e os papéis do fornecedor não podem ser concluídos antes de escolher alojamento e analisar os termos.

Não presumir que consentimento é a base legal adequada, nem que a ausência de contas elimina todo o tratamento de dados pessoais. Registar finalidade, base legal, transparência, retenção, subprocessadores, transferências e direitos antes da publicação.

## 5. Triagem de AIPD/DPIA

**Resultado preliminar: AIPD não determinada; decisão formal pendente.**

O desenho exclui tratamento de dados de saúde de visitantes, profiling, decisões automatizadas e contas pessoais. Isso reduz o risco, mas não permite concluir, por si só, que uma AIPD não é necessária. A conclusão depende do tratamento real, fornecedor, logs, escala, contexto e regras aplicáveis em Portugal/UE.

Antes da publicação: identificar fornecedor, região, logs, retenção, subprocessadores e transferências; determinar responsável pelo tratamento e informação necessária; comparar o tratamento real com o artigo 35.º do RGPD e a lista aplicável da CNPD; registar decisão fundamentada sobre AIPD; cumprir a via legal aplicável se houver risco elevado residual.

Fontes oficiais:
- [CNPD — Avaliação de impacto](https://www.cnpd.pt/organizacoes/outras-obrigacoes/avaliacao-de-impacto/).
- [Diário da República — Regulamento n.º 798/2018 da CNPD](https://diariodarepublica.pt/dr/detalhe/regulamento/798-2018-117182365).
- [Comissão Europeia — categorias especiais de dados, incluindo dados de saúde](https://commission.europa.eu/law/law-topic/data-protection/information-individuals_en).

## 6. Avisos e experiência do utilizador

Informar que o MELLITUS é um diretório de links externos; que um link não representa validação clínica; que o site não presta diagnóstico nem aconselhamento médico; e que os destinos externos têm políticas de privacidade próprias. Não inserir parâmetros de rastreamento, usar encurtadores ou incorporar páginas externas em iframes.

## 7. Retenção e direitos

Não criar base de dados de visitantes. Definir retenção de logs após análise das práticas do fornecedor. Não prometer eliminação de logs sem evidência contratual. Não recolher pedidos de titulares por formulário até existir processo e responsável. O histórico Git e eventuais forks/cópias seguem as políticas da plataforma; apagar um ficheiro não garante apagar todas as cópias.

## 8. Bloqueadores e condições de saída

| ID | Pendência | Estado | Condição de fecho |
|---|---|---|---|
| PR-01 | Selecionar alojamento e região | PENDENTE | Decisão com termos, custo, logs e localização |
| PR-02 | Identificar papéis RGPD e aviso necessário | PENDENTE | Análise documentada para o fornecedor concreto |
| PR-03 | Determinar formalmente necessidade de AIPD | PENDENTE | Decisão fundamentada face ao tratamento real e CNPD |
| PR-04 | Definir aviso de privacidade/links externos | PROPOSTO | Texto validado antes da publicação |
| PR-05 | Confirmar ausência de trackers, cookies e formulários | PROPOSTO | Inspeção técnica da build autorizada |
| PR-06 | Definir responsável por incidentes e contacto público | PENDENTE | Processo operacional definido antes do piloto |

## 9. Conclusão

A arquitetura estática é a opção de minimização preferida. Esta triagem não fecha a análise legal nem prova que o fornecedor não trata dados pessoais. G2 não deve ser aprovado até PR-01 a PR-03 terem evidência suficiente e o proprietário ratificar o desenho. Não recolher dados de saúde nem publicar nesta fase.

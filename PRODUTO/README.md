# Especificação funcional do produto MELLITUS

| Campo | Valor |
|---|---|
| **ID** | MEL-PROD-README-001 |
| **Projeto** | MELLITUS |
| **Repositório** | [carlos-andrade/MELLITUS](https://github.com/carlos-andrade/MELLITUS) |
| **Tipo documental** | ESPECIFICACAO_PRODUTO |
| **Fase** | F0 — Governação e requisitos |
| **Estado** | EM_REVISAO |
| **Versão** | 1.0.0 |
| **SHA-256 (conteúdo canónico)** | PENDENTE_CALCULO |
| **Commit de referência (versão anterior)** | N/A — documento inicial |
| **Data de criação** | 2026-10-15 |
| **Data de atualização** | 2026-10-15 |
| **Responsável** | Responsável de produto — a formalizar |
| **Aprovador** | Pendente de aprovação G0/G1 |
| **Origem** | Plano diretor e requisitos iniciais |
| **Autoridade superior** | [GOVERNANCA](https://github.com/carlos-andrade/GOVERNANCA); [governação MELLITUS](../GOVERNANCA/GOVERNANCA.md) |
| **Cadeia de autoridade** | PROMPTS → CARTAS → LAYOUT ÚNICO → CÓDIGO |
| **Rastreabilidade** | docs/PLANO_DIRETOR.md; docs/REQUISITOS.md; docs/RISCOS.md |

## Objetivo

Definir uma primeira experiência educativa segura sobre diabetes mellitus para o público geral. O produto inicial é proposto como website responsivo, com conteúdo rastreável, pesquisa e processo editorial controlado.

## Personas iniciais propostas

- Pessoa que procura informação introdutória e confiável sobre diabetes.
- Familiar/cuidador que necessita de explicações claras.
- Editor de conteúdo que gere artigos e referências.
- Revisor clínico que verifica afirmações e aprova conteúdo conforme o seu âmbito.
- Administrador técnico que mantém a plataforma sem acesso desnecessário a dados clínicos.

Estas personas são hipóteses a validar com investigação de utilizadores; não comprovam procura ou adequação.

## Jornada pública principal

1. A pessoa entra numa página ou pesquisa um tema.
2. Vê a definição e a explicação em linguagem simples.
3. Consulta tipos, sintomas, gestão geral e sinais de alerta quando relevantes.
4. Abre as fontes e confere a data de revisão.
5. Encontra os limites da informação e os meios apropriados para procurar assistência.

## Módulos funcionais

### MVP proposto
- Página inicial educativa.
- Catálogo de temas e artigos.
- Pesquisa por título, resumo e conteúdo publicado.
- Páginas com fontes, data de revisão e aviso de âmbito.
- Acessibilidade, visualização móvel e navegação consistente.
- Processo editorial para criar, rever, aprovar, publicar, atualizar e retirar conteúdo.
- Página de contacto/correção de conteúdo com tratamento de dados minimizado.

### Futuro, sujeito a gate separado
- Conta e preferências.
- Registos pessoais de medições.
- Histórico e gráficos descritivos.
- Exportação e eliminação.
- Integração com serviços ou dispositivos.

Nenhum módulo futuro pode ser ativado só por estar descrito. Exige requisitos próprios, análise de risco, privacidade, revisão clínica/regulatória se aplicável e aprovação G2.

## Fora do MVP
- Diagnóstico ou exclusão de diagnóstico.
- Ajuste autónomo de medicação ou insulina.
- Prescrição, triagem conclusiva ou previsão clínica.
- Recomendação individualizada a partir de valores pessoais.
- Ligação automática a dispositivos médicos.
- Monetização baseada em dados de saúde ou publicidade comportamental sensível.

## Princípios UX
- Português europeu por defeito e linguagem não estigmatizante.
- Contraste, teclado, foco visível, rótulos e estrutura semântica adequados.
- Fontes próximas das afirmações clínicas.
- Apresentação clara de incerteza e de datas.
- Não usar padrões manipulativos ou urgência comercial.
- Distinguir conteúdo educativo de comunicação de emergência.

## Critérios de sucesso propostos

Definir baseline antes do piloto. Medir conclusão de tarefas de navegação, sucesso de pesquisa, acessibilidade, tempo de carregamento, taxa de erros editoriais, tempo de correção de conteúdo e compreensão testada com participantes. Não usar estes indicadores para inferir resultados de saúde sem investigação própria.

## Próxima ação

Validar público-alvo, jornadas, prioridades e critérios mensuráveis com o responsável de produto e obter decisão G0/G1.

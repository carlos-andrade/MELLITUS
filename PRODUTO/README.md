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
| **SHA-256 (conteúdo canónico)** | 72fce3f12de786ed82ca4831541fc7cad896195930262906e1b449b29de858d2 |
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

Definir um diretório responsivo de fontes oficiais sobre diabetes para o público geral, com pesquisa, navegação, ligações diretas e metadados. O proprietário decidiu que não haverá revisor clínico; portanto, o MVP proposto não produzirá conteúdo clínico próprio.

## Personas iniciais propostas

- Pessoa que procura informação introdutória e confiável sobre diabetes.
- Familiar/cuidador que necessita de explicações claras.
- Responsável de catálogo que verifica entidades, URLs e metadados; função por formalizar.
- Administrador técnico que mantém a plataforma sem recolher nem aceder a dados pessoais de saúde no MVP.

Estas personas são hipóteses a validar com investigação de utilizadores; não comprovam procura ou adequação.

## Jornada pública principal

1. A pessoa pesquisa um tema.
2. Consulta fontes externas de entidades oficiais.
3. Vê entidade, título, jurisdição/idioma e data de verificação do link.
4. Abre diretamente a página original da fonte.
5. Vê o aviso de que o MELLITUS organiza links, não valida clinicamente o conteúdo nem presta aconselhamento individual.

## Módulos funcionais

### MVP proposto — âmbito reduzido sem revisor clínico
- Página inicial com aviso de âmbito.
- Catálogo de fontes oficiais externas organizado por tema.
- Pesquisa por entidade, título e metadados do catálogo.
- Cada registo apresenta entidade, título, URL, jurisdição/idioma e data de verificação.
- Processo rastreável para testar, corrigir e remover links.
- Acessibilidade, visualização móvel e navegação consistente.
- Não criar artigos, resumos, traduções, interpretações ou recomendações clínicas próprias.
- Não recolher dados pessoais de saúde.

### Futuro, sujeito a gate separado
- Conta e preferências.
- Registos pessoais de medições.
- Histórico e gráficos descritivos.
- Exportação e eliminação.
- Integração com serviços ou dispositivos.

Nenhum módulo futuro pode ser ativado só por estar descrito. Exige requisitos próprios, análise de risco, privacidade, revisão apropriada quando aplicável e aprovação G2. A decisão de não nomear revisor clínico mantém conteúdo clínico próprio excluído.

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

Ratificar o âmbito reduzido do catálogo de fontes, formalizar responsável de produto, definir critérios mensuráveis e obter decisão G0/G1.

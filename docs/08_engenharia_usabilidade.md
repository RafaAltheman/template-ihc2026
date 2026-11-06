# Entrega 8 — Ciclo de vida e engenharia de usabilidade

**Data:** {{05/11/2026}}  
**Status:** 🟨 em andamento   
**Responsabilidade:** 1 solução por equipe

## Objetivo da atividade

Transformar o conhecimento acumulado sobre usuários, tarefas, plataforma e contexto em princípios e **metas de usabilidade verificáveis**, mantendo o caráter iterativo do projeto.

## Delimitação do sistema interativo

Antes das características da plataforma, separe:

| Camada | O que pertence ao projeto | O que será avaliado em IHC |
|---|---|---|
| contribuição técnica do TCC | Modelagem do robô humanoide Atom, desenvolvimento de uma política de locomoção por aprendizado por reforço profundo, execução de treinamentos em ambiente simulado e avaliação técnica do comportamento obtido.  | O desempenho técnico da política, a estabilidade física do robô e a qualidade do aprendizado pertencem ao TCC. Os testes de IHC não substituem essas avaliações. |
| camada de interação da disciplina | Interface conceitual para consultar histórico de execuções, visualizar métricas, comparar resultados, selecionar uma referência (baseline), registrar avaliações e hipóteses e apresentar a evolução do desempenho à equipe. | Compreensão das informações, facilidade de navegação, conclusão das tarefas, tempo necessário, erros de interpretação, clareza dos controles e satisfação dos usuários. |
| integrações/dados simulados | Resultados de treinamentos representados por registros de exemplo, incluindo identificadores, métricas, versões, parâmetros e evidências visuais. O funcionamento da interface é representado por protótipos em papel, sem integração obrigatória com o ambiente real de treinamento. | Avaliação da interação com os dados apresentados, das decisões realizadas pelos usuários e dos fluxos de navegação, sem medir processamento real ou desempenho do simulador |

Em um protótipo de disciplina, é aceitável simular processamento ou resultados quando a implementação técnica não estiver integrada, desde que isso seja declarado e a simulação seja suficiente para avaliar a interação.

## 1. Características da plataforma

| Característica | Descrição | Consequência para IHC |
|---|---|---|
| Software | A interface é proposta como uma aplicação de consulta e análise de resultados, com organização compatível com uma aplicação desktop. | A navegação deve ser compreensível independentemente da implementação futura, mantendo padrões consistentes de menus, filtros, tabelas e controles. |
| Hardware/dispositivos | O público previsto utiliza principalmente computadores e notebooks durante o desenvolvimento e acompanhamento dos experimentos. O ambiente técnico do TCC utiliza Linux e ferramentas de simulação. | A interface será inicialmente projetada para telas de computadores, priorizando leitura de tabelas, comparação de resultados e visualização de gráficos. |
| Capacidades | Consultar execuções anteriores, pesquisar por identificadores, aplicar filtros, selecionar execuções, comparar métricas e parâmetros, visualizar evolução temporal, consultar evidências e registrar conclusões ou hipóteses. | As funcionalidades devem corresponder às tarefas T01, T02 e T03, permitindo que os usuários encontrem as informações necessárias sem executar etapas desnecessárias. |
| Restrições | O protótipo não executa algoritmos de treinamento, não controla diretamente o robô e não implementa integração automática com o simulador. Os resultados apresentados são exemplos utilizados para avaliar os fluxos. | É necessário deixar claras as ações simuladas para que o usuário não confunda assuma que os valores apresentados são reais |
| Conectividade/latência | A interface final poderá depender de arquivos ou serviços para acessar resultados, mas ainda não há arquitetura de integração nem requisitos de rede definidos. No protótipo em papel não existe comunicação real com servidores. | Estados de carregamento, indisponibilidade e recuperação poderão ser previstos para versões futuras. Na baixa fidelidade, o foco será a compreensão do fluxo. |
| Segurança/privacidade | Os resultados experimentais são predominantemente técnicos. Entretanto, estudos com participantes podem envolver dados pessoais, gravações e informações internas das equipes. | Minimizar a coleta de dados pessoais, proteger registros de pesquisa e evitar a exposição de informações confidenciais durante avaliações e apresentações. |
| Volume de dados/histórico | Equipes podem acumular diferentes execuções, parâmetros e resultados ao longo do desenvolvimento. O volume real ainda não foi dimensionado. | Disponibilizar busca por ID, filtros por período e versão e identificação clara das execuções. A necessidade de paginação será avaliada caso o volume de registros justifique. |
| Tempo de processamento | Treinamentos por aprendizado por reforço podem exigir processamento prolongado, mas sua execução ocorre fora do escopo interativo definido. As consultas e comparações da interface ainda não possuem tempos reais medidos. | Priorizar feedback após ações, indicar quando uma consulta não apresenta resultados e confirmar o registro de avaliações ou hipóteses. Não estabelecer metas de processamento técnico sem dados reais. |
| Papéis/permissões | As personas P01, P02 e P03 representam necessidades diferentes: avaliação técnica, investigação de experimentos e acompanhamento/comunicação. Ainda não foram definidos níveis de acesso ou autenticação distintos. A princípio, a plataforma oferece uma unica permissão que abrange todas as necessidades. | Organizar as informações conforme as tarefas sem pressupor um sistema de permissões. Recursos de administração e controle de acesso só deverão ser incorporados caso uma necessidade concreta seja identificada. |


## 2. Princípios gerais do projeto

Inclua apenas normas, leis, padrões e princípios realmente relevantes, explicando **como** afetam o projeto. Não transforme esta seção em lista de links.

| Princípio/norma | Aplicabilidade ao contexto | Decisão/requisito decorrente | Fonte |
|---|---|---|---|
| Contexto de uso | Os usuários realizam atividades distintas de avaliação, investigação e comunicação. A interface precisa refletir essas diferenças e considerar o ambiente acadêmico e técnico. | Organizar os fluxos conforme as tarefas T01, T02 e T03, priorizando as informações necessárias para alcançar os objetivos dos usuários. | Entregas 1, 3, 4 e 5 |
| Usabilidade (ISO 9241-11:2018) | Define a avaliação da usabilidade a partir de eficácia, eficiência e satisfação em um contexto de uso específico. | Estabelecer metas mensuráveis de conclusão das tarefas, tempo de execução, erros e satisfação, associadas a usuários e atividades definidos. | [ISO 9241-11:2018](https://committee.iso.org/standard/63500.html) |
| Acessibilidade (WCAG 2.2) | Fornece critérios de acessibilidade para interfaces web, relevantes como referência para uma eventual implementação digital do protótipo. | Planejar textos legíveis, identificação das informações sem depender apenas de cores, legendas em gráficos, controles reconhecíveis e navegação por teclado na implementação futura. | [WCAG 2.2 — W3C](https://www.w3.org/TR/WCAG22/) |
| LGPD — Lei nº 13.709/2018 | É relevante para o tratamento de dados pessoais eventualmente coletados nas pesquisas com participantes. Métricas técnicas anônimas de robôs não constituem, por si só, dados pessoais. | Solicitar consentimento e demais autorizações pertinentes nas atividades de pesquisa, minimizar dados pessoais, restringir acesso aos registros e utilizar resultados anonimizados na documentação. | [Guia da ANPD para fins acadêmicos e pesquisas](https://www.gov.br/anpd/pt-br/centrais-de-conteudo/materiais-educativos-e-publicacoes/guia-orientativo-tratamento-de-dados-pessoais-para-fins-academicos-e-para-a-realizacao-de-estudos-e-pesquisas) |
| Consistência e previsibilidade da navegação | O usuário precisa alternar entre histórico, comparação, avaliação, painel e evidências sem perder o entendimento do fluxo. | Manter nomenclatura consistente, preservar seleções quando possível e identificar claramente o destino dos botões. | Entregas 5 e 6 |
| Visibilidade do estado do sistema e prevenção de erros | Pesquisas sem resultados, referências incompatíveis e salvamentos sem confirmação podem comprometer a conclusão das tarefas. | Apresentar mensagens de estado, orientar recuperação de erros, indicar incompatibilidades e confirmar o salvamento de registros. | Entregas 5 e 6 |


## 3. Metas de usabilidade

Usabilidade deve ser discutida **no contexto de uso**. Metas quantitativas devem dizer o que será medido, em qual tarefa, com qual população e qual limite será considerado aceitável.

### 3.1 Metas qualitativas

| Meta | Para quem/tarefa | Evidência desejada | Justificativa |
|---|---|---|---|
| Compreensão clara dos resultados apresentados | P01 — T01 | O participante consegue explicar quais indicadores melhoraram e quais pioraram, utilizando as informações da interface sem confundir métricas ou execuções. | A avaliação de um treinamento não pode depender de uma única métrica isolada. |
| Identificação adequada do contexto da comparação. | P01 e P02 — T01 e T02 | O participante reconhece os IDs, as versões e os parâmetros das execuções e identifica possíveis incompatibilidades. | Comparações entre experimentos realizados em condições diferentes podem produzir conclusões equivocadas. |
| Facilidade para localizar resultados anteriores | P02 — T02 | O participante compreende os controles de busca e filtros, seleciona os registros desejados e sabe como corrigir uma pesquisa sem resultados. | O histórico precisa apoiar a recuperação das informações. |
| Continuidade da navegação durante apresentações. | P03 — T03 | O participante consegue abrir uma evidência detalhada e retornar à apresentação sem perder o período ou o indicador que estava analisando. | Consultas durante reuniões não devem interromper desnecessariamente o fluxo da comunicação. |
| Compreensão das mensagens de erro e confirmação. | P01, P02 e P03 — T01, T02 e T03 | O participante compreende mensagens de ausência de dados, incompatibilidade e salvamento, identificando a ação seguinte. | Mensagens claras reduzem incerteza, decisões equivocadas e abandono das tarefas. |


### 3.2 Metas quantitativas

| ID | Dimensão | Métrica | Tarefa/escopo | Meta | Como medir | Justificativa |
|---|---|---|---|---|---|---|
| MU01 | eficácia | taxa de conclusão sem ajuda | T01 | ≥ {{x}}% | teste observado | {{...}} |
| MU02 | eficiência | tempo mediano | T02 | ≤ {{tempo}} | cronômetro/log | {{...}} |
| MU03 | satisfação | escala pós-tarefa | T01–T03 | ≥ {{valor}} | questionário | {{...}} |

### 3.3 Priorização das metas (se exigida na disciplina)

Se o professor solicitar porcentagens que somem 100%, trate-as como **peso de prioridade**, não como métrica de usabilidade.

| Meta | Peso de prioridade | Justificativa |
|---|---:|---|
| MU01 | {{...}}% | {{...}} |
| **Total** | **100%** | |

## 4. Como o ciclo será iterado

Explique que artefatos serão revisitados após protótipos e avaliações.

## Checklist

- [ ] Capacidades e restrições têm impacto de IHC explicitado.
- [ ] Está claro o limite entre contribuição técnica do TCC e camada interativa da disciplina.
- [ ] Resultados/processamento simulados no protótipo foram explicitados.
- [ ] Metas de usabilidade avaliam a interação, não substituem métricas técnicas do TCC.
- [ ] Normas/princípios estão contextualizados, não apenas copiados.
- [ ] Metas quantitativas são mensuráveis e associadas a tarefas/público.
- [ ] Eficácia, eficiência e satisfação são consideradas quando pertinentes.
- [ ] Metas poderão ser verificadas nas Entregas 12–14.

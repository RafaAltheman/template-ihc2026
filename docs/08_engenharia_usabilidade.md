# Entrega 8 — Ciclo de vida e engenharia de usabilidade

**Data:** {{05/11/2026}}  
**Status:** 🟩 Concluida  
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
| MU01 | Eficácia | Taxa de conclusão correta, sem ajuda do moderador. | T01 — Avaliar melhoria de treinamento. | >= 80% dos participantes. | Observar quantos participantes identificam ganhos e regressões, selecionam uma conclusão justificada e concluem o registro sem receber instruções adicionais. | A avaliação é crítica porque interpretações incorretas podem orientar ajustes inadequados nos treinamentos. |
| MU02 | Eficácia | Taxa de conclusão correta, sem ajuda do moderador. | T02 — Localizar e comparar execuções. | >= 80% dos participantes. | Verificar quantos localizam as duas execuções solicitadas, realizam a comparação e registram uma hipótese distinguindo evidências e ressalvas. | A comparação é critica para entender se os ajustes no treinamento estão trazendo resultados positivos. |
| MU03 | Eficácia | Taxa de conclusão da apresentação e consulta de evidências. | T03 — Consultar síntese e comunicar resultados. | >= 80% dos participantes. | Observar quantos selecionam o período, identificam ao menos um ponto relevante, consultam uma evidência e retornam ao contexto anterior. | A interface precisa apoiar reuniões sem prejudicar a continuidade da análise. |
| MU04 | Eficiência | Tempo mediano para concluir cada tarefa com sucesso. | T01 e T02. | <= 6 minutos por tarefa. | Cronometrar desde o início do cenário até a conclusão, considerando apenas execuções bem-sucedidas e registrando a mediana separadamente para T01 e T02. | A avaliação e a comparação devem ocorrer sem navegação excessiva ou repetição desnecessária de ações. |
| MU06 | Satisfação | Avaliação subjetiva de facilidade de uso após cada tarefa. | T01, T02 e T03. | Mediana >= 4 em escala de 1 a 5 | Aplicar uma pergunta pós-tarefa com escala de 1 (muito difícil) a 5 (muito fácil) e calcular a mediana por tarefa. | A satisfação complementa as medidas de eficácia e eficiência, permitindo identificar desconforto mesmo quando a tarefa é concluída. |
| MU07 | Prevenção de erros | Quantidade de erros críticos que comprometem a integridade da análise. | T01 e T02. | Zero erros críticos nos testes avaliados. | Registrar casos de associação da conclusão à execução errada, seleção incorreta de referência sem percepção da incompatibilidade ou interpretação de registro não salvo como salvo. | Erros desse tipo comprometem a confiabilidade das análises e precisam receber prioridade de correção. |
| MU08 | Continuidade da interação | Taxa de retorno ao contexto anterior sem refazer seleções. | T03 — Consulta de evidência durante a reunião. | >= 80% dos participantes. | Observar quantos conseguem retornar à apresentação mantendo o período, o indicador e o ponto anterior, sem intervenção do moderador. | Preservar o contexto evita retrabalho e interrupções durante as reuniões. |


### 3.3 Priorização das metas (se exigida na disciplina)

Os pesos representam a importância relativa de cada meta para o projeto e não devem ser confundidos com os valores aceitáveis de desempenho ou com os resultados dos testes.

| Meta | Peso de prioridade | Justificativa |
|---|---:|---|
| **MU01 — Eficácia na avaliação de treinamentos** | 20% | A interpretação correta dos resultados é fundamental para orientar decisões sobre os treinamentos do robô. |
| **MU02 — Eficácia na comparação de execuções** | 15% | A localização e comparação correta dos experimentos sustenta a rastreabilidade das análises. |
| **MU03 — Eficácia na comunicação dos resultados** | 15% | A apresentação deve permitir identificar questões relevantes para discussão e investigação. |
| **MU04 — Eficiência na avaliação e comparação** | 10% | Reduzir o esforço necessário para interpretar e comparar experimentos melhora a utilização recorrente da interface. |
| **MU05 — Eficiência na consulta durante reuniões** | 5% | A rapidez é relevante, mas não deve se sobrepor à compreensão correta das informações. |
| **MU06 — Satisfação dos usuários** | 10% | A percepção de facilidade e conforto é importante para a aceitação da interface. |
| **MU07 — Prevenção de erros críticos** | 15% | Atribuir resultados a execuções incorretas ou registrar conclusões equivocadas pode comprometer decisões técnicas. |
| **MU08 — Continuidade da navegação** | 10% | Preservar informações durante consultas e retornos evita retrabalho e interrupções. |
| **Total** | **100%** | |

Nós atribuímos maior peso às metas de eficácia e prevenção de erros, pois o objetivo principal da interface é apoiar a interpretação correta dos resultados experimentais.

A eficiência e a satisfação também são consideradas importantes, mas a rapidez não deve comprometer a qualidade das decisões realizadas pelos usuários.

## 4. Como o ciclo será iterado

O desenvolvimento da interface seguirá um processo iterativo centrado no usuário, no qual os conhecimentos obtidos em cada etapa serão utilizados para revisar os artefatos anteriores.

O ciclo será organizado em quatro atividades principais: compreender o contexto de uso, propor soluções de interação, avaliar as soluções e revisar o projeto.

### Etapa 1 — Compreensão das necessidades

As Entregas 1 a 5 estabeleceram o escopo de IHC, as personas, os cenários e as tarefas principais. A Entrega 7 definiu instrumentos para investigar as hipóteses H01b, H02 e H03, que permanecem abertas na rastreabilidade.

Após a aplicação dos instrumentos, os resultados deverão ser utilizados para verificar se as atividades e necessidades consideradas pela equipe correspondem ao trabalho real dos usuários.

**Artefatos revisitados:** personas, cenários, descrição das tarefas, escopo de interação e `RASTREABILIDADE.md`.

### Etapa 2 — Revisão dos protótipos

A Entrega 6 apresentou telas em papel para representar os fluxos de consulta ao histórico, comparação de execuções, avaliação de treinamentos e acompanhamento do desempenho.

As observações obtidas em avaliações formativas deverão orientar ajustes na organização das informações, no funcionamento dos controles e na navegação entre telas.

Alguns pontos que merecem investigação são:

- Clareza das legendas dos gráficos e identificação das execuções.
- Compreensão do termo baseline e dos critérios de comparação.
- Apresentação das diferenças de configuração.
- Identificação de estados de erro e ausência de dados.
- Comportamento dos botões de retorno.
- Preservação do contexto durante a consulta a evidências.
- Feedback após o registro de avaliações e hipóteses.

Esses pontos representam aspectos a verificar, não resultados de usabilidade já comprovados.

**Artefatos revisitados:** protótipos da Entrega 6, fluxos de navegação e descrições das telas.

### Etapa 3 — Avaliação da usabilidade

Nas etapas posteriores da disciplina, serão elaborados cenários de teste para verificar as metas quantitativas e qualitativas definidas nesta entrega.

Os participantes serão convidados a realizar tarefas próximas às atividades de T01, T02 e T03, sem receber orientações sobre quais controles devem utilizar.

Durante a interação, serão registrados os resultados das tarefas, os tempos de execução, os erros, os pedidos de ajuda e as dificuldades observadas.

Após cada tarefa, poderá ser aplicada uma pergunta de satisfação utilizando a escala definida na meta MU06.

Os resultados serão comparados aos critérios de aceitação estabelecidos nesta entrega, permitindo identificar quais aspectos da interface atendem às metas e quais precisam de revisão.

**Artefatos produzidos ou revisitados:** roteiros de teste, registros de observação, métricas de usabilidade, relatórios de avaliação e matriz de rastreabilidade.

### Etapa 4 — Revisão e nova iteração

A equipe analisará os problemas identificados, considerando sua gravidade, frequência e impacto na conclusão das tarefas.

Problemas que provocarem erros críticos, perda de informações ou impossibilidade de concluir uma tarefa terão prioridade sobre ajustes puramente visuais.

Após a revisão, os fluxos afetados deverão ser avaliados novamente, quando possível, para verificar se as alterações produziram melhorias.

O ciclo poderá ser repetido sempre que novas evidências indicarem a necessidade de modificar a interface, as tarefas ou os requisitos de usabilidade.

### Registro das decisões

As decisões de revisão deverão registrar:

1. O problema identificado e a tarefa afetada.
2. A evidência obtida durante a coleta ou avaliação.
3. A alteração proposta ou realizada.
4. A meta de usabilidade relacionada.
5. O resultado da nova avaliação, quando disponível.

As alterações relevantes serão incorporadas ao arquivo `../RASTREABILIDADE.md`, mantendo a ligação entre necessidades dos usuários, tarefas, protótipos e critérios de avaliação.

Dessa forma, a evolução da interface será fundamentada em evidências obtidas durante o processo de IHC, e não apenas nas preferências da equipe.

## Checklist

- [X] Capacidades e restrições têm impacto de IHC explicitado.
- [X] Está claro o limite entre contribuição técnica do TCC e camada interativa da disciplina.
- [X] Resultados/processamento simulados no protótipo foram explicitados.
- [X] Metas de usabilidade avaliam a interação, não substituem métricas técnicas do TCC.
- [X] Normas/princípios estão contextualizados, não apenas copiados.
- [X] Metas quantitativas são mensuráveis e associadas a tarefas/público.
- [X] Eficácia, eficiência e satisfação são consideradas quando pertinentes.
- [X] Metas poderão ser verificadas nas Entregas 12–14.

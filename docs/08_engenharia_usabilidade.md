# Entrega 8 — Ciclo de vida e engenharia de usabilidade

**Data:** 14/11/2026  
**Status:** 🟦 revisada após feedback
**Responsabilidade:** 1 solução por equipe

## Objetivo da atividade

Transformar o conhecimento acumulado sobre usuários, tarefas, plataforma e contexto em princípios e **metas de usabilidade verificáveis**, mantendo o caráter iterativo do projeto.

## Delimitação do sistema interativo

Antes das características da plataforma, separe:

| Camada | O que pertence ao projeto | O que será avaliado em IHC |
|---|---|---|
| contribuição técnica do TCC | Modelagem do robô humanoide Atom, desenvolvimento de uma política de locomoção por aprendizado por reforço profundo, execução de treinamentos em ambiente simulado e avaliação técnica do comportamento obtido. | O desempenho técnico da política, a estabilidade física do robô e a qualidade do aprendizado pertencem ao TCC. Os testes de IHC não substituem essas avaliações. |
| camada de interação da disciplina | Interface conceitual para consultar histórico de execuções, visualizar métricas, comparar resultados, selecionar uma referência (baseline), registrar avaliações e hipóteses e apresentar a evolução do desempenho à equipe. | Compreensão das informações, facilidade de navegação, conclusão das tarefas, tempo necessário, erros de interpretação, clareza dos controles e satisfação dos usuários. |
| integrações/dados simulados | Resultados de treinamentos representados por registros de exemplo, incluindo identificadores, métricas, versões, parâmetros e evidências visuais. O funcionamento da interface é representado por protótipos em papel, sem integração obrigatória com o ambiente real de treinamento. | Avaliação da interação com os dados apresentados, das decisões realizadas pelos usuários e dos fluxos de navegação, sem medir processamento real ou desempenho do simulador. |

Em um protótipo de disciplina, é aceitável simular processamento ou resultados quando a implementação técnica não estiver integrada, desde que isso seja declarado e a simulação seja suficiente para avaliar a interação.

## 1. Características da plataforma

| Característica | Descrição | Consequência para IHC |
|---|---|---|
| Software | A interface é proposta como uma aplicação de consulta e análise de resultados, com organização compatível com uma aplicação desktop. | A navegação deve ser compreensível independentemente da implementação futura, mantendo padrões consistentes de menus, filtros, tabelas e controles. |
| Hardware/dispositivos | O público previsto utiliza principalmente computadores e notebooks durante o desenvolvimento e acompanhamento dos experimentos. O ambiente técnico do TCC utiliza Linux e ferramentas de simulação. | A interface será inicialmente projetada para telas de computadores, priorizando leitura de tabelas, comparação de resultados e visualização de gráficos. |
| Capacidades | Consultar execuções anteriores, pesquisar por identificadores, aplicar filtros, selecionar execuções, comparar métricas e parâmetros, visualizar evolução temporal, consultar evidências e registrar conclusões ou hipóteses. | As funcionalidades devem corresponder às tarefas T01, T02 e T03, permitindo que os usuários encontrem as informações necessárias sem executar etapas desnecessárias. |
| Restrições | O protótipo não executa algoritmos de treinamento, não controla diretamente o robô e não implementa integração automática com o simulador. Os resultados apresentados são exemplos utilizados para avaliar os fluxos. | É necessário deixar claras as ações simuladas para que o usuário não confunda os valores apresentados com resultados reais. |
| Conectividade/latência | A interface final poderá depender de arquivos ou serviços para acessar resultados, mas ainda não há arquitetura de integração nem requisitos de rede definidos. No protótipo em papel não existe comunicação real com servidores. | Estados de carregamento, indisponibilidade e recuperação poderão ser previstos para versões futuras. Na baixa fidelidade, o foco será a compreensão do fluxo. |
| Segurança/privacidade | Os resultados experimentais são predominantemente técnicos. Entretanto, estudos com participantes podem envolver dados pessoais, gravações e informações internas das equipes. | Minimizar a coleta de dados pessoais, proteger registros de pesquisa e evitar a exposição de informações confidenciais durante avaliações e apresentações. |
| Volume de dados/histórico | Equipes podem acumular diferentes execuções, parâmetros e resultados ao longo do desenvolvimento. O volume real ainda não foi dimensionado. | Disponibilizar busca por ID, filtros por período e versão e identificação clara das execuções. A necessidade de paginação será avaliada caso o volume de registros justifique. |
| Tempo de processamento | Treinamentos por aprendizado por reforço podem exigir processamento prolongado, mas sua execução ocorre fora do escopo interativo definido. As consultas e comparações da interface ainda não possuem tempos reais medidos. | Priorizar feedback após ações, indicar quando uma consulta não apresenta resultados e confirmar o registro de avaliações ou hipóteses. Não estabelecer metas de processamento técnico sem dados reais. |
| Papéis/permissões | As personas P01, P02 e P03 representam necessidades diferentes: avaliação técnica, investigação de experimentos e acompanhamento/comunicação. Ainda não foram definidos níveis de acesso ou autenticação distintos. A princípio, a plataforma oferece uma única permissão que abrange todas as necessidades. | Organizar as informações conforme as tarefas sem pressupor um sistema de permissões. Recursos de administração e controle de acesso só deverão ser incorporados caso uma necessidade concreta seja identificada. |

## 2. Princípios gerais do projeto

Os princípios gerais foram organizados em dois grupos: princípios direcionados ao negócio e princípios direcionados à interface. Essa separação permite distinguir as normas, regras e requisitos que delimitam o projeto das orientações que influenciam diretamente as decisões de interação e apresentação das informações.

### 2.1 Princípios direcionados ao negócio

| Princípio/norma | Aplicabilidade ao contexto | Decisão/requisito decorrente | Fonte |
|---|---|---|---|
| Nielsen (1993) | Define a avaliação da usabilidade a partir de eficácia, eficiência e satisfação em um contexto de uso específico. Serve como referência para compreender a qualidade da interação no contexto do projeto. | Estabelecer metas mensuráveis de conclusão das tarefas, tempo de execução, erros e satisfação, associadas a usuários e atividades definidos. | https://www.nngroup.com/books/usability-engineering/ |
| LGPD — Lei nº 13.709/2018 | É relevante para o tratamento de dados pessoais eventualmente coletados nas pesquisas com participantes. Métricas técnicas anônimas de robôs não constituem, por si só, dados pessoais. | Solicitar consentimento e demais autorizações pertinentes nas atividades de pesquisa, minimizar dados pessoais, restringir acesso aos registros e utilizar resultados anonimizados na documentação. | [Guia da ANPD para fins acadêmicos e pesquisas](https://www.gov.br/anpd/pt-br/centrais-de-conteudo/materiais-educativos-e-publicacoes/guia-orientativo-tratamento-de-dados-pessoais-para-fins-academicos-e-para-a-realizacao-de-estudos-e-pesquisas) |

### 2.2 Princípios direcionados à interface

| Princípio/norma | Aplicabilidade ao contexto | Decisão/requisito decorrente | Fonte |
|---|---|---|---|
| Acessibilidade (WCAG 2.2) | Fornece critérios de acessibilidade para interfaces web, relevantes como referência para uma eventual implementação digital do protótipo. | Planejar textos legíveis, identificação das informações sem depender apenas de cores, legendas em gráficos, controles reconhecíveis e navegação por teclado na implementação futura. | [WCAG 2.2 — W3C](https://www.w3.org/TR/WCAG22/) |
| Consistência e previsibilidade da navegação | O usuário precisa alternar entre histórico, comparação, avaliação, painel e evidências sem perder o entendimento do fluxo. | Manter nomenclatura consistente, preservar seleções quando possível e identificar claramente o destino dos botões. | Entregas 5 e 6 |
| Visibilidade do estado do sistema e prevenção de erros | Pesquisas sem resultados, referências incompatíveis e salvamentos sem confirmação podem comprometer a conclusão das tarefas. | Apresentar mensagens de estado, orientar recuperação de erros, indicar incompatibilidades e confirmar o salvamento de registros. | Entregas 5 e 6 |

### 2.3 Premissa de projeto: contexto de uso

O contexto de uso é tratado como uma premissa que orienta os dois grupos de princípios, pois não representa propriamente uma norma ou guideline, mas uma condição fundamental para as decisões do projeto.

Os usuários realizam atividades distintas de avaliação, investigação e comunicação. A interface precisa refletir essas diferenças e considerar o ambiente acadêmico e técnico.

Dessa forma, os fluxos devem ser organizados conforme as tarefas T01, T02 e T03, priorizando as informações necessárias para alcançar os objetivos dos usuários.

**Fonte:** Entregas 1, 3, 4 e 5.

## 3. Metas de usabilidade

Usabilidade deve ser discutida **no contexto de uso**. As metas quantitativas devem dizer o que será medido, em qual tarefa, com qual população e qual limite será considerado aceitável.

A priorização das metas utiliza os cinco atributos de usabilidade de Nielsen trabalhados na disciplina:

- **Facilidade de aprendizado:** facilidade para o usuário aprender a utilizar a interface durante o primeiro contato.
- **Facilidade de memorização:** facilidade para lembrar como utilizar a interface após um período sem utilizá-la.
- **Eficiência:** capacidade de realizar as tarefas com rapidez e sem ações desnecessárias.
- **Baixa taxa de erros:** capacidade de evitar erros e permitir que o usuário realize suas tarefas corretamente.
- **Satisfação:** percepção positiva do usuário durante a utilização da interface.

Esses atributos serão utilizados para organizar e justificar a importância das metas do projeto.

### 3.1 Metas qualitativas

| Meta | Para quem/tarefa | Evidência desejada | Justificativa |
|---|---|---|---|
| Compreensão clara dos resultados apresentados | P01 — T01 | O participante consegue explicar quais indicadores melhoraram e quais pioraram, utilizando as informações da interface sem confundir métricas ou execuções. | A avaliação de um treinamento não pode depender de uma única métrica isolada. |
| Identificação adequada do contexto da comparação | P01 e P02 — T01 e T02 | O participante reconhece os IDs, as versões e os parâmetros das execuções e identifica possíveis incompatibilidades. | Comparações entre experimentos realizados em condições diferentes podem produzir conclusões equivocadas. |
| Facilidade para localizar resultados anteriores | P02 — T02 | O participante compreende os controles de busca e filtros, seleciona os registros desejados e sabe como corrigir uma pesquisa sem resultados. | O histórico precisa apoiar a recuperação das informações. |
| Continuidade da navegação durante apresentações | P03 — T03 | O participante consegue abrir uma evidência detalhada e retornar à apresentação sem perder o período ou o indicador que estava analisando. | Consultas durante reuniões não devem interromper desnecessariamente o fluxo da comunicação. |
| Compreensão das mensagens de erro e confirmação | P01, P02 e P03 — T01, T02 e T03 | O participante compreende mensagens de ausência de dados, incompatibilidade e salvamento, identificando a ação seguinte. | Mensagens claras reduzem incerteza, decisões equivocadas e abandono das tarefas. |
| Facilidade de aprendizado no primeiro contato | P01, P02 e P03 — T01, T02 e T03 | O participante consegue compreender a organização da interface e realizar as operações principais após uma orientação inicial, sem depender constantemente de ajuda. | Os usuários podem apresentar diferentes níveis de familiaridade com a plataforma e com os termos técnicos utilizados. |
| Facilidade de memorização dos procedimentos | P01, P02 e P03 — T01, T02 e T03 | O participante consegue repetir operações de consulta, comparação e navegação após um período sem utilizar a interface. | A interface deve permitir que os usuários recuperem os procedimentos aprendidos sem precisar reaprender todas as funcionalidades. |

### 3.2 Metas quantitativas

| ID | Atributo de Nielsen | Métrica | Tarefa/escopo | Meta | Como medir | Justificativa |
|---|---|---|---|---|---|---|
| MU01 | Baixa taxa de erros | Taxa de conclusão correta, sem ajuda do moderador. | T01 — Avaliar melhoria de treinamento. | >= 80% dos participantes. | Observar quantos participantes identificam ganhos e regressões, selecionam uma conclusão justificada e concluem o registro sem receber instruções adicionais. | A avaliação é crítica porque interpretações incorretas podem orientar ajustes inadequados nos treinamentos. |
| MU02 | Baixa taxa de erros | Taxa de conclusão correta, sem ajuda do moderador. | T02 — Localizar e comparar execuções. | >= 80% dos participantes. | Verificar quantos localizam as duas execuções solicitadas, realizam a comparação e registram uma hipótese distinguindo evidências e ressalvas. | A comparação é crítica para entender se os ajustes no treinamento estão trazendo resultados positivos. |
| MU03 | Baixa taxa de erros | Taxa de conclusão correta da apresentação e consulta de evidências. | T03 — Consultar síntese e comunicar resultados. | >= 80% dos participantes. | Observar quantos selecionam o período, identificam ao menos um ponto relevante, consultam uma evidência e retornam ao contexto anterior. | A interface precisa apoiar reuniões sem prejudicar a continuidade da análise e a interpretação das informações. |
| MU04 | Eficiência | Tempo mediano para concluir cada tarefa com sucesso. | T01 e T02. | <= 6 minutos por tarefa. | Cronometrar desde o início do cenário até a conclusão, considerando apenas execuções bem-sucedidas e registrando a mediana separadamente para T01 e T02. | A avaliação e a comparação devem ocorrer sem navegação excessiva ou repetição desnecessária de ações. |
| MU05 | Eficiência | Tempo necessário para consultar uma evidência detalhada e retornar ao contexto anterior, preservando as seleções realizadas. | T03 — Consulta de evidência durante a reunião. | <= 2 minutos por consulta. | Cronometrar desde a solicitação de consulta à evidência até o retorno à apresentação, verificando se o período e o indicador selecionados foram preservados. | A consulta durante reuniões precisa ser rápida para evitar interrupções e perda de continuidade na apresentação. |
| MU06 | Satisfação | Avaliação subjetiva de facilidade de uso após cada tarefa. | T01, T02 e T03. | Mediana >= 4 em escala de 1 a 5. | Aplicar uma pergunta pós-tarefa com escala de 1 (muito difícil) a 5 (muito fácil) e calcular a mediana por tarefa. | A satisfação complementa as demais medidas, permitindo identificar desconforto mesmo quando a tarefa é concluída. |
| MU07 | Baixa taxa de erros | Quantidade de erros críticos que comprometem a integridade da análise. | T01 e T02. | Zero erros críticos nos testes avaliados. | Registrar casos de associação da conclusão à execução errada, seleção incorreta de referência sem percepção da incompatibilidade ou interpretação de registro não salvo como salvo. | Erros desse tipo comprometem a confiabilidade das análises e precisam receber prioridade de correção. |
| MU08 | Eficiência | Taxa de retorno ao contexto anterior sem refazer seleções. | T03 — Consulta de evidência durante a reunião. | >= 80% dos participantes. | Observar quantos conseguem retornar à apresentação mantendo o período, o indicador e o ponto anterior, sem intervenção do moderador. | Preservar o contexto evita retrabalho e interrupções durante as reuniões. |
| MU09 | Facilidade de aprendizado | Taxa de conclusão correta de uma tarefa de consulta ao histórico no primeiro contato com a interface. | T02 — Primeiro contato com a localização de execuções. | >= 80% dos participantes. | Solicitar que os participantes realizem uma consulta ao histórico após uma orientação inicial padronizada de até 5 minutos, sem ajuda adicional do moderador, registrando quantos concluem corretamente a tarefa. | A interface deve ser compreensível mesmo para usuários que ainda não conhecem seus controles e sua organização. |
| MU10 | Facilidade de memorização | Taxa de conclusão correta de uma tarefa após um período sem utilizar a interface. | T02 — Repetição da consulta ao histórico. | >= 75% dos participantes. | Após um intervalo de 7 dias sem utilizar a interface, solicitar que os participantes repitam a tarefa de consulta ao histórico, sem reapresentação do tutorial ou ajuda do moderador, registrando quantos conseguem concluí-la corretamente. | A interface deve permitir que os usuários recuperem os procedimentos aprendidos anteriormente sem precisar reaprender sua utilização. |

### 3.3 Priorização das metas

Os pesos representam a importância relativa de cada meta para o projeto e não devem ser confundidos com os valores aceitáveis de desempenho ou com os resultados dos testes.

A priorização foi reorganizada considerando os cinco atributos de Nielsen trabalhados na disciplina.

| Atributo de usabilidade | Meta | Peso de prioridade | Justificativa |
|---|---|---:|---|
| Facilidade de aprendizado | **MU09 — Aprendizado no primeiro contato** | 15% | É importante que usuários com diferentes níveis de familiaridade consigam aprender a utilizar as funcionalidades principais da interface. |
| Facilidade de memorização | **MU10 — Memorização dos procedimentos** | 5% | A possibilidade de recuperar procedimentos após um período sem utilização contribui para o uso recorrente da plataforma. |
| Eficiência | **MU04 — Eficiência na avaliação e comparação** | 10% | Reduzir o esforço necessário para interpretar e comparar experimentos melhora a utilização recorrente da interface. |
| Eficiência | **MU05 — Eficiência na consulta durante reuniões** | 5% | A rapidez na consulta de evidências é relevante, mas não deve se sobrepor à compreensão correta das informações. |
| Eficiência | **MU08 — Continuidade da navegação** | 5% | Preservar informações durante consultas e retornos evita retrabalho e interrupções. |
| Baixa taxa de erros | **MU01 — Baixa ocorrência de erros na avaliação de treinamentos** | 15% | A interpretação correta dos resultados é fundamental para orientar decisões sobre os treinamentos do robô. |
| Baixa taxa de erros | **MU02 — Baixa ocorrência de erros na comparação de execuções** | 10% | A localização e comparação correta dos experimentos sustenta a rastreabilidade das análises. |
| Baixa taxa de erros | **MU03 — Baixa ocorrência de erros na comunicação dos resultados** | 10% | A apresentação deve permitir identificar questões relevantes para discussão e investigação sem comprometer a interpretação das informações. |
| Baixa taxa de erros | **MU07 — Prevenção de erros críticos** | 15% | Atribuir resultados a execuções incorretas ou registrar conclusões equivocadas pode comprometer decisões técnicas. |
| Satisfação | **MU06 — Satisfação dos usuários** | 10% | A percepção de facilidade e conforto é importante para a aceitação da interface. |
| **Total** | | **100%** | |

A equipe atribuiu maior peso à baixa taxa de erros, pois o objetivo principal da interface é apoiar a interpretação correta dos resultados experimentais e evitar decisões baseadas em comparações ou registros incorretos.

A facilidade de aprendizado também recebeu uma prioridade significativa, considerando que os usuários podem apresentar diferentes níveis de familiaridade com os termos técnicos e com a organização da interface.

A eficiência, a facilidade de memorização e a satisfação também são consideradas importantes, pois contribuem para que a plataforma seja compreensível e adequada à utilização recorrente, sem comprometer a qualidade das decisões realizadas pelos usuários.

## 4. Como o ciclo será iterado

O desenvolvimento da interface seguirá o **Ciclo de Vida de Engenharia de Usabilidade de Mayhew**, modelo trabalhado na disciplina, que organiza o desenvolvimento em etapas sucessivas e iterativas, considerando as necessidades dos usuários, os requisitos de usabilidade, o projeto da interface, as avaliações e a evolução do produto.

O modelo é composto por três níveis de projeto:

1. **Nível 1 — Projeto essencial:** envolve a compreensão dos usuários, do contexto de uso, das tarefas e dos requisitos de usabilidade, incluindo a definição do modelo conceitual e a elaboração de protótipos iniciais.
2. **Nível 2 — Padrões de telas e diálogos:** envolve a definição da organização das telas, dos padrões de interação, da navegação e das diretrizes visuais, incluindo a elaboração de um guia de estilo.
3. **Nível 3 — Projeto detalhado:** envolve o detalhamento das telas, dos diálogos, dos controles e dos comportamentos da interface, refinando os elementos definidos nos níveis anteriores.

Esses três níveis são desenvolvidos de maneira iterativa para cada grupo de funcionalidades essenciais. Após o desenvolvimento e a avaliação das funcionalidades, o processo avança para a fase de instalação, na qual o produto em utilização permite obter retorno de usuários reais e identificar melhorias para versões futuras.

As quatro atividades descritas a seguir representam como a equipe pretende aplicar esse modelo ao projeto.

### Etapa 1 — Compreensão das necessidades e projeto essencial (Nível 1)

As Entregas 1 a 5 estabeleceram o escopo de IHC, as personas, os cenários e as tarefas principais. A Entrega 7 definiu instrumentos para investigar as hipóteses H01b, H02 e H03, que permanecem abertas na rastreabilidade.

Essa atividade corresponde principalmente ao Nível 1 do modelo de Mayhew, pois envolve a compreensão do contexto de uso, a identificação das necessidades dos usuários e a definição dos requisitos e das metas de usabilidade.

Após a aplicação dos instrumentos, os resultados deverão ser utilizados para verificar se as atividades e necessidades consideradas pela equipe correspondem ao trabalho real dos usuários.

**Artefatos revisitados:** personas, cenários, descrição das tarefas, escopo de interação e `RASTREABILIDADE.md`.

### Etapa 2 — Revisão dos protótipos e padrões de telas e diálogos (Nível 2)

A Entrega 6 apresentou telas em papel para representar os fluxos de consulta ao histórico, comparação de execuções, avaliação de treinamentos e acompanhamento do desempenho.

As observações obtidas em avaliações formativas deverão orientar ajustes na organização das informações, no funcionamento dos controles e na navegação entre telas.

Essa atividade representa a transição do Nível 1 para o Nível 2 do modelo de Mayhew. A partir do entendimento das necessidades dos usuários e dos primeiros protótipos, serão definidos padrões de telas, diálogos, navegação e apresentação das informações.

Alguns pontos que merecem investigação são:

- Clareza das legendas dos gráficos e identificação das execuções.
- Compreensão do termo baseline e dos critérios de comparação.
- Apresentação das diferenças de configuração.
- Identificação de estados de erro e ausência de dados.
- Comportamento dos botões de retorno.
- Preservação do contexto durante a consulta a evidências.
- Feedback após o registro de avaliações e hipóteses.

Esses pontos representam aspectos a verificar, não resultados de usabilidade já comprovados.

**Artefatos revisitados:** protótipos da Entrega 6, fluxos de navegação, descrições das telas e padrões de interação.

### Etapa 3 — Projeto detalhado e avaliação da usabilidade (Nível 3)

Nas etapas posteriores da disciplina, serão elaborados cenários de teste para verificar as metas quantitativas e qualitativas definidas nesta entrega.

Essa atividade corresponde ao Nível 3 do modelo de Mayhew, no qual os elementos da interface são detalhados e avaliados, considerando o comportamento das telas, os controles, os diálogos e os fluxos de interação.

Os participantes serão convidados a realizar tarefas próximas às atividades de T01, T02 e T03, sem receber orientações sobre quais controles devem utilizar.

Durante a interação, serão registrados os resultados das tarefas, os tempos de execução, os erros, os pedidos de ajuda e as dificuldades observadas.

Após cada tarefa, poderá ser aplicada uma pergunta de satisfação utilizando a escala definida na meta MU06.

Os resultados serão comparados aos critérios de aceitação estabelecidos nesta entrega, permitindo identificar quais aspectos da interface atendem às metas e quais precisam de revisão.

**Artefatos produzidos ou revisitados:** roteiros de teste, registros de observação, métricas de usabilidade, relatórios de avaliação e matriz de rastreabilidade.

### Etapa 4 — Revisão e nova iteração

A equipe analisará os problemas identificados, considerando sua gravidade, frequência e impacto na conclusão das tarefas.

Problemas que provocarem erros críticos, perda de informações ou impossibilidade de concluir uma tarefa terão prioridade sobre ajustes puramente visuais.

Após a revisão, os fluxos afetados deverão ser avaliados novamente, quando possível, para verificar se as alterações produziram melhorias.

Os níveis de projeto essencial, padrões de telas e diálogos e projeto detalhado poderão ser retomados sempre que novas evidências indicarem a necessidade de modificar a interface, as tarefas ou os requisitos de usabilidade.

Após o desenvolvimento e a avaliação dos grupos de funcionalidades, o modelo de Mayhew prevê a fase de instalação. Nessa fase, o produto passa a ser utilizado em seu contexto real, permitindo coletar retornos dos usuários e identificar necessidades de melhoria para versões futuras.

**Posicionamento atual do projeto:** a equipe já desenvolveu atividades relacionadas ao Nível 1, principalmente por meio da definição de personas, tarefas, requisitos e protótipos em papel da Entrega 6. As próximas entregas deverão avançar para o Nível 2, com a definição dos padrões de telas, diálogos e navegação. Posteriormente, será desenvolvido o Nível 3, com o detalhamento e a avaliação das funcionalidades.

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
- [X] Princípios direcionados ao negócio e à interface estão organizados separadamente.
- [X] Contexto de uso foi apresentado como premissa que orienta os dois grupos de princípios.
- [X] Metas quantitativas são mensuráveis e associadas a tarefas/público.
- [X] A priorização das metas considera os cinco atributos de usabilidade de Nielsen.
- [X] Existem metas específicas de facilidade de aprendizado e facilidade de memorização.
- [X] A meta MU05 possui métrica, tarefa, meta numérica e forma de medição definidos.
- [X] Os pesos de priorização das metas totalizam 100%.
- [X] O Ciclo de Vida de Engenharia de Usabilidade de Mayhew foi explicitado.
- [X] Os três níveis do modelo foram relacionados às atividades do projeto.
- [X] Foi indicado em qual nível o projeto se encontra e quais serão os próximos avanços.
- [X] Metas poderão ser verificadas nas Entregas 12–14.

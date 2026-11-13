# Entrega 9 — Modelo conceitual e design centrado na comunicação

**Data:** 06/11/2026 <br>
**Status:** 🟩 concluída <br>
**Responsabilidade:** soluções individuais, com consolidação da equipe para mapa de objetivos e esquema de signos.

## Objetivo da atividade

Passar do cenário de problema para uma concepção da interação, explicitando objetivos, tópicos de conversa, falas e signos que a interface deverá comunicar/manipular.

## Transformando resultados técnicos em conceitos compreensíveis

Em TCCs algorítmicos ou orientados a dados, esta entrega deve evitar que a interface exponha apenas estruturas internas do código. Identifique os **conceitos e signos que fazem sentido para o usuário**.

Exemplos:

- `query plan`, custo estimado, recomendação e impacto para um DBA;
- modelo, dataset, versão, execução e métrica para engenheiro de IA;
- período, indicador, grupo, tendência e filtro para gestor/analista;
- alerta, severidade, evidência, responsável e status para analista de segurança.

Se um termo técnico for necessário, modele como será comunicado, explicado e relacionado à tarefa.

Dashboards, relatórios, filtros e CRUDs devem aparecer no modelo conceitual por meio dos **objetivos, signos e conversas** que justificam sua existência.


# 1. Cenários de interação

## CI01 Análise do desempenho do robô

**Autor(a):** Letizia Lowatzki Baptistella  22.125.063-2  
**Origem:** Cenário problema C01: Análise de Performance do Robô.

### Cenário de interação

Rafael Martins, estudante e integrante técnico de uma equipe de robótica humanoide, está desenvolvendo e testando o comportamento do robô para partidas de futebol. Após realizar um novo treinamento, ele precisa verificar se o resultado representa uma melhoria em relação aos experimentos anteriores e decidir quais ajustes devem ser realizados no próximo treinamento.<br>
Durante o desenvolvimento, Rafael acompanha o resultado do treinamento por meio das métricas obtidas e da observação do comportamento do robô. Nessa análise, verifica a velocidade média, a distância percorrida, a taxa de quedas, a estabilidade durante o movimento e a localização do robô. **Na interface, ele consulta essas informações relacionadas à execução selecionada, após o treino, podendo observar os indicadores e o comportamento correspondente do robô na simulação.** <br>
Antes de executar um novo treinamento, Rafael e a equipe verificam como foi o resultado anterior, a fim de entender se houve uma boa avaliação. **A interface permite consultar essas avaliações de execução, para que Rafael considere os resultados em relação ao desempenho anterior do robô. A interface permitirá abrir os treinos comparados em uma mesma tela, para visualização fácil** <br>
Depois disso, Rafael realiza ajustes nos parâmetros, realiza o treino, e observa uma melhora na velocidade. Apesar disso, o robô permanece menos tempo equilibrado, percorre uma distância maior, mas cai com frequência. O resultado, portanto, não representa necessariamente uma melhoria na capacidade de jogar. **Ao consultar os indicadores em conjunto, Rafael consegue analisar quais aspectos apresentaram melhora e quais apresentaram piora, evitando considerar apenas uma métrica isolada. Dessa forma, a interface centralizará essas métricas em uma unica tela** <br>
Para entender melhor o que aconteceu, Rafael compara as métricas e as configurações utilizadas anteriormente. **Ele consulta os resultados e os parâmetros de treinamentos anteriores que possam servir de referência, relacionando as diferenças encontradas às alterações realizadas na caminhada.** <br>
**Durante a comparação, Rafael verifica se as informações disponíveis permitem relacionar as execuções. Quando faltam dados sobre algum treinamento, ele precisa considerar essa limitação antes de concluir quais alterações podem ter influenciado o desempenho.** <br>
Ao final da análise, Rafael considera o conjunto das métricas e o comportamento observado para decidir se mantém os parâmetros utilizados ou realiza novos ajustes no próximo treinamento. **Dessa forma, utiliza os resultados das execuções anteriores como apoio para definir os próximos experimentos.** <br>
A análise é realizada durante os ciclos de desenvolvimento do robô, em um computador utilizado para executar os treinamentos. Como novos treinamentos são realizados a partir dos resultados anteriores, uma interpretação incorreta pode levar Rafael e a equipe a escolher parâmetros inadequados para o próximo experimento, desperdiçando tempo computacional e prolongando os ciclos de desenvolvimento.

### Diferenças relevantes

| Alteração | Por que foi necessária | Evidência/artefato que justifica |
|---|---|---|
| Consulta conjunta das métricas e do comportamento visual | Permitir que Rafael relacione os valores ao comportamento do robô. | C01 refinado e Entrega 3, P01: necessidade de analisar diferentes métricas e relacioná-las ao comportamento observado. |
| Análise conjunta dos indicadores | Evitar que uma melhora isolada seja interpretada como melhoria geral. | C01 refinado, questão Q1: considerar as informações em conjunto para avaliar o treinamento. |
| Comparação de treinamentos anteriores | Facilitar a identificação de diferenças entre métricas e configurações. | C01 refinado, questões Q4 e Q5: escolha de treinamentos de referência e comparação de resultados e configurações. |
| Consideração de informações ausentes | Evitar conclusões sem evidências suficientes para relacionar os resultados às configurações. | Entrega 3, P01: informações distribuídas entre execuções; C01: necessidade de consultar e relacionar resultados anteriores. |
| Utilização dos resultados para decidir novos ajustes | Apoiar a escolha dos parâmetros do próximo treinamento. | C01 refinado, questão Q7: decidir se mantém os parâmetros ou realiza novos ajustes. |

## CI02 Recuperação da configuração de um treinamento anterior para comparação

**Autor(a):** Manuella Filipe Peres 22.224.029-3  
**Origem:** Cenário problema C02: Recuperação da configuração de um treinamento anterior.

### Cenário de interação

Marina Oliveira, pesquisadora de robótica, está investigando diferentes estratégias utilizadas para melhorar o desempenho de um robô humanoide em simulação. Durante sua pesquisa, ela analisa resultados de treinamentos anteriores para compreender como as alterações nos parâmetros influenciam o comportamento do robô e identificar experimentos que possam servir de referência para novas investigações.
Após consultar resultados recentes que não apresentaram melhorias significativas, Marina se lembra de um treinamento realizado algumas semanas antes, no qual o robô percorreu uma distância maior e apresentou menor frequência de quedas. Ela decide investigar esse experimento para compreender quais configurações contribuíram para o resultado obtido. <br>
**Para localizar o treinamento, Marina consulta os registros das execuções e examina os arquivos de métricas disponíveis, procurando identificar o experimento que apresentou os resultados que deseja investigar. Ela poderá busca por id ou utilizando filtro.**
Para isso, Marina precisa identificar os parâmetros utilizados naquela execução. Entretanto, os parâmetros são configurados diretamente no código antes dos treinamentos, e diferentes alterações foram realizadas desde então. Ao consultar a pasta do experimento, ela encontra o modelo salvo e algumas anotações da equipe, mas essas informações não reúnem todos os valores utilizados na configuração original. <br>
**Na interface, Marina consulta as informações disponíveis sobre a execução selecionada, incluindo os resultados e as observações associadas ao experimento. Quando necessário, ela também precisa consultar os arquivos de configuração e o histórico do código para recuperar informações que não estejam reunidas nos registros da execução.**<br>
**Quando algum parâmetro não está disponível, a interface indica que a informação não foi registrada, sem apresentar um valor presumido. Assim, Marina consegue distinguir os dados recuperados daqueles que ainda precisam ser investigados.** <br>
Marina procura relacionar os resultados do treinamento anterior aos das execuções recentes, mas encontra dificuldades para confirmar se os experimentos foram realizados nas mesmas condições. **Para verificar se os resultados podem ser comparados, ela consulta as informações disponíveis sobre os parâmetros de execução. Quando os registros não são suficientes, precisa buscar esclarecimentos com os integrantes responsáveis pelos experimentos.** <br>
Sem essa confirmação, Marina não consegue determinar com segurança quais alterações podem ter influenciado as diferenças observadas no desempenho do robô. **Quando não consegue confirmar as configurações utilizadas, ela avalia se o treinamento pode ser utilizado como referência ou se será necessário obter informações adicionais ou realizar uma nova execução.** <br>
**Depois de identificar o experimento relevante, Marina pretende manter suas informações como referência e backup para avaliar, após novos ajustes, se o desempenho do robô melhorou ou piorou.**
Essa situação facilita a interpretação dos resultados e reduz a dependência da busca manual por informações distribuídas entre diferentes arquivos e registros, apoiando a escolha de experimentos anteriores como referência para novas investigações.

### Diferenças relevantes

| Alteração | Por que foi necessária | Evidência/artefato que justifica |
|---|---|---|
| Consulta aos registros e arquivos de métricas para localizar uma execução | Representar como Marina identifica o treinamento que deseja investigar. | C02 refinado, questão Q1: localização do treinamento entre pastas e arquivos de métricas. |
| Consulta das configurações e dos registros associados à execução | Permitir recuperar os parâmetros utilizados sem depender apenas das anotações. | C02 refinado, questão Q2: informações incompletas nas anotações e necessidade de consultar arquivos de configuração e histórico do código. |
| Identificação de parâmetros não registrados | Evitar que informações ausentes sejam tratadas como conhecidas. | C02 refinado, questão Q2: as anotações nem sempre apresentam todos os parâmetros. |
| Consulta das condições dos experimentos | Verificar se diferentes treinamentos podem ser comparados. | C02 refinado, questão Q3: necessidade de verificar se os experimentos foram realizados em condições comparáveis. |
| Busca de esclarecimentos com integrantes da equipe | Permitir recuperar informações que não estão disponíveis nos registros consultados. | C02 refinado, questões Q3 e Q4: necessidade de consultar os responsáveis pelos treinamentos e pelas alterações. |
| Avaliação sobre utilizar o treinamento como referência ou realizar nova execução | Representar a decisão tomada quando não é possível confirmar as configurações. | C02 refinado, questão Q5: avaliar se o experimento pode ser utilizado como referência ou se são necessárias informações adicionais ou nova execução. |


## CI03   Avaliação de treinamentos em reunião de orientação

**Autor(a):** Rafaela Altheman de Campos 22.125.062-4  
**Origem:** cenário problema C03 Avaliação de treinamentos em reunião de orientação.

### Cenário de interação

Carlos Almeida, professor e orientador de uma equipe universitária de robótica humanoide, acompanha o desenvolvimento de um robô projetado para jogar futebol. Como não participa diretamente de todos os treinamentos, utiliza as reuniões com os estudantes para compreender os resultados obtidos e orientar as próximas etapas do desenvolvimento.
**Antes da reunião, a estudante responsável pela apresentação seleciona os resultados que pretende discutir com Carlos. A interface permite consultar as informações das execuções e organizar os indicadores relevantes para a apresentação, considerando o tempo disponível para a discussão.** <br>
Durante uma reunião de acompanhamento, uma estudante apresenta os resultados de um treinamento recente. O gráfico da recompensa indica um aumento em relação à execução anterior, sugerindo inicialmente uma possível melhoria. Entretanto, Carlos precisa compreender se essa evolução numérica corresponde a um avanço real no comportamento do robô. <br>
**Para avaliar o treinamento, Carlos consulta a diversos indicadores, como distância percorrida, velocidade, estabilidade e frequência de quedas. Também pode relacionar esses resultados ao comportamento do robô durante a simulação.** <br>
Para isso, pergunta qual foi a distância percorrida, quantas quedas ocorreram e quais alterações foram realizadas em comparação ao treinamento anterior. **Quando precisa investigar algum resultado, Carlos consulta as informações da execução, incluindo os arquivos de métricas, as anotações da equipe e a visualização do robô no simulador, sem depender apenas do dado apresentado inicialmente.** <br>
Ao observar o comportamento do robô, Carlos percebe que ele permanece equilibrado durante parte da execução, mas apresenta pouco deslocamento. Dessa forma, o aumento da recompensa não representa necessariamente uma melhoria na capacidade de caminhar. **A consulta conjunta dos indicadores e do comportamento observado permite que Carlos e a estudante discutam as diferenças entre o resultado numérico e o desempenho apresentado pelo robô.** <br>
Como algumas informações precisam ser recuperadas e comparadas durante a reunião, a equipe encontra dificuldades para concluir a avaliação no tempo disponível. **As conclusões discutidas durante o acompanhamento podem ser registradas nas anotações de evidências, incluindo os problemas identificados, os pontos que exigem investigação e os próximos ajustes propostos.** <br>
Ao final da discussão, Carlos utiliza as informações apresentadas para orientar a equipe sobre quais aspectos precisam ser investigados e quais ajustes podem ser considerados nos próximos treinamentos. **Caso a avaliação não possa ser concluída, a equipe identifica quais informações ainda precisam ser analisadas antes de definir os próximos ajustes.** <br>
Dessa forma, a reunião consegue se concentrar na interpretação dos resultados e na definição dos próximos passos, reduzindo o tempo gasto para recuperar informações e facilitando o acompanhamento da evolução do projeto.

**OBS: Apesar de termos descrito anteriomente como papel do estudante separar a execução que será apresentada, esta etapa poderia ser feita por Carlos também, sendo este uma das personas pelo qual a interface foi modelada. Além disso, paramos de utilizar a "recompensa" como parâmetro primordial pois não estamos tratando apenas de treinos de caminhada de robôs humanoides, mas sim de robôs humanoides que jogam futebol (houve mudança do escopo)**

### Diferenças relevantes

| Alteração | Por que foi necessária | Evidência/artefato que justifica |
|---|---|---|
| Seleção prévia dos resultados para apresentação | Permitir que a estudante (ou Carlos) organize as informações relevantes antes da reunião. | C03 refinado, questões Q1 e Q3: preparação da apresentação e ausência de indicadores importantes. |
| Visão conjunta dos principais indicadores | Permitir que Carlos avalie o desempenho sem depender apenas de um (1) dado numérico. | C03 refinado, questão Q2: considerar distância, velocidade, estabilidade e frequência de quedas. |
| Relação entre indicadores e execução visual | Ajudar a interpretar se a evolução numérica corresponde à melhoria real da caminhada. | C03 refinado, questões Q2 e Q4: relacionar métricas ao comportamento observado e questionar resultados aparentemente positivos. |
| Consulta dos detalhes durante a reunião | Permitir investigar dúvidas sem depender da busca manual em diferentes arquivos e registros. | C03 refinado: necessidade de consultar arquivos de métricas, anotações e simulador durante a reunião. |
| Registro das conclusões e orientações | Preservar os pontos discutidos para apoiar as atividades posteriores da equipe. | C03 refinado, questão Q5: registrar problemas, pontos que exigem investigação e próximos ajustes nas anotações compartilhadas do projeto. |
| Identificação de pontos que exigem análise complementar | Evitar decisões precipitadas quando a avaliação não pode ser concluída durante a reunião. | C03 refinado, questão Q6: adiamento da decisão e impacto no planejamento dos próximos treinamentos. |

# 2. Design centrado na comunicação

## CI01   Análise do desempenho do robô

| Tópico > subtópico | Falas e signos envolvidos | Intenção/efeito esperado |
|---|---|---|
| Enviar treinamento | `U: Quero enviar os resultados do treinamento que acabei de realizar.` / `D: Selecione os arquivos do treinamento e informe a identificação. Algumas informações não foram encontradas nos arquivos: confirma o envio mesmo assim?` | Disponibilizar o treinamento para análise e informar, desde o início, o que não foi registrado. |
| Avaliar desempenho | `U: Quero verificar se o treinamento melhorou a caminhada do robô.` / `D: Consulte os indicadores e o comportamento do robô nesta execução. Depois, classifique o treinamento como melhora, não melhora ou falta de evidências e, se quiser, registre uma observação.` | Permitir uma avaliação baseada em diferentes informações e registrar o resultado dessa avaliação. |
| > Consultar métricas | `U: Quero analisar a velocidade, a distância, as quedas, a localização e a estabilidade.` / `D: Estes são os indicadores registrados para esta execução, reunidos em uma mesma tela.` | Apresentar os principais indicadores do treinamento. |
| > Observar comportamento | `U: Quero verificar como o robô se comportou durante a execução.` / `D: Consulte a visualização correspondente ao treinamento.` | Relacionar resultados quantitativos ao comportamento observado. |
| Consultar avaliações | `U: Quero verificar se o resultado atingiu melhora.` / `D: Verifique qual foi a avaliação daquele treinamento: melhora, não melhora ou falta de evidências, e leia as observações registradas.` | Relacionar a avaliação aos objetivos definidos pela equipe, para  determinar se os treinos estão apresentando bons resultados |
| Comparar treinamentos | `U: Quero comparar esta execução com uma anterior.` / `D: Escolha os dois treinamentos que deseja comparar; os resultados e as configurações serão exibidos lado a lado, na mesma tela.` | Permitir identificar diferenças entre experimentos. |
| > Verificar diferenças | `U: O que mudou entre os treinamentos?` / `D: Consulte as diferenças entre as métricas e os parâmetros disponíveis.` | Relacionar alterações de configuração aos resultados. |
| > Considerar informações disponíveis | `U: Tenho informações suficientes para comparar estas execuções?` / `D: Verifique os registros disponíveis para cada treinamento e considere os dados que não foram registrados.` | Comunicar limitações e evitar conclusões sem evidência suficiente. |
| Planejar ajustes | `U: Quero decidir o que devo ajustar no próximo treinamento.` / `D: Considere o conjunto das métricas, o comportamento observado e as diferenças entre as execuções. Registre os próximos ajustes como anotação.` | Apoiar a decisão sobre novos experimentos. |

## CI02   Recuperação da configuração de um treinamento anterior

| Tópico > subtópico | Falas e signos envolvidos | Intenção/efeito esperado |
|---|---|---|
| Recuperar treinamento | `U: Quero encontrar um treinamento realizado anteriormente.` / `D: Consulte os registros e os arquivos das execuções disponíveis.` | Facilitar a localização de uma execução. |
| > Localizar execução | `U: Quero encontrar o treinamento que apresentou menor frequência de quedas.` / `D: Busque pela identificação do treinamento ou use os filtros (robô, período, versão ou avaliação) para encontrar a execução com esse resultado.` | Ajudar a identificar o experimento desejado. |
| Consultar resultados | `U: Quero verificar o desempenho desse treinamento.` / `D: Estes são os resultados registrados para a execução selecionada.` | Apresentar os indicadores relacionados ao experimento. |
| Recuperar configurações | `U: Quero saber quais parâmetros foram utilizados.` / `D: Consulte as configurações e os registros disponíveis para esta execução.` | Permitir recuperar o contexto técnico do treinamento. |
| > Consultar registros complementares | `U: Quero verificar se existem outras informações sobre essa configuração.` / `D: Consulte as anotações da equipe, os arquivos de configuração e o histórico do código enviados com o treinamento.` | Orientar a recuperação de informações distribuídas entre diferentes registros. |
| > Identificar dados ausentes | `U: Por que não aparece o valor deste parâmetro?` / `D: Esta informação não está disponível nos registros consultados.` | Comunicar ausência de informação sem presumir valores. |
| Comparar execuções | `U: Quero comparar esse treinamento com outro mais recente.` / `D: Consulte as métricas, os parâmetros e as condições disponíveis para cada execução.` | Facilitar a identificação de diferenças entre experimentos. |
| > Verificar condições | `U: Os treinamentos foram realizados nas mesmas condições?` / `D: Verifique as informações disponíveis. Quando os registros não forem suficientes, será necessário buscar esclarecimentos com os responsáveis pelos experimentos.` | Evitar comparações inadequadas. |
| Avaliar referência | `U: Posso utilizar esse treinamento como referência?` / `D: Considere as configurações e as condições registradas. Se faltarem informações, avalie a necessidade de obter dados adicionais ou realizar uma nova execução. Se decidir usá-lo, marque o treinamento como referência.` | Apoiar a decisão sobre a confiabilidade do experimento como referência. |

## CI03 Avaliação de treinamentos em reunião de orientação

| Tópico > subtópico | Falas e signos envolvidos | Intenção/efeito esperado |
|---|---|---|
| Preparar apresentação | `U: Quero apresentar os resultados mais relevantes do treinamento.` / `D: Consulte a execução e selecione os indicadores que serão discutidos na reunião.` | Organizar as informações para a reunião. |
| Consultar visão geral | `U: Quero entender rapidamente como foi o desempenho.` / `D: Consulte os principais indicadores registrados para esta execução.` | Facilitar a leitura geral pelo orientador. |
| > Analisar métricas | `U: A velocidade aumentou. Isso significa que a caminhada melhorou?` / `D: A velocidade deve ser analisada junto à distância, estabilidade e frequência de quedas.` | Evitar conclusões baseadas em uma única métrica. |
| > Observar execução | `U: Quero ver como o robô se comportou.` / `D: Consulte a visualização da execução correspondente no simulador.` | Relacionar os indicadores ao comportamento do robô. |
| Comparar resultados | `U: Como esse treinamento se compara ao anterior?` / `D: Consulte as diferenças entre os indicadores e as configurações das execuções.` | Apoiar a discussão sobre a evolução do treinamento. |
| Consultar detalhes | `U: Quero entender quais alterações foram realizadas.` / `D: Consulte os parâmetros e as informações registradas para cada execução.` | Permitir aprofundamento quando surgirem dúvidas. |
| Registrar orientação | `U: Quero guardar os pontos discutidos para a equipe.` / `D: Registre os problemas identificados, os pontos que precisam de investigação e os próximos ajustes nas anotações da reunião.` | Preservar as decisões da reunião. |
| Planejar próximos passos | `U: O que ainda precisamos investigar antes de iniciar outro treinamento?` / `D: Consulte os pontos identificados durante a reunião e as informações que ainda precisam ser verificadas.` | Apoiar o planejamento dos próximos experimentos. |

**Convenção:** `U` = usuário; `D` = preposto do designer/sistema, conforme a abordagem de Engenharia Semiótica adotada na disciplina.


## 3. Mapa de objetivos

Cada integrante apresenta seu mapa e a equipe cria um **mapa consolidado**, eliminando duplicidades e resolvendo conflitos de nomenclatura.

![Mapa consolidado](../assets/09_modelo_conceitual/mapa_objetivos.svg)

### Dicionário de objetivos

| ID | Objetivo | Persona(s) | Cenário(s) | Prioridade |
|---|---|---|---|---|
| O01 | **localizar treinamento anterior** (instrumental): encontrar um treinamento já enviado, buscando pela identificação ou por filtros (robô, período, versão ou avaliação) | P01, P02, P03 | CI01, CI02, CI03 | Alta |
| O02 | **observar comportamento do robô na simulação**: relacionar os resultados numéricos ao comportamento do robô | P01, P02, P03 | CI01, CI03 | Alta |
| O03 | **consultar avaliação do treinamento**: verificar a avaliação registrada (melhora, não melhora ou falta de evidências) e as observações sobre o treinamento | P01, P02, P03 | CI01 | Média |
| O04 | **avaliar desempenho do treinamento** (final): a partir dos indicadores e do comportamento do robô, classificar o treinamento como melhora, não melhora ou falta de evidências e registrar observações, sem depender de uma única métrica | P01, P02, P03 | CI01, CI03 | Alta |
| O05 | **consultar condições de execução**: conhecer a situação em que o treinamento foi realizado | P01, P02, P03 | CI02 | Média |
| O06 | **consultar registros complementares** (instrumental): buscar parâmetros em anotações, arquivos de configuração e histórico do código enviados com o treinamento | P01, P02 | CI02 | Média |
| O07 | **identificar informações não registradas** (instrumental): distinguir o que foi recuperado do que ainda precisa ser investigado | P01, P02 | CI01, CI02 | Alta |
| O08 | **verificar informações disponíveis** (instrumental): saber se há dados suficientes para comparar e concluir | P01, P02 | CI01, CI02 | Alta |
| O09 | **verificar diferenças entre treinamentos**: relacionar alterações de parâmetros às mudanças nos resultados | P01, P02, P03 | CI01, CI02, CI03 | Alta |
| O10 | **verificar comparabilidade das condições**: confirmar se os treinamentos foram realizados em condições comparáveis | P01, P02 | CI02 | Alta |
| O11 | **comparar treinamentos** (final): comparar resultados, parâmetros e condições de dois treinamentos, exibidos lado a lado na mesma tela | P01, P02, P03 | CI01, CI02, CI03 | Alta |
| O12 | **avaliar treinamento como referência** (final): decidir se pode servir de referência, se faltam informações ou se é preciso nova execução, e marcá-lo como referência | P01, P02 | CI01, CI02 | Média |
| O13 | **selecionar execuções e indicadores a apresentar** (instrumental): preparar a reunião com o tempo disponível | P01, P03 | CI03 | Média |
| O14 | **consultar anotações de evidências**: rever problemas, pontos de investigação e ajustes já registrados nas reuniões | P01, P03 | CI03 | Média |
| O15 | **registrar conclusões da reunião** (final): guardar problemas, pontos a investigar e próximos ajustes | P01, P03 | CI03 | Média |
| O16 | **consultar pendências de investigação**: saber o que falta verificar antes de definir ajustes | P01, P02, P03 | CI03 | Média |
| O17 | **planejar ajustes do próximo treinamento** (final): definir os próximos ajustes (manter ou alterar parâmetros), registrados como anotação do tipo "próximo ajuste" | P01, P02 | CI01, CI03 | Alta |
| O18 | **fazer upload de treinamento** (instrumental): enviar os arquivos de um treinamento para análise, sabendo o que ficou sem registro | P01, P02 | CI01, CI02 | Alta |


## 4. Esquema conceitual de signos

Consolide as informações em **uma tabela única**.

**Legenda**

- **Origem:** *domínio* = conceito do mundo da robótica e dos treinamentos; *aplicação* = produzido ou calculado pelo sistema; *usuário* = informado pelo usuário.
- **Prevenção:** PP = prevenção passiva (explicação ou dica); PA = prevenção ativa (o sistema impede a fala inválida); AL = alerta, ou prevenção apoiada (pede decisão informada ao usuário).
- **Recuperação:** RA = recuperação apoiada; CE = captura de erro (indica algo a fazer fora do sistema).
- **+** marca o identificador do grupo. **—** significa que não se aplica.

| Grupo | Signo | Origem | Observações/semântica | Tipo de conteúdo | Restrição | Valor padrão | Prevenção | Recuperação |
|---|---|---|---|---|---|---|---|---|
| Envio | + arquivos do treinamento | usuário | Arquivos enviados para análise | arquivo | Formatos aceitos | — | PP: formatos permitidos | RA: selecionar novamente |
| Envio | identificação informada | usuário | Código do treinamento enviado | texto | Não nulo e único | — | PP: campo obrigatório | RA: corrigir ID |
| Envio | informações ausentes | aplicação | Dados não encontrados nos arquivos | lista | — | — | AL: confirmar envio incompleto | RA: adicionar arquivos |
| Treinamento | + identificação | domínio | Código único da execução | texto | Não nulo e único | — | PP: identificar execução | — |
| Treinamento | data | domínio | Data de realização | data | Não futura | — | PP: formato da data | — |
| Treinamento | versão | domínio | Versão do experimento | texto | — | — | — | — |
| Treinamento | situação do registro | aplicação | Informação registrada ou ausente | seleção simples | {registrado, não registrado} | Conforme registro | PP: indicar ausência | CE: consultar fonte |
| Histórico | + busca e filtros | usuário | Busca por ID, robô, período, versão ou avaliação | texto/seleção | Critérios válidos | Todos | PA: validar período | RA: corrigir filtros |
| Histórico | resultados da busca | aplicação | Execuções encontradas | lista | Pode estar vazia | — | — | RA: alterar busca |
| Indicadores | + velocidade média | domínio | Velocidade do robô | número real | >= 0 | — | PP: unidade m/s | — |
| Indicadores | distância percorrida | domínio | Deslocamento do robô | número real | >= 0 | — | PP: unidade m | — |
| Indicadores | taxa de quedas | domínio | Frequência de quedas | número real | >= 0 | — | PP: unidade e cálculo | — |
| Indicadores | estabilidade | domínio | Equilíbrio durante a execução | número real | Conforme unidade | — | PP: significado | — |
| Indicadores | gols marcados | domínio | Gols registrados no experimento | número inteiro | >= 0 | — | — | — |
| Comportamento | + visualização da simulação | aplicação | Comportamento registrado do robô | vídeo/animação | Associado à execução | — | PP: identificar execução | CE: informar indisponibilidade |
| Avaliação | + resultado | usuário | Melhora, não melhora ou falta de evidências | seleção simples | Uma classificação | — | PA: exigir seleção | RA: revisar |
| Avaliação | observação | usuário | Justificativa ou comentário da avaliação | texto | Opcional | — | PP: orientar preenchimento | RA: editar |
| Configuração | + parâmetro utilizado | domínio | Parâmetro de treinamento anterior | texto | — | — | PP: explicar termo | — |
| Configuração | valor do parâmetro | domínio | Valor registrado na execução | número/texto | Conforme parâmetro | — | PP: indicar ausência | CE: consultar arquivos |
| Configuração | condições de execução | domínio | Condições utilizadas no treinamento | texto | — | — | PP: identificar condições | CE: consultar responsável |
| Comparação | + execuções selecionadas | usuário | Dois treinamentos comparados lado a lado | seleção dupla | Exatamente duas | — | PA: exigir duas seleções | RA: alterar |
| Comparação | diferenças | aplicação | Variação entre métricas e parâmetros | lista | Dados disponíveis | — | PP: destacar diferenças | RA: consultar detalhes |
| Comparação | comparabilidade | usuário | Verifica se as condições permitem comparar | seleção simples | {comparável, não comparável, não confirmada} | não confirmada | AL: alertar limitações | CE: buscar informações |
| Referência | + baseline | usuário | Treinamento escolhido como referência | seleção simples | Execução existente | — | PP: explicar baseline | RA: trocar referência |
| Apresentação | + indicadores selecionados | usuário | Métricas escolhidas para reunião | seleção múltipla | Mínimo de um | — | PA: exigir seleção | RA: alterar |
| Apresentação | contexto | aplicação | Preserva período, execução e indicador | registro | — | Atual | PP: indicar retorno | RA: retornar à apresentação |
| Anotações | + anotação | usuário | Registro de problemas, conclusões e ajustes | texto | Não vazio | — | PA: impedir registro vazio | RA: corrigir |
| Anotações | tipo | usuário | Problema, investigação ou próximo ajuste | seleção simples | Opção válida | ponto a investigar | PP: explicar tipos | RA: alterar |
| Anotações | situação | usuário | Estado de investigação | seleção simples | {pendente, verificado} | pendente | PP: indicar estado | RA: atualizar |
| Planejamento | + próximo ajuste | usuário | Proposta de ajuste futuro | texto | Associada à análise | — | AL: evidências insuficientes | RA: revisar |


### Regras para os signos

- Use o vocabulário do domínio do usuário.
- Evite duplicar o mesmo conceito com nomes diferentes.
- Diferencie informação fornecida pelo usuário, produzida pelo sistema e derivada do domínio.
- Registre prevenção e recuperação apenas quando fizer sentido; explique as siglas usadas.

## Síntese

Quais objetivos/tópicos/signos deverão necessariamente aparecer nos diagramas MoLIC?

*Objetivos:* contemplar os objetivos O01 a O18, priorizando os fluxos principais de avaliação de desempenho (CI01), recuperação e comparação de treinamentos (CI02) e apresentação dos resultados em reunião (CI03).

*Tópicos:*
- *CI01:* Enviar treinamento, Avaliar desempenho, Consultar métricas, Observar comportamento, Comparar treinamentos, Consultar avaliações e Planejar ajustes.
- *CI02:* Recuperar treinamento, Consultar resultados, Recuperar configurações, Identificar dados ausentes, Comparar execuções e Avaliar referência.
- *CI03:* Preparar apresentação, Consultar visão geral, Analisar métricas, Observar execução, Registrar orientação e Planejar próximos passos.

*Signos:* arquivos do treinamento, identificação da execução, busca e filtros, indicadores de desempenho, visualização da simulação, resultado da avaliação, parâmetros utilizados, informações ausentes, execuções comparadas, comparabilidade, baseline, indicadores selecionados, contexto da apresentação, anotações e próximos ajustes.

Os diagramas também deverão representar caminhos alternativos, prevenção e recuperação de rupturas, como falhas no envio, buscas sem resultados, ausência de informações, comparações incompletas e erros de registro.

A configuração e a execução de novos treinamentos permanecem fora do escopo da interface, que se concentra na consulta, análise e comunicação dos resultados.


## Checklist

- [x] Cenários de interação mostram alterações em relação aos cenários de problema.
- [x] Cada solução individual identifica autor e cenário de origem.
- [x] Tópicos/falas/signos são coerentes com objetivos do usuário.
- [x] Mapas individuais foram consolidados.
- [x] O esquema de signos está em uma tabela única e sem duplicações conceituais.
- [x] Nomes de objetivos/signos serão reutilizados na Entrega 10.
- [x] Em TCC técnico, signos representam conceitos do domínio compreensíveis ao usuário, não apenas variáveis/estruturas internas.
- [x] Padrões como dashboard, relatório, filtros, administração e CRUD possuem objetivos e signos correspondentes.
- [x] A interface comunica não só o resultado técnico, mas também seu significado para a tarefa.
# Entrega 4  Cenários de análise/problema

**Data:** 05/10/2026
**Status:** 🟩 Concluído
**Responsabilidade:** 1 solução completa por integrante

## Objetivo da atividade

Descrever situações atuais em que o usuário tenta alcançar um objetivo e encontra dificuldades. O cenário de análise/problema deve tornar visível **o contexto, os atores, as ações e as rupturas**, sem antecipar a interface que será projetada.

> **Regra central:** cenário de problema é a “história do problema”. Se o texto já diz “o sistema mostra”, “o aplicativo resolve” ou descreve botões/telas futuras, provavelmente está misturando problema com solução.

Sempre que possível, o cenário deve aprofundar uma **situação concreta já registrada na Entrega 1**.

### Quando o TCC não possuía interface

O cenário continua sendo uma história de **problema/atividade humana**, não uma história do futuro sistema. Descreva como o profissional realiza hoje uma atividade semelhante ou como lida atualmente com dados, resultados, configurações, logs, decisões e limitações que o tema do TCC pretende apoiar.

Exemplo: em vez de “o DBA abre o novo dashboard e executa o algoritmo”, descreva “o DBA precisa investigar uma consulta lenta, reúne informações em ferramentas distintas, compara planos manualmente e tem dificuldade para estimar o impacto de uma mudança”.

A interface da disciplina aparecerá somente depois, nos cenários de interação.

Se o integrante escolher um novo problema/situação, explique por que ele passou a ser relevante e indique a evidência que motivou sua inclusão.

## Cenário C01  Análise de Performance do Robô

**Autor(a):** Letizia L. Baptistella
**Persona(s) relacionada(s):** Rafael Martins
**Necessidade relacionada:** Visualizar métricas de forma rápida, comparar diferentes treinamentos e versões, consultar histórico e relacionar métricas com o comportamento observado do robô.
**Situação concreta da Entrega 1 relacionada:** Interpretação incorreta dos resultados de treinamento; situação concreta em que a recompensa aumenta, mas o robô apresenta pouco deslocamento.
**Hipóteses ainda presentes:** H01 e H02

### 1. Cenário inicial

Rafael Martins, integrante técnico de uma equipe de robótica humanoide, está desenvolvendo e testando o comportamento do robô para uma partida de futebol. Após realizar um novo treinamento, ele precisa verificar se o resultado representa uma melhoria em relação aos experimentos anteriores e decidir quais ajustes devem ser realizados no próximo treinamento.

Durante o desenvolvimento, Rafael observa se o treinamento apresentou um resultado positivo a partir do comportamento do robô e das métricas obtidas. Nessa análise, ele verifica a velocidade média, a distância percorrida, a taxa de quedas, a estabilidade durante o movimento e a localização do robô. Ele realiza ajustes nos parâmetros da caminhada e observa uma melhora na velocidade. Apesar disso, o robô permanece menos tempo equilibrado, percorre uma distância maior, mas cai com frequência. O resultado, portanto, não representa necessariamente uma melhoria na capacidade de caminhar. Rafael precisa considerar diferentes informações antes de concluir se o treinamento foi bem-sucedido.

Para entender melhor o que aconteceu, Rafael compara as métricas e as configurações utilizadas anteriormente e ajusta os novos parâmetros com base nesses resultados. Essas informações estão associadas a diferentes execuções e observações, tornando a comparação dependente da consulta e organização dos resultados disponíveis.

A análise é realizada durante os ciclos de desenvolvimento do robô, em um computador utilizado para executar os treinamentos. Como novos treinamentos são realizados a partir dos resultados anteriores, uma interpretação incorreta pode levar Rafael e a equipe a escolher parâmetros inadequados para o próximo experimento, desperdiçando tempo computacional e prolongando os ciclos de desenvolvimento.

### 2. Questões de refinamento

Use os tipos de questões/taxonomia definidos na aula. As perguntas devem revelar informações **ainda ausentes** do cenário, não repetir o que já foi respondido.

| ID | Questão | O que ainda falta no cenário | Como investigar |
| --- | --- | --- | --- |
| Q1 | Quais informações Rafael precisa ter para decidir se o treinamento deve ser considerado uma melhoria em relação aos anteriores? | O cenário apresenta o objetivo de avaliar o treinamento, mas ainda não deixa claro quais informações são necessárias para essa decisão. | Entrevista com integrantes da equipe e observação de uma sessão de avaliação. |
| Q2 | Em que momento e em quais condições Rafael realiza essa análise dos resultados do treinamento? | O cenário informa que a análise ocorre durante os ciclos de desenvolvimento, mas não detalha quando e em quais condições ela acontece. | Observação do processo de treinamento e entrevista com Rafael e equipe. |
| Q3 | Quais características e conhecimentos de Rafael influenciam a forma como ele interpreta os resultados do treinamento? | O cenário identifica Rafael como integrante técnico, mas não especifica quais conhecimentos ou características são necessários para realizar a atividade. | Entrevista com Rafael e demais integrantes da equipe. |
| Q4 | Como Rafael decide quais resultados anteriores utilizar como referência e quais parâmetros modificar no próximo treinamento? | O cenário informa que ele compara resultados e ajusta parâmetros, mas não explica como essas decisões são planejadas. | Entrevista e observação de um ciclo real de treinamento. |
| Q5 | Como Rafael realiza atualmente a comparação entre as métricas e os parâmetros de diferentes treinamentos? | A comparação é uma ação central do cenário, mas ainda não foi detalhado como ela é executada na prática. | Observação da atividade e análise dos arquivos/registros utilizados pela equipe. |
| Q6 | O que faz Rafael perceber que precisa investigar os resultados de treinamentos anteriores? | O cenário apresenta uma diferença entre as métricas, mas não especifica qual acontecimento desencadeia a busca por outros resultados. | Observação de uma sessão de avaliação e entrevista com Rafael. |
| Q7 | Como Rafael determina, ao final da análise, se o treinamento foi bem-sucedido ou se é necessário realizar um novo ajuste? | O cenário mostra que ele precisa avaliar o treinamento, mas ainda não define como ele chega à conclusão sobre o resultado. | Entrevista com Rafael/equipe e análise de treinamentos anteriores. |


### 3. Cenário refinado

Rafael Martins, estudante e integrante técnico de uma equipe de robótica humanoide, está desenvolvendo e testando o comportamento de caminhada do robô para partidas de futebol.

Durante o desenvolvimento, Rafael observa se o treinamento apresentou um resultado positivo a partir do comportamento do robô e das métricas obtidas. Nessa análise, ele verifica a velocidade média, a distância percorrida, a taxa de quedas, a estabilidade durante o movimento e a localização do robô.

**[NOVO: Rafael utiliza essas informações em conjunto para decidir se o treinamento representa uma melhoria, pois uma melhora isolada em uma métrica não é suficiente para considerar o resultado positivo.] [Q1]**

**[NOVO: Essa análise é realizada após a execução de cada treinamento, durante os ciclos de desenvolvimento e ajuste do comportamento de caminhada do robô.] [Q2]**

**[NOVO: Por possuir conhecimento sobre o funcionamento da caminhada e sobre os parâmetros utilizados no treinamento, Rafael consegue relacionar as alterações realizadas com as mudanças observadas nas métricas e no comportamento do robô.] [Q3]**

Ele realiza ajustes nos parâmetros da caminhada e observa uma melhora na velocidade. Apesar disso, o robô permanece menos tempo equilibrado, percorre uma distância maior, mas cai com frequência. O resultado, portanto, não representa necessariamente uma melhoria na capacidade de caminhar. Rafael precisa considerar diferentes informações antes de concluir se o treinamento foi bem-sucedido.

Para entender melhor o que aconteceu, Rafael compara as métricas e as configurações utilizadas anteriormente e ajusta os novos parâmetros com base nesses resultados.

**[NOVO: Rafael utiliza como referência treinamentos anteriores que apresentem características semelhantes às da execução atual e utiliza as diferenças observadas para decidir quais parâmetros devem ser modificados.] [Q4]**

**[NOVO: Para realizar a comparação, Rafael consulta os resultados e as configurações das diferentes execuções e relaciona os valores das métricas aos parâmetros utilizados em cada treinamento.] [Q5]**

**[NOVO: A necessidade de investigar treinamentos anteriores surge quando Rafael identifica que uma métrica apresentou melhora, mas outras indicam piora no comportamento do robô, como o aumento da frequência de quedas.] [Q6]**

Essas informações estão associadas a diferentes execuções e observações, tornando a comparação dependente da consulta e organização dos resultados disponíveis.

**[NOVO: Ao final da análise, Rafael considera o conjunto das métricas e o comportamento observado para decidir se mantém os parâmetros utilizados ou realiza novos ajustes no próximo treinamento.] [Q7]**

A análise é realizada durante os ciclos de desenvolvimento do robô, em um computador utilizado para executar os treinamentos. Como novos treinamentos são realizados a partir dos resultados anteriores, uma interpretação incorreta pode levar Rafael e a equipe a escolher parâmetros inadequados para o próximo experimento, desperdiçando tempo computacional e prolongando os ciclos de desenvolvimento.

### 4. Elementos extraídos

| Elemento | Descrição |
| --- | --- |
| Ator(es) | Rafael Martins (integrante de desenvolvimento do time de robótica humanoide) |
| Objetivo(s) | Avaliar se o treinamento apresentou uma melhoria no comportamento do robô, comparar o resultado com treinamentos anteriores e definir quais ajustes realizar no próximo treinamento. |
| Contexto | Rafael está desenvolvendo e testando o comportamento de um robô humanoide para uma partida de futebol, realizando ciclos de treinamento e ajustes em um computador. |
| Recursos/informações | Velocidade média, distância percorrida, taxa de quedas, estabilidade durante o movimento, localização do robô, parâmetros da caminhada, configurações e resultados de treinamentos anteriores. |
| Ações | Executar um treinamento; observar o comportamento do robô; analisar as métricas; ajustar os parâmetros da caminhada; comparar métricas e configurações com treinamentos anteriores; consultar resultados anteriores; definir novos parâmetros para o próximo treinamento. |
| Problemas/rupturas | A melhora em uma métrica, como a velocidade, pode ocorrer junto à piora de outras características, como estabilidade e frequência de quedas. Além disso, as informações de diferentes treinamentos precisam ser consultadas e relacionadas para permitir uma comparação. |
| Consequências | Rafael pode interpretar incorretamente o resultado do treinamento e escolher parâmetros inadequados para a próxima execução, gerando novos treinamentos desnecessários, desperdício de tempo computacional e prolongamento do desenvolvimento. |


### 5. Implicações para as próximas entregas

A partir do cenário analisado, as próximas entregas devem aprofundar como Rafael realiza a avaliação dos treinamentos e a comparação entre diferentes execuções. É necessário compreender quais métricas são utilizadas, como ele relaciona essas métricas ao comportamento observado do robô e como interpreta situações em que alguns resultados melhoram enquanto outros pioram. Também deve ser investigado como os resultados e parâmetros dos treinamentos anteriores são registrados, consultados e utilizados como referência para definir novos ajustes. Além disso, é importante identificar quais informações Rafael considera necessárias para comparar diferentes treinamentos e quais critérios utiliza para determinar se um treinamento foi bem-sucedido ou se um novo ciclo de ajustes é necessário.

---
## Cenário C02 — Recuperação da configuração de um treinamento anterior

**Autor(a):** Manuella Filipe Peres  
**Persona(s) relacionada(s):** P02 — Marina Oliveira  
**Necessidade relacionada:** Consultar resultados de experimentos anteriores, compreender as métricas de desempenho, recuperar informações sobre as configurações utilizadas e relacionar alterações nos parâmetros ao comportamento observado do robô.

**Situação concreta da Entrega 1 relacionada:** O histórico dos experimentos e das configurações é registrado manualmente pela equipe e não fica centralizado, o que dificulta identificar configurações anteriores e comparar diferentes execuções. Também foi apontado o risco de comparar testes realizados em condições diferentes.

**Hipóteses ainda presentes:** H01 e H02. As características e necessidades específicas da persona P02 também permanecem sujeitas à validação.

### 1. Cenário inicial

Marina Oliveira, pesquisadora de robótica, está investigando diferentes estratégias utilizadas para melhorar a caminhada de um robô humanoide em simulação. Durante sua pesquisa, ela analisa resultados de treinamentos anteriores para compreender como as alterações nos parâmetros influenciam o comportamento do robô e identificar experimentos que possam servir de referência para novas investigações.

Após consultar resultados recentes que não apresentaram melhorias significativas, Marina se lembra de um treinamento realizado algumas semanas antes, no qual o robô percorreu uma distância maior e apresentou menor frequência de quedas. Ela decide investigar esse experimento para compreender quais configurações contribuíram para o resultado obtido.

Para isso, Marina precisa identificar os parâmetros utilizados naquela execução. Entretanto, os parâmetros são configurados diretamente no código antes dos treinamentos, e diferentes alterações foram realizadas desde então. Ao consultar a pasta do experimento, ela encontra o modelo salvo e algumas anotações da equipe, mas essas informações não reúnem todos os valores utilizados na configuração original.

Marina procura relacionar os resultados do treinamento anterior aos das execuções recentes, mas encontra dificuldades para confirmar se os experimentos foram realizados nas mesmas condições. Sem essa confirmação, não consegue determinar com segurança quais alterações podem ter influenciado as diferenças observadas no desempenho do robô.

Essa situação dificulta a interpretação dos resultados e pode comprometer a escolha de experimentos anteriores como referência para novas investigações.

### 2. Questões de refinamento

| ID | Questão | O que ainda falta no cenário | Como investigar |
|---|---|---|---|
| Q1 | Como Marina identifica qual treinamento anterior apresentou os resultados mais relevantes para sua investigação? | O cenário informa que ela se lembra de um treinamento, mas não explica como localiza a execução correspondente entre os registros disponíveis. | Entrevista com integrantes da equipe e análise das pastas e registros dos treinamentos. |
| Q2 | Quais informações sobre os treinamentos são registradas nas anotações da equipe? | O cenário informa que os registros estão incompletos, mas não especifica quais informações estão disponíveis e quais precisam ser recuperadas. | Análise das anotações existentes e comparação com os parâmetros utilizados nos treinamentos. |
| Q3 | Como Marina verifica se diferentes treinamentos foram realizados em condições comparáveis? | O cenário apresenta a dificuldade de comparação, mas não descreve quais informações precisam ser verificadas para confirmar a equivalência das condições. | Observação de uma atividade de análise e entrevista com integrantes responsáveis pelos treinamentos. |
| Q4 | Quem registra as informações dos experimentos e quem realiza alterações nos parâmetros ao longo do desenvolvimento? | O cenário não esclarece como as responsabilidades relacionadas ao registro e à configuração dos treinamentos são distribuídas entre os integrantes da equipe. | Entrevista com a equipe sobre a organização e a divisão das atividades. |
| Q5 | O que Marina faz quando não consegue confirmar as configurações utilizadas em um treinamento anterior? | O cenário apresenta a dificuldade, mas não esclarece como essa limitação influencia a continuidade da investigação. | Entrevista com pesquisadores e integrantes da equipe e análise de situações anteriores. |
| Q6 | Como a necessidade de recuperar informações de diferentes registros interfere no processo de análise dos resultados? | O cenário não detalha as consequências da recuperação manual das configurações para o tempo e a continuidade da investigação. | Observação do processo de consulta aos registros e levantamento das dificuldades relatadas pelos integrantes. |

### 3. Cenário refinado

Marina Oliveira, pesquisadora de robótica, está investigando diferentes estratégias utilizadas para melhorar a caminhada de um robô humanoide em simulação. Durante sua pesquisa, ela analisa resultados de treinamentos anteriores para compreender como as alterações nos parâmetros influenciam o comportamento do robô e identificar experimentos que possam servir de referência para novas investigações.

Após consultar resultados recentes que não apresentaram melhorias significativas, Marina se lembra de um treinamento realizado algumas semanas antes, no qual o robô percorreu uma distância maior e apresentou menor frequência de quedas. Ela decide investigar esse experimento para compreender quais configurações contribuíram para o resultado obtido.

**[NOVO: Para localizar o treinamento, Marina consulta as pastas das execuções e examina os arquivos de métricas disponíveis, procurando identificar aquele que apresenta os resultados de desempenho que deseja investigar.] [Q1]**

Para isso, Marina precisa identificar os parâmetros utilizados naquela execução. Entretanto, os parâmetros são configurados diretamente no código antes dos treinamentos, e diferentes alterações foram realizadas desde então. Ao consultar a pasta do experimento, ela encontra o modelo salvo e algumas anotações da equipe, mas essas informações não reúnem todos os valores utilizados na configuração original.

**[NOVO: As anotações disponíveis registram as principais alterações realizadas e observações sobre os experimentos, mas nem sempre apresentam todos os parâmetros utilizados. Informações adicionais precisam ser consultadas nos arquivos de configuração e no histórico do código.] [Q2]**

**[NOVO: Como o desenvolvimento dos treinamentos envolve diferentes integrantes da equipe, Marina também precisa identificar quais alterações foram realizadas em cada execução e quais registros estão associados ao experimento investigado.] [Q4]**

Marina procura relacionar os resultados do treinamento anterior aos das execuções recentes, mas encontra dificuldades para confirmar se os experimentos foram realizados nas mesmas condições.

**[NOVO: Para verificar se os resultados podem ser comparados, Marina consulta as informações disponíveis sobre os parâmetros, as configurações e as condições de execução dos treinamentos. Quando os registros não são suficientes, ela precisa buscar esclarecimentos com os integrantes responsáveis pelos experimentos.] [Q3]**

**[NOVO: A necessidade de consultar diferentes arquivos, registros e integrantes da equipe interrompe a análise dos resultados e exige atividades adicionais de recuperação e organização das informações antes que a comparação possa ser concluída.] [Q6]**

**[NOVO: Quando não consegue confirmar as configurações utilizadas, Marina precisa reconhecer as limitações da comparação e avaliar, junto à equipe, se o experimento pode ser utilizado como referência ou se será necessário obter informações adicionais ou realizar uma nova execução.] [Q5]**

Sem essa confirmação, Marina não consegue determinar com segurança quais alterações podem ter influenciado as diferenças observadas no desempenho do robô.

Essa situação dificulta a interpretação dos resultados, compromete a utilização de experimentos anteriores como referência e pode levar à repetição de análises ou treinamentos para recuperar informações necessárias à pesquisa.

### 4. Elementos extraídos

| Elemento | Descrição |
|---|---|
| **Ator(es)** | Marina Oliveira (pesquisadora de robótica) e integrantes da equipe responsáveis pelos treinamentos, registros e alterações dos parâmetros. |
| **Objetivo(s)** | Recuperar informações sobre um treinamento anterior, compreender as configurações utilizadas, comparar resultados de diferentes experimentos e identificar condições que possam explicar as diferenças observadas no comportamento do robô. |
| **Contexto** | Pesquisa sobre locomoção de robôs humanoides em simulação, envolvendo diferentes ciclos de treinamento, alterações nos parâmetros e análise de resultados registrados em arquivos e anotações da equipe. |
| **Recursos/informações** | Pastas das execuções, modelos salvos, arquivos de métricas, anotações da equipe, histórico de versões do código, parâmetros de treinamento, configurações anteriores e informações sobre as condições dos experimentos. |
| **Ações** | Consultar resultados anteriores; localizar um treinamento de referência; examinar arquivos de métricas; consultar anotações e configurações; investigar alterações realizadas no código; buscar esclarecimentos com integrantes da equipe; comparar as condições dos experimentos; avaliar a confiabilidade das informações disponíveis. |
| **Problemas/rupturas** | Informações incompletas ou distribuídas entre diferentes registros; dificuldade para identificar os parâmetros utilizados em execuções anteriores; necessidade de consultar diferentes fontes; impossibilidade de confirmar se os treinamentos foram realizados nas mesmas condições. |
| **Consequências** | Dificuldade para interpretar diferenças de desempenho, aumento do esforço necessário para recuperar informações, risco de realizar comparações inadequadas, necessidade de repetir análises ou experimentos e comprometimento da reprodutibilidade dos resultados. |

### 5. Implicações para as próximas entregas

A partir do cenário analisado, as próximas entregas devem aprofundar como os integrantes da equipe registram, organizam e recuperam as informações relacionadas aos treinamentos realizados.

É necessário compreender quais parâmetros e configurações são considerados essenciais para interpretar os resultados dos experimentos e quais informações precisam estar disponíveis para que diferentes execuções possam ser comparadas de maneira confiável.

Também deve ser investigado como pesquisadores e integrantes da equipe identificam treinamentos anteriores relevantes, consultam as alterações realizadas entre execuções e verificam se os experimentos foram conduzidos em condições comparáveis.

Na modelagem de tarefas, a localização de um treinamento de referência, a recuperação de suas configurações e a comparação dos resultados devem ser tratadas como atividades relacionadas, mas distintas, pois apresentam objetivos, recursos e dificuldades específicos.

Além disso, deve ser avaliado como a ausência de informações completas influencia a continuidade da pesquisa, incluindo possíveis atrasos, repetição de análises e necessidade de novos treinamentos.

As hipóteses H01 e H02 permanecem presentes, uma vez que as necessidades de organização, recuperação e comparação dos resultados ainda precisam ser verificadas com outros usuários. As características específicas da persona Marina Oliveira também devem ser validadas com pesquisadores que desempenhem atividades semelhantes.

## Cenário C03 — Avaliação de treinamentos em reunião de orientação

**Autor(a):** Rafaela Altheman de Campos  
**Persona(s) relacionada(s):** P03 — Carlos Almeida  
**Necessidade relacionada:** Obter uma visão consolidada do desempenho do robô, comparar resultados importantes e compreender rapidamente quais aspectos evoluíram ou pioraram, de modo a orientar as decisões técnicas da equipe.

**Situação concreta da Entrega 1 relacionada:** Situação em que a recompensa aumenta, mas o robô permanece equilibrado e quase não se desloca. Também foi registrado que professores e orientadores acompanham os resultados e participam das decisões técnicas do projeto.

**Hipóteses ainda presentes:** H01 e H02. As características e necessidades específicas da persona P03 permanecem sujeitas à validação.

### 1. Cenário inicial

Carlos Almeida, professor e orientador de uma equipe universitária de robótica humanoide, acompanha o desenvolvimento da caminhada de um robô projetado para jogar futebol. Como não participa diretamente de todos os treinamentos, utiliza as reuniões com os estudantes para compreender os resultados obtidos e orientar as próximas etapas do desenvolvimento.

Durante uma reunião de acompanhamento, uma estudante apresenta os resultados de um treinamento recente. O gráfico da recompensa indica um aumento em relação à execução anterior, sugerindo inicialmente uma possível melhoria. Entretanto, Carlos precisa compreender se essa evolução numérica corresponde a um avanço real no comportamento do robô.

Para isso, pergunta qual foi a distância percorrida, quantas quedas ocorreram e quais alterações foram realizadas em comparação ao treinamento anterior. A estudante não incluiu todas essas informações na apresentação e precisa consultar os arquivos de métricas, as anotações da equipe e a visualização do modelo no simulador.

Ao observar o comportamento do robô, Carlos percebe que ele permanece equilibrado durante parte da execução, mas apresenta pouco deslocamento. Dessa forma, o aumento da recompensa não representa necessariamente uma melhoria na capacidade de caminhar.

Como algumas informações precisam ser recuperadas e comparadas durante a reunião, a equipe encontra dificuldades para concluir a avaliação no tempo disponível. A ausência de uma comparação completa pode levar ao adiamento da decisão sobre os próximos ajustes, interferindo no planejamento dos experimentos.

### 2. Questões de refinamento

| ID | Questão | O que ainda falta no cenário | Como investigar |
|---|---|---|---|
| Q1 | Com que frequência e de que forma os resultados dos treinamentos são apresentados a Carlos? | O cenário menciona uma reunião de acompanhamento, mas não detalha como os estudantes preparam e organizam os resultados para apresentação. | Entrevista com professores, orientadores e estudantes, além da observação de reuniões de acompanhamento. |
| Q2 | Quais informações Carlos considera necessárias para avaliar se um treinamento apresentou melhoria? | O cenário apresenta perguntas sobre deslocamento e quedas, mas não esclarece todos os critérios utilizados para interpretar o desempenho. | Entrevista com orientadores e análise de avaliações anteriores realizadas pela equipe. |
| Q3 | Por que as informações solicitadas por Carlos não estavam disponíveis na apresentação? | O cenário mostra que a estudante precisa consultar outros registros, mas não explica como as informações são selecionadas e organizadas antes da reunião. | Observação da preparação das apresentações e entrevista com integrantes da equipe. |
| Q4 | O que leva Carlos a questionar um resultado aparentemente positivo? | O cenário apresenta a diferença entre recompensa e comportamento, mas não detalha como o orientador identifica a necessidade de uma análise adicional. | Entrevista com professores e orientadores sobre a interpretação das métricas. |
| Q5 | Como as decisões e orientações discutidas nas reuniões são registradas e utilizadas posteriormente? | O cenário não esclarece como a equipe documenta as conclusões e recupera as decisões tomadas. | Análise dos registros de acompanhamento do projeto e entrevista com os integrantes da equipe. |
| Q6 | Quais consequências o adiamento de uma decisão pode provocar no planejamento dos próximos treinamentos? | O cenário menciona possíveis dificuldades no planejamento, mas não detalha como o adiamento interfere nas atividades da equipe. | Entrevista com integrantes da equipe e análise do planejamento dos experimentos. |

### 3. Cenário refinado

Carlos Almeida, professor e orientador de uma equipe universitária de robótica humanoide, acompanha o desenvolvimento da caminhada de um robô projetado para jogar futebol. Como não participa diretamente de todos os treinamentos, utiliza as reuniões com os estudantes para compreender os resultados obtidos e orientar as próximas etapas do desenvolvimento.

**[NOVO: As reuniões de acompanhamento representam momentos em que os estudantes apresentam resultados selecionados dos treinamentos realizados. Como o tempo disponível para discussão é limitado, Carlos precisa compreender as informações mais relevantes sem necessariamente consultar todos os detalhes de cada execução. A frequência das reuniões e os formatos de apresentação ainda precisam ser confirmados com os participantes.] [Q1]**

Durante uma reunião de acompanhamento, uma estudante apresenta os resultados de um treinamento recente. O gráfico da recompensa indica um aumento em relação à execução anterior, sugerindo inicialmente uma possível melhoria.

Entretanto, Carlos precisa compreender se essa evolução numérica corresponde a um avanço real no comportamento do robô.

**[NOVO: Para avaliar o treinamento, Carlos considera importante relacionar a recompensa obtida a outros indicadores, como distância percorrida, velocidade, estabilidade e frequência de quedas, além de observar o comportamento do robô durante a simulação.] [Q2]**

**[NOVO: O aumento da recompensa, quando apresentado isoladamente, leva Carlos a solicitar outras informações, pois esse indicador não permite concluir, por si só, que houve melhoria na locomoção. Um robô pode obter uma recompensa elevada sem apresentar deslocamento satisfatório.] [Q4]**

Para isso, pergunta qual foi a distância percorrida, quantas quedas ocorreram e quais alterações foram realizadas em comparação ao treinamento anterior.

A estudante não incluiu todas essas informações na apresentação e precisa consultar os arquivos de métricas, as anotações da equipe e a visualização do modelo no simulador.

**[NOVO: A apresentação foi preparada com foco no gráfico da recompensa, sem reunir previamente todos os indicadores necessários à comparação. Embora a equipe possua registros dos treinamentos, a necessidade de consultar diferentes informações durante a reunião dificulta a análise conjunta dos resultados.] [Q3]**

Ao observar o comportamento do robô, Carlos percebe que ele permanece equilibrado durante parte da execução, mas apresenta pouco deslocamento. Dessa forma, o aumento da recompensa não representa necessariamente uma melhoria na capacidade de caminhar.

Como algumas informações precisam ser recuperadas e comparadas durante a reunião, a equipe encontra dificuldades para concluir a avaliação no tempo disponível.

**[NOVO: As conclusões discutidas durante o acompanhamento precisam ser registradas para orientar as atividades posteriores da equipe. Os estudantes podem utilizar as anotações compartilhadas do projeto para documentar os problemas identificados, os pontos que exigem investigação e os próximos ajustes propostos. A forma efetiva desse registro deverá ser verificada com a equipe.] [Q5]**

**[NOVO: Quando a avaliação não pode ser concluída, a definição dos próximos ajustes pode depender de uma análise complementar. Isso pode exigir novas consultas aos resultados e interferir no planejamento dos experimentos seguintes, especialmente quando a equipe precisa decidir quais parâmetros serão modificados antes de iniciar outro treinamento.] [Q6]**

A ausência de uma comparação completa pode levar ao adiamento da decisão sobre os próximos ajustes, interferindo no planejamento dos experimentos.

Essa situação evidencia a importância de compreender como os resultados são preparados, apresentados, comparados e discutidos durante o acompanhamento do desenvolvimento do robô, principalmente quando diferentes métricas indicam conclusões distintas sobre o desempenho obtido.

### 4. Elementos extraídos

| Elemento | Descrição |
|---|---|
| **Ator(es)** | Carlos Almeida (professor e orientador), estudante responsável pela apresentação e demais integrantes da equipe de robótica humanoide. |
| **Objetivo(s)** | Avaliar se o treinamento recente representa uma melhoria real na caminhada do robô, compreender as diferenças em relação às execuções anteriores e orientar a decisão sobre os próximos experimentos. |
| **Contexto** | Reunião de acompanhamento de um projeto universitário de robótica humanoide, na qual estudantes apresentam resultados de treinamentos e discutem com o orientador possíveis ajustes e melhorias. |
| **Recursos/informações** | Gráficos de recompensa, distância percorrida, velocidade, frequência de quedas, estabilidade, arquivos de métricas, resultados anteriores, parâmetros de treinamento, anotações da equipe e visualização do comportamento do robô no simulador. |
| **Ações** | Apresentar os resultados; analisar métricas; questionar diferenças entre os treinamentos; consultar registros; observar o comportamento do robô; comparar resultados; discutir possíveis ajustes; registrar conclusões e orientar próximos experimentos. |
| **Problemas/rupturas** | Recompensa elevada sem melhoria correspondente na locomoção; ausência de métricas importantes na apresentação; necessidade de recuperar informações durante a reunião; dificuldade para concluir comparações no tempo disponível. |
| **Consequências** | Risco de interpretar incorretamente os resultados, dificuldade para justificar decisões técnicas, necessidade de análises complementares, possível adiamento das decisões e impacto no planejamento dos próximos treinamentos. |

### 5. Implicações para as próximas entregas

A partir do cenário analisado, as próximas entregas devem aprofundar como os resultados dos treinamentos são organizados e apresentados aos professores e orientadores durante as reuniões de acompanhamento.

É necessário compreender quais métricas são consideradas essenciais para avaliar a evolução do comportamento do robô e como os orientadores relacionam os indicadores quantitativos às observações realizadas no simulador.

Também deve ser investigado como os estudantes selecionam as informações que serão apresentadas, quais dificuldades encontram ao recuperar resultados anteriores e como as comparações entre diferentes experimentos influenciam as discussões técnicas.

Na modelagem de tarefas, a avaliação realizada durante uma reunião deve ser tratada como uma atividade distinta da análise individual de resultados apresentada no cenário C01. Enquanto a análise individual envolve a investigação detalhada das métricas e dos parâmetros de treinamento, a avaliação coletiva exige a comunicação dos resultados, a interpretação compartilhada das informações e a definição de próximos passos em conjunto.

Além disso, as próximas etapas devem investigar como as decisões e orientações são registradas e utilizadas posteriormente, verificando se a ausência de informações completas pode provocar atrasos ou dificultar o planejamento de novos experimentos.

As hipóteses H01 e H02 permanecem presentes, pois a necessidade de organizar, comparar e apresentar resultados de maneira mais eficiente ainda precisa ser validada diretamente com os usuários.

Como Carlos Almeida permanece parcialmente caracterizado como proto-persona, suas necessidades, comportamentos e critérios de avaliação deverão ser verificados com professores e orientadores que desempenhem atividades semelhantes.

## Checklist

- [x] Há um cenário completo por integrante.
- [x] Cada cenário tem título, ator, objetivo, contexto e problema.
- [x] O cenário possui origem rastreável na Entrega 1 ou justifica claramente a inclusão de uma nova situação.
- [x] O texto descreve a situação atual, sem antecipar a solução.
- [x] Para TCC sem interface original, o cenário descreve uma prática humana plausível relacionada à contribuição técnica, e não "a falta de uma tela".
- [x] Questões de refinamento acrescentam informação nova.
- [x] O refinamento mostra claramente o que foi adicionado/alterado.
- [x] Cenários são diferentes o suficiente para cobrir objetivos/problemas relevantes.
- [x] Cada cenário está ligado a persona/necessidade na matriz de rastreabilidade.

# Entrega 4  Cenários de análise/problema

**Data:** 16/09/2026
**Status:** 🟧 Em andamento
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

Rafael Martins, integrante técnico de uma equipe de robótica humanoide, está desenvolvendo e testando o comportamento do robô para uma partida de futebol. Após realizar um novo treinamento, ele precisa verificar se o resultado representa uma melhoria em relação aos experimentos anteriores e decidir quais ajustes devem ser realizados no próximo treinamento.

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
## Cenário C02 - Recuperação da configuração de um treinamento anterior

**Autor(a):** Manuella Filipe Peres
**Persona(s) relacionada(s):** Marina Oliveira
**Necessidade relacionada:** Acessar rapidamente os resultados dos treinamentos, comparar diferentes experimentos e consultar os parâmetros utilizados em cada execução.
**Situação concreta da Entrega 1 relacionada:** O histórico dos experimentos e das configurações é registrado manualmente pela equipe e não fica centralizado, o que dificulta saber o que já foi tentado e comparar diferentes execuções. Também foi apontado o risco de comparar testes realizados em condições diferentes.
**Hipóteses ainda presentes:** H01 e H02

### 1. Cenário inicial

Marina Oliveira, pesquisadora de robótica, está estudando diferentes estratégias para melhorar a caminhada do robô humanoide em simulação. Depois de algumas execuções recentes sem melhora, ela se lembra de um treinamento feito algumas semanas antes em que o robô percorria uma distância maior e caía menos. Ela decide usar esse treinamento como ponto de partida e alterar apenas o peso de um termo da função de recompensa.

Para isso, Marina precisa saber exatamente quais parâmetros foram utilizados naquele treinamento. Os parâmetros são configurados diretamente no código antes de cada execução, e o código foi alterado várias vezes desde então. Ela encontra a pasta com o melhor modelo salvo daquela execução e as anotações feitas pela equipe, mas as anotações não reúnem todos os valores que estavam configurados no código naquele momento.

Marina compara as métricas desse treinamento com as das execuções recentes, mas não tem certeza de que todas foram realizadas nas mesmas condições. Se ela iniciar um novo treinamento a partir de uma configuração reconstruída de forma errada, o experimento, que pode levar de 10 a 48 horas, será feito sobre uma base diferente da que ela imagina, e a comparação com os resultados antigos deixa de ser válida.

### 2. Questões de refinamento

| ID | Questão | O que ainda falta no cenário | Como investigar |
| --- | --- | --- | --- |
| Q1 | Como Marina identifica qual treinamento anterior apresentou o melhor resultado? | O cenário informa que ela se lembra do treinamento, mas não explica como encontra essa execução entre as demais. | Entrevista com integrantes da equipe e análise das pastas e anotações dos treinamentos. |
| Q2 | Quais informações sobre o treinamento são registradas nas anotações? | O cenário informa que as anotações não reúnem todos os valores, mas não detalha o que é registrado. | Análise das anotações existentes comparadas com os parâmetros que influenciam o treinamento. |
| Q3 | Como Marina verifica se dois treinamentos foram realizados nas mesmas condições? | O cenário apresenta a dúvida, mas não descreve o que ela confere para resolvê-la. | Observação de uma comparação real e entrevista com Marina. |
| Q4 | Quem registra e quem altera os parâmetros ao longo do tempo? | O cenário não informa se o código e as anotações são mantidos por uma ou por várias pessoas. | Entrevista com a equipe sobre a divisão do trabalho. |
| Q5 | O que Marina faz quando não consegue reconstruir a configuração com segurança? | O cenário apresenta o risco, mas não mostra qual decisão ela toma diante dele. | Entrevista com Marina e relato de situações anteriores. |
| Q6 | Quanto tempo a reconstrução da configuração leva em relação à análise dos resultados? | O custo da atividade atual ainda não aparece no cenário. | Observação de uma reconstrução real, registrando o tempo gasto. |

### 3. Cenário refinado

Marina Oliveira, pesquisadora de robótica, está estudando diferentes estratégias para melhorar a caminhada do robô humanoide em simulação. Depois de algumas execuções recentes sem melhora, ela se lembra de um treinamento feito algumas semanas antes em que o robô percorria uma distância maior e caía menos. Ela decide usar esse treinamento como ponto de partida e alterar apenas o peso de um termo da função de recompensa.

**[NOVO: Para encontrar esse treinamento, Marina procura entre as pastas das execuções e abre os arquivos de métricas de algumas delas até encontrar a que corresponde ao que ela lembrava.] [Q1]**

Para isso, Marina precisa saber exatamente quais parâmetros foram utilizados naquele treinamento. Os parâmetros são configurados diretamente no código antes de cada execução, e o código foi alterado várias vezes desde então. Ela encontra a pasta com o melhor modelo salvo daquela execução e as anotações feitas pela equipe, mas as anotações não reúnem todos os valores que estavam configurados no código naquele momento.

**[NOVO: As anotações registram a mudança principal de cada experimento e todas as observações. Os demais valores configurados no código, como a quantidade de timesteps, precisam ser recuperados a partir do próprio código.] [Q2]**

**[NOVO: O código e as anotações são alterados por mais de uma integrante da equipe.] [Q4]**

Marina compara as métricas desse treinamento com as das execuções recentes, mas não tem certeza de que todas foram realizadas nas mesmas condições.

**[NOVO: Para verificar, ela consulta o histórico de versões do código e compara os arquivos de configuração da época do treinamento com os atuais. Mesmo assim, nem sempre consegue confirmar quais valores estavam sendo usados no momento exato da execução.] [Q3]**

**[NOVO: Essa reconstrução da configuração leva mais tempo do que a própria análise das métricas.] [Q6]**

**[NOVO: Quando não consegue confirmar todos os valores, Marina precisa escolher entre repetir o treinamento antigo para ter uma referência confiável, gastando um ciclo inteiro de treinamento, ou continuar com a configuração reconstruída sabendo que a comparação pode não ser válida.] [Q5]**

Se ela iniciar um novo treinamento a partir de uma configuração reconstruída de forma errada, o experimento, que pode levar de 10 a 48 horas, será feito sobre uma base diferente da que ela imagina, e a comparação com os resultados antigos deixa de ser válida.

### 4. Elementos extraídos

| Elemento | Descrição |
| --- | --- |
| Ator(es) | Marina Oliveira (pesquisadora de robótica) e demais integrantes que alteram o código e as anotações. |
| Objetivo(s) | Utilizar um treinamento anterior com bom desempenho como ponto de partida e garantir que a comparação com os novos resultados seja válida. |
| Contexto | Pesquisa sobre locomoção bípede com aprendizado por reforço em simulação, com treinamentos que levam de 10 a 48 horas, parâmetros configurados no código e histórico registrado manualmente pela equipe. |
| Recursos/informações | Pastas das execuções, melhor modelo salvo, arquivos de métricas, anotações da equipe, histórico de versões do código, parâmetros da função de recompensa e demais valores configurados no código. |
| Ações | Localizar o treinamento de referência; abrir os arquivos de métricas; consultar as anotações; consultar o histórico de versões do código; reconstruir a configuração; decidir se repete o treinamento antigo ou continua com a configuração reconstruída. |
| Problemas/rupturas | As anotações não reúnem todos os valores configurados no código; a configuração precisa ser reconstruída a partir do histórico de versões; nem sempre é possível confirmar a configuração usada no momento da execução; não é possível garantir que os treinamentos comparados foram realizados nas mesmas condições. |
| Consequências | Comparações que podem não ser válidas, um ciclo de treinamento gasto para recuperar uma referência, tempo perdido reconstruindo configurações e perda da reprodutibilidade dos experimentos. |

### 5. Implicações para as próximas entregas

As próximas entregas devem investigar como a equipe registra atualmente as configurações de cada treinamento e quais informações precisam ser recuperadas a partir do código. Também é necessário entender o que Marina considera como "mesmas condições" para que dois treinamentos possam ser comparados e com que frequência a dúvida sobre a configuração atrasa ou impede uma comparação. Na modelagem de tarefas, localizar um treinamento de referência e confirmar sua configuração deve ser tratado como uma tarefa separada da comparação das métricas, pois envolve informações e dificuldades diferentes. As hipóteses H01 e H02 continuam presentes, já que a evidência atual vem da experiência da própria equipe e ainda precisa ser verificada com outros integrantes e equipes.

## Checklist

- [ ] Há um cenário completo por integrante.
- [ ] Cada cenário tem título, ator, objetivo, contexto e problema.
- [ ] O cenário possui origem rastreável na Entrega 1 ou justifica claramente a inclusão de uma nova situação.
- [ ] O texto descreve a situação atual, sem antecipar a solução.
- [ ] Para TCC sem interface original, o cenário descreve uma prática humana plausível relacionada à contribuição técnica, e não “a falta de uma tela”.
- [ ] Questões de refinamento acrescentam informação nova.
- [ ] O refinamento mostra claramente o que foi adicionado/alterado.
- [ ] Cenários são diferentes o suficiente para cobrir objetivos/problemas relevantes.
- [ ] Cada cenário está ligado a persona/necessidade na matriz de rastreabilidade.

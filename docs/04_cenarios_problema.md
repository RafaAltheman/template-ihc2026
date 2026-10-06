# Entrega 4 — Cenários de análise/problema

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

## Cenário C01 — Análise de Performance do Robô

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

> Repita para C02, C03... com autoria individual.

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

# Entrega 9 — Modelo conceitual e design centrado na comunicação

**Data:** 06/11/2026
**Status:** ⬜ Em Desenvolvimento
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

## 1. Cenários de interação

Para cada cenário de problema, produza uma versão em que a solução já pode ser descrita. **Destaque claramente o texto alterado** em relação ao cenário original.

### CI01 — Análise do desempenho do robô

**Autor(a):** Letizia Lowatzki Baptistella --- 22.125.063-2
**Origem:** cenário problema C01 --- Análise de Performance do Robô

Rafael Martins, estudante e integrante técnico de uma equipe de robótica humanoide, está desenvolvendo e testando o comportamento de caminhada do robô para partidas de futebol. Após realizar um novo treinamento, ele precisa verificar se o resultado representa uma melhoria em relação aos experimentos anteriores e decidir quais ajustes devem ser realizados no próximo treinamento.
Durante o desenvolvimento, Rafael acompanha o resultado do treinamento por meio das métricas obtidas e da observação do comportamento do robô. Nessa análise, verifica a velocidade média, a distância percorrida, a taxa de quedas, a estabilidade durante o movimento e a localização do robô. **Na interface, ele consegue consultar esses indicadores em conjunto e visualizar a execução correspondente, relacionando os valores apresentados ao comportamento observado na simulação.**
Antes de executar um treinamento, Rafael e a equipe definem metas de desempenho relacionadas à distância percorrida, à velocidade, à frequência de quedas e ao equilíbrio do robô, pois, para conseguir marcar gols, o robô precisa caminhar de forma estável durante a partida. **A interface permite registrar ou consultar essas metas e utilizá-las como referência na análise dos resultados.**
Rafael realiza ajustes nos parâmetros da caminhada e observa uma melhora na velocidade. Apesar disso, o robô permanece menos tempo equilibrado, percorre uma distância maior, mas cai com frequência. O resultado, portanto, não representa necessariamente uma melhoria na capacidade de caminhar. **Ao consultar os indicadores, Rafael recebe informações sobre o significado de cada métrica e consegue identificar quais aspectos melhoraram e quais apresentaram piora, sem considerar apenas um valor isolado.**
Para entender melhor o que aconteceu, Rafael compara as métricas e as configurações utilizadas anteriormente. **Ele seleciona treinamentos anteriores para visualizar lado a lado seus resultados, parâmetros e informações de execução. A interface também permite consultar o histórico e localizar experimentos que possam servir de referência, considerando as características de cada execução.**
**Durante a comparação, a interface sinaliza quando existem informações ausentes ou diferenças nas condições dos treinamentos que podem limitar a análise. Assim, Rafael consegue considerar essas limitações antes de atribuir uma mudança de desempenho a determinado parâmetro.**
Ao final da análise, Rafael considera o conjunto das métricas e o comportamento observado para decidir se mantém os parâmetros utilizados ou realiza novos ajustes no próximo treinamento. **Ele pode registrar as observações sobre o experimento e consultar essas informações posteriormente, mantendo o histórico que servirá de apoio aos próximos ciclos de desenvolvimento.**
A análise é realizada durante os ciclos de desenvolvimento do robô, em um computador utilizado para executar os treinamentos. Como novos treinamentos são realizados a partir dos resultados anteriores, uma interpretação incorreta pode levar Rafael e a equipe a escolher parâmetros inadequados para o próximo experimento, desperdiçando tempo computacional e prolongando os ciclos de desenvolvimento.

### Diferenças relevantes

| Alteração | Por que foi necessária | Evidência/artefato que justifica |
|---|---|---|
| Consulta conjunta das métricas e da execução visual | Permitir que Rafael relacione os valores ao comportamento real do robô. | C01 e Entrega 1, seção 4.3: necessidade de analisar métricas e comportamento visual. |
| Consulta e registro das metas de desempenho | Dar contexto aos indicadores e permitir avaliar o resultado em relação ao que a equipe pretendia alcançar. | C01 refinado: metas de distância, velocidade, quedas e equilíbrio. |
| Explicação do significado das métricas | Evitar que o usuário interprete um indicador isoladamente ou sem conhecer seu significado. | Persona P01 e Entrega 3: necessidade de analisar diferentes métricas. |
| Comparação de treinamentos na interface | Reduzir a consulta manual de arquivos e facilitar a identificação de diferenças. | C01: comparação de métricas e configurações de diferentes execuções. |
| Sinalização de informações ausentes ou condições diferentes | Evitar conclusões inadequadas quando os experimentos não são diretamente comparáveis. | Entrega 1, seção 4.2, e C01: comparação depende das informações de cada execução. |
| Registro de observações sobre o experimento | Manter o contexto da análise para apoiar os próximos ciclos de treinamento. | C01: decisões sobre novos ajustes são realizadas a partir dos resultados anteriores. |

## CI02 — Recuperação da configuração de um treinamento anterior

**Autor(a):** Manuella Filipe Peres — 22.224.029-3  
**Origem:** cenário problema C02 — Recuperação da configuração de um treinamento anterior  

### Cenário de interação

Marina Oliveira, pesquisadora de robótica, está investigando diferentes estratégias utilizadas para melhorar a caminhada de um robô humanoide em simulação. Durante sua pesquisa, ela analisa resultados de treinamentos anteriores para compreender como as alterações nos parâmetros influenciam o comportamento do robô e identificar experimentos que possam servir de referência para novas investigações.
Após consultar resultados recentes que não apresentaram melhorias significativas, Marina se lembra de um treinamento realizado algumas semanas antes, no qual o robô percorreu uma distância maior e apresentou menor frequência de quedas. Ela decide investigar esse experimento para compreender quais configurações contribuíram para o resultado obtido.
**Para localizar a execução, Marina acessa o histórico de treinamentos e utiliza informações como período, identificação e resultados disponíveis para encontrar o experimento desejado. Ao selecionar uma execução, consegue consultar suas métricas e abrir os detalhes correspondentes.**
Para isso, Marina precisa identificar os parâmetros utilizados naquela execução. Entretanto, os parâmetros são configurados diretamente no código antes dos treinamentos, e diferentes alterações foram realizadas desde então. Ao consultar a pasta do experimento, ela encontra o modelo salvo e algumas anotações da equipe, mas essas informações não reúnem todos os valores utilizados na configuração original.
**Na interface, Marina consulta as configurações registradas para a execução selecionada, incluindo os parâmetros disponíveis, a versão do modelo e as informações sobre as condições em que o treinamento foi realizado. As informações são apresentadas relacionadas à identificação do experimento, para que ela não precise reconstruir seu contexto consultando arquivos separados.**
**Quando algum parâmetro ou informação não está registrado, a interface indica que o dado não está disponível, em vez de apresentar um valor presumido. Marina também consegue consultar as observações e os registros associados à execução para verificar se existem informações complementares.**
Marina procura relacionar os resultados do treinamento anterior aos das execuções recentes, mas precisa confirmar se os experimentos foram realizados nas mesmas condições. **Para isso, seleciona as execuções que deseja analisar e consulta suas métricas e configurações em conjunto. A interface apresenta as informações correspondentes e destaca diferenças ou dados ausentes que podem interferir na comparação.**
Sem essa confirmação, Marina não consegue determinar com segurança quais alterações podem ter influenciado as diferenças observadas no desempenho do robô. **Quando os registros não são suficientes para confirmar as condições dos experimentos, a interface informa essa limitação e Marina pode buscar esclarecimentos com os integrantes responsáveis pelos treinamentos antes de utilizar a execução como referência.**
**Depois de concluir a consulta, Marina pode manter o treinamento identificado como referência para sua pesquisa e registrar observações sobre o que foi analisado. Dessa forma, as informações disponíveis sobre o experimento podem ser recuperadas em consultas futuras.**
Essa situação facilita a interpretação dos resultados e reduz a dependência da busca manual por informações distribuídas entre diferentes arquivos e registros, apoiando a escolha de experimentos anteriores como referência para novas investigações.

### Diferenças relevantes

| Alteração | Por que foi necessária | Evidência/artefato que justifica |
|---|---|---|
| Inclusão de histórico e recursos de busca | Facilitar a localização de uma execução entre diferentes treinamentos. | C02 refinado, questão Q1: localização do treinamento entre pastas e registros. |
| Apresentação das configurações relacionadas à execução | Permitir recuperar os parâmetros sem reconstruir manualmente o contexto do experimento. | C02 e Entrega 1, seções 4.1 e 4.2: parâmetros no código e informações distribuídas. |
| Identificação de informações ausentes | Evitar que valores não registrados sejam tratados como se fossem conhecidos. | C02 refinado, questões Q2 e Q3: registros incompletos e necessidade de verificar condições. |
| Comparação de métricas, parâmetros e condições | Ajudar a compreender quais diferenças podem estar relacionadas ao desempenho. | C02: dificuldade para confirmar se os treinamentos ocorreram nas mesmas condições. |
| Comunicação de limitações da comparação | Evitar conclusões sem evidências suficientes e orientar a busca de informações adicionais. | C02 refinado, questão Q5: avaliação sobre utilizar o experimento como referência. |
| Preservação do treinamento como referência e registro de observações | Apoiar novas investigações e permitir recuperar o contexto da análise. | C02 refinado: intenção de utilizar o treinamento como referência e manter informações do experimento. |

## CI03 — Avaliação de treinamentos em reunião de orientação

**Autor(a):** Rafaela Altheman de Campos — 22.125.062-4  
**Origem:** cenário problema C03 — Avaliação de treinamentos em reunião de orientação  

### Cenário de interação

Carlos Almeida, professor e orientador de uma equipe universitária de robótica humanoide, acompanha o desenvolvimento da caminhada de um robô projetado para jogar futebol. Como não participa diretamente de todos os treinamentos, utiliza as reuniões com os estudantes para compreender os resultados obtidos e orientar as próximas etapas do desenvolvimento.
**Antes da reunião, a estudante responsável pelo acompanhamento seleciona os treinamentos e as informações que serão apresentados. A interface permite organizar os resultados relevantes de cada execução, reunindo os indicadores necessários para a discussão e mantendo disponíveis os detalhes para consulta quando houver dúvidas.**
Durante uma reunião de acompanhamento, uma estudante apresenta os resultados de um treinamento recente. O gráfico da recompensa indica um aumento em relação à execução anterior, sugerindo inicialmente uma possível melhoria. Entretanto, Carlos precisa compreender se essa evolução numérica corresponde a um avanço real no comportamento do robô.
**A apresentação reúne a recompensa e outros indicadores importantes, como distância percorrida, velocidade, estabilidade e frequência de quedas. Os resultados podem ser relacionados à execução visual do robô no simulador, permitindo que Carlos compreenda melhor o comportamento correspondente aos valores apresentados.**
Para avaliar o treinamento, Carlos considera importante relacionar a recompensa obtida a outros indicadores, além de observar o comportamento do robô durante a simulação. O aumento da recompensa, quando apresentado isoladamente, não permite concluir que houve melhoria na locomoção. Um robô pode obter uma recompensa elevada sem apresentar deslocamento satisfatório.
Para isso, pergunta qual foi a distância percorrida, quantas quedas ocorreram e quais alterações foram realizadas em comparação ao treinamento anterior. **Quando precisa investigar algum resultado, Carlos consegue consultar os detalhes da execução e comparar os indicadores com os de treinamentos anteriores, sem interromper a apresentação para procurar manualmente arquivos e anotações em diferentes locais.**
Ao observar o comportamento do robô, Carlos percebe que ele permanece equilibrado durante parte da execução, mas apresenta pouco deslocamento. Dessa forma, o aumento da recompensa não representa necessariamente uma melhoria na capacidade de caminhar. **A interface apresenta descrições dos indicadores e permite consultar as condições e configurações relacionadas aos resultados, ajudando a equipe a discutir as possíveis causas das diferenças observadas.**
**Durante a reunião, Carlos e a estudante podem registrar os pontos discutidos, os problemas identificados e as orientações para os próximos experimentos. O registro fica relacionado ao treinamento analisado, permitindo que a equipe consulte posteriormente as conclusões e os ajustes propostos.**
Ao final da discussão, Carlos utiliza as informações apresentadas para orientar a equipe sobre quais aspectos precisam ser investigados e quais ajustes podem ser considerados nos próximos treinamentos. **Caso ainda faltem informações para concluir a avaliação, a interface permite identificar os pontos que precisam de análise complementar, evitando que uma decisão seja tomada apenas com base em uma métrica isolada.**
Dessa forma, a reunião consegue se concentrar na interpretação dos resultados e na definição dos próximos passos, reduzindo o tempo gasto para recuperar informações e facilitando o acompanhamento da evolução do projeto.

### Diferenças relevantes

| Alteração | Por que foi necessária | Evidência/artefato que justifica |
|---|---|---|
| Preparação e seleção prévia dos resultados | Permitir que a estudante apresente as informações mais relevantes durante a reunião. | C03 refinado, questão Q3: informações não estavam organizadas previamente. |
| Visão consolidada das métricas | Dar ao orientador uma leitura geral do desempenho sem depender apenas da recompensa. | Persona P03 e C03: necessidade de visão consolidada e comparação de resultados. |
| Relação entre indicadores e execução visual | Ajudar a interpretar se a evolução numérica corresponde à melhoria real da caminhada. | Entrega 1, seção 4.4, e C03: recompensa elevada sem deslocamento satisfatório. |
| Consulta dos detalhes durante a reunião | Permitir investigar dúvidas sem procurar manualmente arquivos separados. | C03: necessidade de consultar arquivos de métricas, anotações e simulador. |
| Registro de conclusões e orientações | Preservar as decisões discutidas para orientar os próximos experimentos. | C03 refinado, questão Q5: necessidade de registrar e recuperar decisões. |
| Identificação de pontos que exigem análise complementar | Evitar decisões precipitadas quando faltam informações para avaliar o treinamento. | C03 refinado, questões Q2, Q4 e Q6: critérios de avaliação e consequências do adiamento. |

## 2. Design centrado na comunicação

**Nome do cenário:** {{CI01}}

| Tópico > subtópico | Falas e signos envolvidos | Intenção/efeito esperado |
|---|---|---|
| {{objetivo}} | `U: ...` / `D: ...` | {{...}} |
| > {{subtópico}} | {{...}} | {{...}} |

**Convenção:** `U` = usuário; `D` = preposto do designer/sistema, conforme a abordagem de Engenharia Semiótica adotada na disciplina.

## 3. Mapa de objetivos

Cada integrante apresenta seu mapa e a equipe cria um **mapa consolidado**, eliminando duplicidades e resolvendo conflitos de nomenclatura.

![Mapa consolidado](../assets/09_modelo_conceitual/mapa_objetivos.svg)

### Dicionário de objetivos

| ID | Objetivo | Persona(s) | Cenário(s) | Prioridade |
|---|---|---|---|---|
| O01 | {{...}} | {{P01}} | {{CI01}} | {{...}} |

## 4. Esquema conceitual de signos

Consolide as informações em **uma tabela única**.

| Grupo | Signo | Origem | Observações/semântica | Tipo de conteúdo | Restrição | Valor padrão | Prevenção | Recuperação |
|---|---|---|---|---|---|---|---|---|
| Credenciais | usuário | domínio | {{...}} | texto | não nulo | — | {{...}} | {{...}} |

### Regras para os signos

- Use o vocabulário do domínio do usuário.
- Evite duplicar o mesmo conceito com nomes diferentes.
- Diferencie informação fornecida pelo usuário, produzida pelo sistema e derivada do domínio.
- Registre prevenção e recuperação apenas quando fizer sentido; explique as siglas usadas.

## Síntese

Quais objetivos/tópicos/signos deverão necessariamente aparecer nos diagramas MoLIC?

## Checklist

- [ ] Cenários de interação mostram alterações em relação aos cenários de problema.
- [ ] Cada solução individual identifica autor e cenário de origem.
- [ ] Tópicos/falas/signos são coerentes com objetivos do usuário.
- [ ] Mapas individuais foram consolidados.
- [ ] O esquema de signos está em uma tabela única e sem duplicações conceituais.
- [ ] Nomes de objetivos/signos serão reutilizados na Entrega 10.
- [ ] Em TCC técnico, signos representam conceitos do domínio compreensíveis ao usuário, não apenas variáveis/estruturas internas.
- [ ] Padrões como dashboard, relatório, filtros, administração e CRUD possuem objetivos e signos correspondentes.
- [ ] A interface comunica não só o resultado técnico, mas também seu significado para a tarefa.

# Entrega 6 — Prototipação em papel

**Data:** {{28/10/2026}}  
**Status:** 🟨 em andamento
**Responsabilidade:** 1 solução integrada por equipe

## Objetivo da atividade

Externalizar rapidamente ideias de interação em baixa fidelidade para explorar alternativas antes de investir em detalhes visuais. O valor da atividade está no **ciclo construir → simular → observar → revisar**, não na beleza do desenho.

## 1. Escopo do protótipo

### Personas:

P01 — Rafael Martins: responsável por avaliar os resultados dos treinamentos e identificar se houve melhoria real no desempenho do robô.

P02 — Marina Oliveira: responsável por localizar execuções anteriores, comparar experimentos e investigar possíveis causas para diferenças de desempenho.

P03 — Carlos Almeida: responsável por acompanhar a evolução do desempenho do robô, interpretar indicadores e comunicar à equipe os pontos que precisam de investigação.

### Cenários/tarefas cobertos:

C01/T01: avaliar se o resultado de um treinamento representa uma melhoria real no desempenho do robô, comparando indicadores com uma execução de referência (baseline) e registrando uma conclusão fundamentada.

C02/T02: localizar duas execuções anteriores por identificadores ou filtros, comparar suas métricas e parâmetros e registrar uma hipótese para explicar as diferenças encontradas, acompanhada de evidências e ressalvas.

C03/T03: consultar uma síntese da evolução do desempenho ao longo dos treinamentos, identificar pontos relevantes de investigação e apresentar os resultados à equipe, permitindo consultar evidências detalhadas durante a reunião.

### Objetivos principais:

O protótipo tem como objetivo explorar uma solução integrada de visualização e análise dos resultados dos treinamentos do robô humanoide, facilitando a interpretação dos indicadores e apoiando decisões da equipe sobre possíveis melhorias e necessidades de investigação.

Para isso, a interface deverá permitir:

Visualizar os resultados de treinamentos, incluindo velocidade média, distância percorrida, taxa de quedas, estabilidade, gols marcados e força de chute.

Consultar o histórico de execuções utilizando busca por identificador e filtros de período, versão e parâmetros.

Selecionar e comparar duas execuções, apresentando métricas e configurações lado a lado para facilitar a identificação de diferenças.

Avaliar se uma execução apresentou melhoria em relação a um baseline, considerando ganhos e possíveis regressões em diferentes indicadores.

Registrar conclusões e hipóteses com justificativas, evidências e ressalvas, mantendo a associação com as execuções analisadas.

Acompanhar a evolução dos indicadores e parâmetros ao longo do tempo por meio de um painel de síntese.

Apoiar a comunicação dos resultados durante reuniões, mantendo a interpretação e a definição dos encaminhamentos sob responsabilidade da equipe.

## 1.1 Possíveis famílias de interface

Escolha apenas o que for coerente com tarefas e cenários. Para TCCs técnicos, o protótipo pode explorar:

- **dashboard** para monitoramento e tomada de decisão;
- **configuração/parametrização** para preparar algoritmo/modelo/processo;
- **entrada/seleção de dados** com validação;
- **acompanhamento de execução** com progresso, fila, cancelamento e recuperação;
- **relatório/resultados** com explicação, gráficos e exportação;
- **histórico** com busca, filtros, ordenação e detalhes;
- **comparação** entre execuções, versões, algoritmos ou períodos;
- **administração** de usuários, papéis, permissões ou entidades do domínio;
- **auditoria/logs** traduzidos para o perfil;
- **alertas/ocorrências** com ação de resposta.

> Não desenhe todas essas telas por obrigação. O objetivo da baixa fidelidade é experimentar a **estrutura da interação** necessária para as tarefas priorizadas.

## 2. Fluxos escolhidos

Os fluxos foram definidos com base nas três tarefas priorizadas na Entrega 5, contemplando a avaliação de treinamentos, a comparação de execuções anteriores e o acompanhamento da evolução do desempenho do robô. A proposta é integrar essas funcionalidades em uma única interface, permitindo que diferentes integrantes da equipe consultem os resultados de acordo com seus objetivos.

| Fluxo | Tarefa/objetivo | Por que foi priorizado |
|---|---|---|
| PF01 | T01 — Avaliar melhoria de um treinamento: selecionar uma execução, definir um baseline comparável, analisar métricas e evidências e registrar uma conclusão sobre o desempenho. | É uma atividade frequente e crítica para a evolução do robô. A classificação em melhoria, não melhoria e sem evidências indica se os treinos estão seguindo o caminho certo |
| PF02 | T02 — Localizar e comparar execuções anteriores: buscar duas execuções por ID ou filtros, comparar métricas e parâmetros e registrar uma hipótese sobre as diferenças encontradas. | Garante rastreabilidade dos experimentos e permite investigar variações de desempenho. |
| PF03 | T03 — Consultar síntese e comunicar pontos de investigação: selecionar um período, visualizar a evolução dos indicadores, identificar pontos relevantes e apresentar os resultados à equipe, consultando evidências detalhadas quando necessário. | Apoia reuniões de acompanhamento e decisões sobre futuras investigações. O fluxo permite organizar os resultados e manter o contexto da análise durante a comunicação com a equipe. |

### Descrição dos fluxos

**PF01 — Avaliação de melhoria do treinamento**

O usuário acessa o histórico de treinamentos e seleciona uma execução para avaliação. Em seguida, escolhe um baseline e consulta as métricas e evidências disponíveis. Após analisar os resultados, classifica o treinamento como melhoria, não melhoria ou evidências insuficientes, registrando uma justificativa associada às execuções.

**PF02 — Localização e comparação de execuções**

O usuário localiza duas execuções anteriores utilizando identificadores conhecidos ou filtros do histórico. Depois de confirmar as seleções, acessa uma visualização comparativa das métricas, versões e parâmetros. Com base nas divergências observadas, formula uma hipótese explicativa, registra as evidências utilizadas e indica possíveis limitações da análise.

**PF03 — Acompanhamento e comunicação do desempenho**

O usuário seleciona um período de análise e consulta um painel com a evolução dos principais indicadores dos treinamentos. A partir dos resultados, identifica tendências, regressões e pontos que precisam de investigação. Durante a apresentação à equipe, pode consultar evidências detalhadas sem perder o contexto do painel. Por fim, a equipe discute os resultados e define os encaminhamentos necessários.

### Integração entre os fluxos

Os três fluxos compartilham informações sobre execuções, métricas e parâmetros dos treinamentos. O histórico e a comparação de resultados atendem principalmente aos fluxos PF01 e PF02, enquanto o painel de evolução temporal atende ao PF03.

Essa integração permite reutilizar componentes e informações, evitando a criação de telas independentes para funcionalidades semelhantes. A prototipação em papel deverá representar tanto os caminhos principais quanto situações relevantes, como ausência de dados, incompatibilidade entre execuções e retorno ao painel após a consulta de evidências.


## 3. Telas e estados

A navegação foi estruturada por meio de um menu lateral compartilhado entre as telas, contendo as opções Painel Geral, Histórico, Comparação, Avaliação, Reunião. Essa organização busca manter a consistência da interface e facilitar o deslocamento entre funcionalidades relacionadas.

Durante a simulação em papel, os controles desenhados representam ações do usuário, enquanto a troca das folhas corresponde às transições entre telas. A numeração P01 a P10 identifica os estados do protótipo e permite relacioná-los aos fluxos e às tarefas analisadas anteriormente.

### P01 — Painel geral de desempenho

**Fluxo relacionado:** PF03 — Consultar síntese e comunicar pontos de investigação.

A tela P01 representa a visão inicial do sistema, oferecendo uma síntese dos resultados dos treinamentos do robô humanoide. Seu objetivo é permitir que os integrantes da equipe acompanhem a evolução do desempenho sem precisar consultar individualmente cada execução realizada.

Na parte superior, o usuário encontra o controle de seleção do período de análise. Após definir o intervalo desejado e aplicar a consulta, o painel apresenta indicadores consolidados, incluindo velocidade média, distância percorrida, taxa de quedas e estabilidade.

A região central contém um gráfico de evolução dos treinamentos, permitindo identificar tendências e alterações no comportamento dos indicadores ao longo do tempo. Uma área lateral apresenta pontos de atenção que podem exigir investigação adicional.

Essa organização procura facilitar uma interpretação inicial dos resultados e apoiar a identificação de questões relevantes para as reuniões de acompanhamento.

**Controles e navegação:**

- Selecionar o período de análise.
- Acionar o botão "Aplicar" para atualizar os resultados.
- Consultar os indicadores e o gráfico de evolução.
- Selecionar "Abrir evidência" para acessar P08.
- Acessar o histórico de execuções (P02).
- Acessar a área de reunião (P07).
- Quando o período não apresentar dados, visualizar P10.

![P01 — Painel geral de desempenho](../assets/06_prototipos/P01_painel_geral.jpeg)

### P02 — Histórico de execuções

**Fluxos relacionados:** PF01 — Avaliação de treinamento e PF02 — Localização e comparação de execuções.

A tela P02 apresenta o histórico dos treinamentos realizados, permitindo localizar execuções anteriores e selecionar registros para análise comparativa.

Na parte superior, existe um campo de busca por identificador, acompanhado de um botão para executar a pesquisa. Também há a possibilidade de utilizar filtros de período e versão, oferecendo diferentes maneiras de localizar um treinamento conforme as informações disponíveis.

A área central apresenta uma lista de execuções com seus identificadores, datas, versões e estados de conclusão. Cada registro possui um controle de seleção, permitindo escolher duas execuções para comparação.

Na parte inferior, a interface apresenta a quantidade de execuções selecionadas, ajudando o usuário a compreender quantos registros ainda precisam ser escolhidos antes de iniciar a comparação.

**Controles e navegação:**

- Digitar o identificador de uma execução no campo de busca.
- Acionar o botão "Buscar".
- Aplicar filtros de período e versão.
- Selecionar duas execuções na lista.
- Conferir a quantidade de registros selecionados.
- Acionar "Comparar selecionadas" para acessar P03.
- Visualizar P09 quando a pesquisa não encontrar resultados.
- Retornar ao painel geral (P01).

![P02 — Histórico de execuções](../assets/06_prototipos/P02_historico_execucoes.jpeg)

### P03 — Comparação de execuções

**Fluxos relacionados:** PF01 — Avaliação de melhoria e PF02 — Investigação de diferenças de desempenho.

A tela P03 permite comparar os resultados de duas execuções selecionadas anteriormente no histórico. Seu objetivo é apresentar os dados de maneira organizada para facilitar a identificação de diferenças entre os treinamentos.

Na parte superior, são exibidos os identificadores das execuções, suas versões e datas. A região central apresenta uma tabela com as métricas dispostas lado a lado, permitindo comparar velocidade média, distância percorrida, taxa de quedas, estabilidade, gols marcados e força de chute.

A estrutura facilita a identificação de indicadores que apresentaram melhoria ou regressão entre os experimentos. Além disso, existe uma área destinada às diferenças de configuração, permitindo relacionar alterações nos parâmetros às variações observadas nos resultados.

A comparação não determina automaticamente qual execução é superior nem estabelece relações causais entre mudanças de configuração e desempenho. Essas interpretações permanecem sob responsabilidade do usuário.

**Controles e navegação:**

- Visualizar as duas execuções selecionadas.
- Comparar métricas e parâmetros lado a lado.
- Examinar diferenças de configuração.
- Selecionar "Voltar ao histórico" para retornar à P02.
- Selecionar "Registrar hipótese" para acessar P04.
- Selecionar "Avaliar desempenho" para acessar P05.

![P03 — Comparação de execuções](../assets/06_prototipos/P03_comparacao_execucoes.jpeg)

### P04 — Registro de hipóteses e ressalvas

**Fluxo relacionado:** PF02 — Localizar e comparar execuções anteriores.

A tela P04 representa a etapa de formulação e registro de uma hipótese explicativa sobre as diferenças encontradas entre duas execuções.

O contexto da comparação permanece identificado na parte superior, apresentando os IDs das execuções analisadas. A interface organiza as informações em três áreas principais: diferenças observadas, hipótese explicativa e ressalvas ou limitações.

A primeira área permite consultar as divergências efetivamente identificadas nos resultados. A segunda disponibiliza um campo para o usuário escrever uma possível explicação para essas diferenças. A terceira permite registrar fatores que podem limitar a interpretação, como condições divergentes entre treinamentos.

A separação entre evidências, hipóteses e ressalvas busca evitar que uma correlação entre parâmetros e resultados seja interpretada como uma relação causal comprovada.

**Controles e navegação:**

- Consultar as diferenças observadas.
- Preencher o campo de hipótese explicativa.
- Informar ressalvas e limitações da análise.
- Selecionar "Voltar à comparação" para retornar à P03.
- Acionar "Salvar hipótese e ressalvas" para registrar a análise.

![P04 — Registro de hipóteses e ressalvas](../assets/06_prototipos/P04_hipoteses_ressalvas.jpeg)

### P05 — Avaliação do resultado do treinamento

**Fluxo relacionado:** PF01 — Avaliar se um treinamento apresentou melhoria real no desempenho.

A tela P05 representa a etapa de avaliação de um treinamento em relação a uma execução de referência, denominada baseline.

Na parte superior, são identificadas a execução avaliada e a referência utilizada na comparação. O usuário pode solicitar a troca do baseline caso identifique a necessidade de selecionar outra execução.

A região central apresenta uma área dedicada às evidências quantitativas, incluindo gráficos de desempenho, enquanto uma seção complementar disponibiliza informações sobre o comportamento do robô durante a simulação.

Depois de analisar os resultados, o usuário deve selecionar uma classificação entre três possibilidades: melhoria, não melhoria ou evidências insuficientes.

A classificação deve ser acompanhada de uma justificativa, permitindo documentar os indicadores e comportamentos que fundamentaram a decisão.

A existência da opção "evidências insuficientes" é importante para representar situações em que os dados não permitem determinar com segurança se houve uma melhoria real.

**Controles e navegação:**

- Consultar a execução e o baseline selecionados.
- Acionar "Trocar baseline".
- Analisar gráficos e indicadores de desempenho.
- Selecionar "Abrir detalhe" para acessar P08.
- Escolher uma das três classificações disponíveis.
- Preencher o campo de justificativa obrigatória.
- Selecionar "Voltar à comparação" para retornar à P03.
- Acionar "Salvar avaliação" para acessar P06.

![P05 — Avaliação do treinamento](../assets/06_prototipos/P05_avaliacao_treinamento.jpeg)

### P06 — Confirmação do registro

**Fluxos relacionados:** PF01 — Avaliação do treinamento e PF02 — Registro de análise.

A tela P06 apresenta uma confirmação visual após o salvamento de um registro de análise. Sua finalidade é informar ao usuário que a operação foi concluída e permitir a conferência das informações associadas ao registro.

No exemplo representado no protótipo, a confirmação corresponde a uma avaliação de treinamento vinculada à execução EXEC-104 e à referência EXEC-103, com a conclusão "não melhoria".

A interface apresenta o tipo de registro realizado, os identificadores envolvidos e a classificação registrada, permitindo verificar se a análise foi associada aos treinamentos corretos.

Esse estado procura evitar incertezas sobre a conclusão da operação e oferece caminhos para continuar utilizando o sistema.

**Controles e navegação:**

- Consultar as informações do registro salvo.
- Selecionar "Ver registro" para acessar os detalhes.
- Selecionar "Voltar ao painel" para retornar à P01.
- Selecionar "Histórico" para acessar P02.

![P06 — Confirmação do registro](../assets/06_prototipos/P06_confirmacao_registro.jpeg)

### P07 — Reunião e apresentação dos resultados

**Fluxo relacionado:** PF03 — Consultar síntese e comunicar pontos de investigação.

A tela P07 representa o uso do painel durante uma reunião de acompanhamento dos treinamentos.

Na parte superior, são apresentados o período de análise e a identificação da síntese de desempenho. A região central contém um gráfico que permite observar a evolução dos resultados, enquanto uma área lateral reúne os pontos que precisam ser discutidos com a equipe.

Essa organização procura apoiar a apresentação das informações e facilitar o acompanhamento dos indicadores durante a reunião.

O usuário pode apresentar a interpretação dos resultados e consultar evidências detalhadas para complementar as explicações. A consulta deve permitir o retorno à apresentação sem perda do contexto anterior.

As discussões sobre prioridades e a definição dos encaminhamentos continuam sendo realizadas pelos integrantes da equipe.

**Controles e navegação:**

- Consultar os indicadores do período selecionado.
- Visualizar os pontos a discutir.
- Selecionar "Abrir evidência" para acessar P08.
- Acionar "Próximo indicador" para continuar a apresentação.
- Selecionar "Retornar ao painel" para acessar P01.

![P07 — Reunião e apresentação dos resultados](../assets/06_prototipos/P07_reuniao_apresentacao.jpeg)

### P08 — Evidência detalhada da execução

**Fluxos relacionados:** PF01 — Avaliação de treinamento e PF03 — Apresentação dos resultados.

A tela P08 apresenta uma visualização detalhada de uma execução específica, permitindo que o usuário consulte informações complementares às métricas apresentadas nas telas anteriores.

A interface possui uma área destinada ao registro visual do comportamento do robô em simulação, acompanhada de um painel lateral com dados sobre a execução.

O contexto de origem é identificado por meio de informações como o ID da execução, o período e o indicador analisado.

A principal finalidade dessa tela é permitir o aprofundamento da análise sem exigir que o usuário reinicie a tarefa. Isso é especialmente importante durante uma reunião, quando a consulta a uma evidência pode ocorrer enquanto os resultados estão sendo apresentados.

**Controles e navegação:**

- Consultar o registro visual do comportamento do robô.
- Visualizar informações complementares da execução.
- Conferir o identificador e o contexto da evidência.
- Selecionar "Voltar à apresentação" para retornar à tela anterior, preservando o contexto.

![P08 — Evidência detalhada](../assets/06_prototipos/P08_evidencia_detalhada.jpeg)

### P09 — Estado de busca sem resultados

**Fluxos relacionados:** PF01 e PF02 — Localização de execuções.

A tela P09 representa um estado alternativo em que a busca por um identificador não encontra nenhuma execução correspondente.

No exemplo desenhado, a pesquisa pelo identificador EXEC-999 não retorna resultados. A interface apresenta uma mensagem informativa e orienta o usuário a verificar o identificador ou utilizar filtros alternativos.

A inclusão desse estado busca evitar que uma pesquisa sem resultados seja interpretada como falha do sistema. Além disso, são oferecidas alternativas para que o usuário consiga retomar a tarefa sem abandonar o processo.

**Controles e navegação:**

- Visualizar a mensagem de ausência de resultados.
- Selecionar "Corrigir ID" para modificar a pesquisa.
- Selecionar "Usar filtros" para buscar por outros critérios.
- Selecionar "Voltar ao histórico" para retornar à P02.

![P09 — Busca sem resultados](../assets/06_prototipos/P09_busca_sem_resultados.jpeg)

### P10 — Estado de painel sem dados no período

**Fluxo relacionado:** PF03 — Acompanhamento da evolução do desempenho.

A tela P10 representa a situação em que o usuário seleciona um período para análise, mas não existem resultados de treinamento disponíveis naquele intervalo.

No exemplo apresentado, o painel informa a ausência de resultados para o período selecionado e orienta o usuário a ampliar o intervalo ou consultar o histórico.

Esse estado é importante porque diferencia a ausência de dados de indicadores com valores iguais a zero ou de possíveis falhas de carregamento.

A interface permite recuperar a interação por meio da alteração do período ou da navegação para outras áreas do sistema.

**Controles e navegação:**

- Visualizar a mensagem de ausência de dados.
- Selecionar "Alterar período" para definir outro intervalo.
- Selecionar "Abrir histórico" para acessar P02.
- Selecionar "Retornar ao painel" para acessar P01.

![P10 — Painel sem dados no período](../assets/06_prototipos/P10_painel_sem_dados.jpeg)

### Organização da navegação entre telas

As dez telas foram organizadas em uma estrutura integrada, permitindo que diferentes tarefas compartilhem componentes e informações. Embora estejam numeradas para facilitar a documentação, sua utilização não depende de uma sequência única, pois cada fluxo possui caminhos próprios e estados alternativos.

**PF01 — Avaliação de treinamento:**

P02 (Histórico) → P03 (Comparação) → P05 (Avaliação) → P06 (Confirmação).

Durante esse fluxo, P08 pode ser acessada para consultar evidências detalhadas. Caso uma pesquisa não encontre resultados, o usuário pode acessar P09 e corrigir a busca.

**PF02 — Localização e comparação de execuções:**

P02 (Histórico) → P03 (Comparação) → P04 (Hipóteses e ressalvas).

O usuário pode retornar ao histórico para modificar as execuções selecionadas. Caso a pesquisa não encontre resultados, P09 apresenta alternativas para continuar a tarefa.

**PF03 — Acompanhamento e comunicação do desempenho:**

P01 (Painel geral) → P07 (Reunião) → P08 (Evidência detalhada) → P07 (Retorno à reunião).

Quando o período selecionado não possui dados, o sistema apresenta P10, permitindo alterar o intervalo ou consultar o histórico.

A organização proposta busca preservar o contexto das análises e reduzir a necessidade de repetir operações durante a navegação. Na simulação em papel, as transições serão representadas pela troca das folhas correspondentes às ações realizadas pelo participante.

Os estados alternativos foram incluídos para observar como o usuário reage a situações inesperadas e se os controles apresentados permitem a recuperação da tarefa.


## 4. Simulação / walkthrough

Realize uma simulação com uma pessoa que não participou da elaboração dessas telas. Um colega pode ser usado **para essa iteração formativa**, mas isso não substitui os participantes finais da Entrega 14.

Transcrição da simulação:

Moderador: Tá, então é o seguinte: a gente fez umas telas de um sistema pra acompanhar o desempenho de um robô que é treinado pra jogar futebol. Eu vou te dar umas tarefas e você vai falando o que tá pensando enquanto tenta fazer, beleza?

Participante: Tá bom. Eu não entendo muito de robô, mas vamos lá, kkk.

Moderador: Não tem problema. A ideia é justamente ver se dá pra entender as telas sem a gente ficar explicando.

Moderador: Primeiro, imagina que você precisa encontrar dois treinamentos, o 103 e o 104, e comparar os resultados deles.

Participante: Tá... deixa eu olhar aqui. Tem painel geral, histórico, comparação... Acho que eu iria direto em comparação.

Moderador: Pode tentar.

Participante: Ué, mas eu tenho que escolher os treinamentos antes, né? Acho que seria no histórico então.

Moderador: Pode seguir.

Participante: Ah, aqui tem os dois. O 104 e o 103. Vou marcar eles.

Participante: Pera, é pra marcar só dois? Ah, tá escrito ali embaixo, selecionados zero de dois. Beleza.

Participante: Agora apareceu dois de dois. Vou clicar em comparar selecionadas.

Moderador: E aí, conseguiu entender essa tela?

Participante: Acho que sim. Tá mostrando os dois lado a lado, né? A velocidade de um é 0,32 e do outro 0,28.

Participante: Nossa, mas olha aqui, o que tá mais rápido também cai mais. Então não é necessariamente melhor, né?

Moderador: O que mais você olharia?

Participante: A estabilidade também. Aqui tá 78 e 84. Então o 104 tá mais rápido, só que tá menos estável.

Participante: Só não entendi esse negócio de diferenças de configuração. Era pra aparecer o que mudou?

Moderador: O que você esperava encontrar ali?

Participante: Ah, sei lá, tipo, qual configuração usaram no 103 e qual usaram no 104. Porque aí daria pra entender o que mudou.

Moderador: Entendi. Agora imagina que você precisa registrar uma explicação pra essa diferença.

Participante: Acho que é nesse registrar hipótese aqui.

Participante: Ah, beleza. Tem as diferenças observadas e aí eu escrevo o que acho que aconteceu.

Participante: Eu colocaria que alguma mudança deixou ele mais rápido, mas acabou fazendo ele cair mais. Só que eu não sei exatamente o que mudou, então não dá pra afirmar.

Moderador: E as ressalvas?

Participante: Acho que é isso que eu falei, que não dá pra ter certeza se foi por causa da configuração. Eu colocaria aí.

Moderador: Agora você precisa decidir se o treinamento 104 realmente melhorou em relação ao 103.

Participante: Tá. Vou voltar aqui... acho que é avaliação.

Participante: Ah, aqui tem o 104 e o baseline 103. Baseline é o treinamento que eu tô usando pra comparar?

Moderador: Isso.

Participante: Tá, entendi. Mas acho que podia ter escrito referência também, porque baseline eu não saberia de primeira.

Participante: Aqui tem o gráfico, mas eu não tô entendendo qual linha é qual. Tem duas linhas e não tem uma legenda.

Moderador: O que você faria?

Participante: Eu tentaria abrir esse detalhe aqui do comportamento do robô.

Participante: Ah, aqui seria o vídeo dele andando. Legal. Porque só os números não mostram se ele tá andando esquisito ou caindo toda hora.

Participante: Só que agora eu quero voltar pra avaliação. Esse botão tá escrito voltar à apresentação... Mas eu não tava apresentando nada.

Moderador: E isso te atrapalharia?

Participante: Um pouco, porque eu ia ficar com medo de voltar pra uma tela nada a ver. Eu colocaria só "Voltar" ou "Voltar à avaliação".

Moderador: Tá. Agora você precisa escolher uma classificação.

Participante: Eu acho que colocaria não melhoria. Porque ele ficou mais rápido, mas a estabilidade piorou e ele caiu mais.

Participante: Aí eu escreveria isso na justificativa e salvaria.

Moderador: E essa tela de confirmação?

Participante: Ah, essa tá boa. Mostra que salvou mesmo. Eu gosto quando aparece isso, porque senão fico naquela dúvida se foi ou não.

Moderador: Agora imagina que você quer trocar o treinamento usado como referência.

Participante: Tá, vou naquele trocar baseline.

Participante: Aqui aparece uma lista. Acho que eu escolheria o 102, porque é outro treinamento anterior.

Moderador: Pode selecionar.

Participante: Opa, apareceu que não é compatível.

Participante: Ah, entendi, porque é outra versão. Tem outras diferenças também.

Moderador: O que você faria nessa situação?

Participante: Eu acho que escolheria outro. Se o sistema tá falando que não dá pra comparar direito, melhor não arriscar.

Participante: Mas achei legal que ele explica o motivo. Se só aparecesse "incompatível", eu não ia entender nada.

Moderador: Você usaria a opção de continuar com ressalva?

Participante: Talvez, se eu precisasse muito comparar esses dois. Mas aí teria que deixar bem claro que a comparação pode não ser justa.

Moderador: Agora imagina que você vai mostrar pra equipe como o robô evoluiu nos últimos 30 dias.

Participante: Tá, acho que agora eu iria no painel geral.

Participante: Ah, aqui já tem os últimos 30 dias. Tem velocidade, distância, quedas... Essa tela parece mais fácil.

Moderador: E como você faria pra apresentar isso pra equipe?

Participante: Tem reunião aqui no menu. Vou clicar.

Participante: Ah, aqui parece uma apresentação mesmo. Tem o gráfico maior e os pontos pra discutir.

Participante: Só esse botão de próximo indicador que eu fiquei meio perdido. Próximo indicador qual?

Moderador: O que você colocaria no lugar?

Participante: Talvez "Próximo: estabilidade", por exemplo. Aí eu já saberia o que vai aparecer.

Moderador: E se alguém da reunião perguntasse por que a taxa de quedas aumentou?

Participante: Eu clicaria em abrir evidência pra mostrar o treinamento específico.

Participante: Aí depois voltaria pra reunião.

Participante: Isso eu achei importante, porque imagina ter que escolher o período tudo de novo no meio da reunião. Ia ser chato.

Moderador: Agora vou te mostrar mais uma tela, que é pra configurar um novo treinamento do robô. O que você acha que faria aqui?

Participante: Nossa, essa tem bem mais coisa, hein, kkk.

Participante: Tem o nome, o robô, o simulador... Essa parte eu entendi. Mas esses números aqui eu não faço ideia do que significam.

Moderador: Quais?

Participante: Learning rate, batch size, gamma... Essas coisas. Acho que quem trabalha com isso vai entender, mas eu teria medo de mudar alguma coisa errada.

Moderador: O que te ajudaria?

Participante: Talvez deixar os valores recomendados já preenchidos. E colocar um negocinho explicando cada um.

Participante: Aqui embaixo tem iniciar treinamento. Se eu clicar, começa direto?

Moderador: O que você esperaria?

Participante: Eu esperaria aparecer uma confirmação antes, porque parece que demora bastante, né? Vai que eu coloquei alguma coisa errada.

Moderador: Entendi.

Participante: E depois que começa, eu ia querer ver se tá rodando mesmo, quanto falta, se deu erro... Alguma tela de progresso.

Moderador: Beleza. Agora falando de tudo que você viu, o que achou mais fácil?

Participante: Acho que o histórico e a comparação. Dá pra entender bem o que tem que fazer.

Moderador: E o que achou mais difícil?

Participante: A parte do treinamento, por causa dos parâmetros. E também fiquei um pouco perdido nos gráficos porque não sabia qual linha representava qual execução.

Moderador: Você mudaria alguma coisa na navegação?

Participante: Ah, eu deixaria os botões de voltar mais claros. Tipo, mostrar pra onde vai voltar.

Moderador: E teve alguma coisa que você gostou?

Participante: Gostei da comparação lado a lado e da confirmação quando salva. E também daquele aviso quando os treinamentos não são compatíveis, porque ele explica o que tá errado.

Moderador: Tá ótimo, era isso. Valeu pela ajuda!

Participante: Imagina, espero ter ajudado, kkk.


### 4.1 Registro de observações do walkthrough

| Observação | Tela/ação | Evidência (fala simulada do participante) | Consequência para o design |
|---|---|---|---|
| O participante inicialmente tentou acessar a comparação diretamente, sem selecionar as execuções. | P02 — Acesso ao histórico e seleção de execuções. | "Acho que eu iria direto em comparação. Ué, mas eu tenho que escolher os treinamentos antes, né?" | Tornar mais clara a necessidade de selecionar duas execuções antes de iniciar uma comparação, oferecendo orientação na tela de comparação quando não houver seleções. |
| O contador de execuções selecionadas ajudou o participante a compreender a quantidade necessária para continuar. | P02 — Seleção das execuções EXEC-103 e EXEC-104. | "Pera, é pra marcar só dois? Ah, tá escrito ali embaixo, selecionados zero de dois. Beleza." | Manter o contador de seleções e destacar visualmente quando as duas execuções necessárias estiverem selecionadas. |
| A apresentação das métricas lado a lado facilitou a identificação de diferenças de desempenho. | P03 — Comparação das métricas. | "Nossa, mas olha aqui, o que tá mais rápido também cai mais. Então não é necessariamente melhor, né?" | Preservar a visualização comparativa, permitindo observar simultaneamente indicadores positivos e negativos. |
| As diferenças de configuração não estavam suficientemente claras para explicar as alterações de desempenho. | P03 — Consulta às diferenças de configuração. | "Só não entendi esse negócio de diferenças de configuração. Era pra aparecer o que mudou?" | Apresentar os parâmetros modificados, com os valores de cada execução, facilitando a identificação de possíveis relações com as mudanças observadas. |
| A separação entre diferenças observadas, hipóteses e ressalvas foi compreendida. | P04 — Registro de hipótese explicativa. | "Ah, beleza. Tem as diferenças observadas e aí eu escrevo o que acho que aconteceu." | Manter a organização dos campos, diferenciando resultados medidos de explicações ainda não comprovadas. |
| O termo técnico "baseline" gerou dúvida durante a avaliação. | P05 — Identificação da execução de referência. | "Baseline é o treinamento que eu tô usando pra comparar?" | Apresentar o termo como "Baseline (execução de referência)", mantendo a terminologia técnica com uma explicação complementar. |
| O gráfico de avaliação não permitia identificar claramente qual linha correspondia a cada execução. | P05 — Análise dos gráficos de desempenho. | "Aqui tem o gráfico, mas eu não tô entendendo qual linha é qual. Tem duas linhas e não tem uma legenda." | Adicionar uma legenda que identifique cada execução e seu respectivo traçado no gráfico. |
| O botão de retorno da evidência detalhada não correspondia ao contexto da avaliação. | P08 — Retorno da evidência para a avaliação. | "Esse botão tá escrito voltar à apresentação... Mas eu não tava apresentando nada." | Utilizar um botão de retorno contextual, identificando a tela de origem, como "Voltar à avaliação" ou "Voltar à reunião". |
| A confirmação de salvamento foi facilmente compreendida e transmitiu segurança. | P06 — Confirmação do registro. | "Ah, essa tá boa. Mostra que salvou mesmo. Eu gosto quando aparece isso, porque senão fico naquela dúvida se foi ou não." | Manter a confirmação explícita do salvamento, acompanhada dos identificadores das execuções e da conclusão registrada. |
| O aviso de incompatibilidade entre execuções foi compreendido e auxiliou a decisão do participante. | P11 e P12 — Seleção de baseline e aviso de incompatibilidade. | "Ah, entendi, porque é outra versão. Tem outras diferenças também. Eu acho que escolheria outro." | Manter a apresentação das incompatibilidades identificadas e oferecer uma opção clara para selecionar outra referência. |
| O participante considerou importante informar os riscos de continuar uma comparação com referência incompatível. | P12 — Opção de continuar com ressalvas. | "Talvez, se eu precisasse muito comparar esses dois. Mas aí teria que deixar bem claro que a comparação pode não ser justa." | Destacar visualmente as limitações da comparação e exigir o registro de uma ressalva quando o usuário decidir continuar. |
| O painel geral apresentou uma organização compreensível para consultar as informações iniciais. | P01 — Consulta à síntese dos últimos 30 dias. | "Ah, aqui já tem os últimos 30 dias. Tem velocidade, distância, quedas... Essa tela parece mais fácil." | Manter os indicadores principais agrupados e o período de análise visível. |
| O botão de navegação da reunião não deixava claro qual indicador seria apresentado em seguida. | P07 — Apresentação dos resultados. | "Só esse botão de próximo indicador que eu fiquei meio perdido. Próximo indicador qual?" | Identificar o indicador seguinte no próprio botão ou apresentar uma sequência visível dos indicadores da reunião. |
| O participante demonstrou preocupação com a possibilidade de perder o contexto ao consultar evidências durante a reunião. | P07 e P08 — Abertura de evidência e retorno à apresentação. | "Isso eu achei importante, porque imagina ter que escolher o período tudo de novo no meio da reunião. Ia ser chato." | Preservar o período, o indicador e o ponto anterior da apresentação durante a navegação entre as telas. |
| A tela de iniciar treinamento apresentou termos técnicos que podem dificultar sua utilização por pessoas menos familiarizadas com aprendizado por reforço. | P14 — Configuração de treinamento (exploratória). | "Learning rate, batch size, gamma... Essas coisas. Acho que quem trabalha com isso vai entender, mas eu teria medo de mudar alguma coisa errada." | Incluir explicações sobre os parâmetros e apresentar valores padrão para orientar sua configuração. |
| O participante demonstrou preocupação com o início imediato de um treinamento e com a falta de informações sobre seu andamento. | P14 — Ação de iniciar treinamento (exploratória). | "Eu esperaria aparecer uma confirmação antes, porque parece que demora bastante, né?" | Propor uma etapa de confirmação antes do início e um estado de acompanhamento com progresso, situação da execução e possíveis erros. |

## 5. Alterações após a simulação

As observações apresentadas na simulação foram utilizadas para identificar possíveis melhorias na organização das informações, na clareza dos controles e na continuidade da navegação. A tabela apresenta propostas de alteração que poderão ser incorporadas à próxima versão do protótipo após validação com um participante real.

| Antes | Problema | Depois (alteração proposta) | Justificativa |
|---|---|---|---|
| A tela de comparação pode ser acessada pelo menu mesmo sem duas execuções selecionadas, sem uma orientação específica sobre como iniciar a comparação. | O participante tentou acessar diretamente a comparação e somente depois percebeu que precisava selecionar os treinamentos no histórico. | Apresentar uma mensagem de orientação quando não houver duas execuções selecionadas, acompanhada de um botão "Selecionar execuções" que encaminhe ao histórico. | Facilitar o entendimento da sequência de ações e reduzir dúvidas durante o início da comparação. |
| A área de diferenças de configuração apresenta informações pouco detalhadas sobre as alterações realizadas entre os treinamentos. | O participante não conseguiu identificar quais parâmetros haviam sido modificados, dificultando a formulação de uma hipótese. | Apresentar uma tabela com os parâmetros, seus valores nas duas execuções e as diferenças identificadas. | Permitir que o usuário relacione os resultados observados às configurações utilizadas, sem assumir automaticamente uma relação causal. |
| A tela de avaliação utiliza apenas o termo "baseline" para identificar a referência. | O participante demonstrou dúvida sobre o significado do termo, apesar de compreender a finalidade da comparação. | Utilizar a identificação "Baseline (execução de referência)" e disponibilizar uma explicação breve sobre sua função. | Manter a terminologia técnica utilizada pela equipe e facilitar a compreensão por usuários com diferentes níveis de conhecimento. |
| Os gráficos apresentam diferentes linhas sem uma identificação visual suficientemente clara. | O participante não conseguiu distinguir com segurança os resultados da execução avaliada e da referência. | Acrescentar legendas com os identificadores das execuções e utilizar diferentes estilos de linha para representá-las. | Evitar interpretações incorretas das métricas e facilitar a identificação de tendências, melhorias e regressões. |
| A tela de evidências possui um botão fixo denominado "Voltar à apresentação". | O participante acessou a evidência pela tela de avaliação e ficou em dúvida sobre o destino do botão. | Adaptar o botão de retorno conforme a origem, utilizando "Voltar à avaliação" ou "Voltar à reunião". | Tornar a navegação previsível e permitir que o usuário retorne à atividade anterior sem perder seu contexto. |
| A seleção de uma referência incompatível apresenta riscos para a comparação, mas a continuidade com ressalvas precisa ser compreendida pelo usuário. | O participante demonstrou preocupação em continuar uma análise mesmo sabendo que as condições dos experimentos eram diferentes. | Destacar as incompatibilidades identificadas, explicar suas consequências e exigir uma ressalva quando o usuário optar por continuar. | Evitar conclusões equivocadas e registrar as limitações consideradas durante a análise. |
| O botão "Próximo indicador" não informa qual conteúdo será exibido em seguida. | O participante não conseguiu prever qual métrica seria apresentada ao avançar na reunião. | Substituir a descrição genérica por uma identificação contextual, como "Próximo: estabilidade", e indicar o indicador atual. | Facilitar a condução da reunião e melhorar a previsibilidade das ações disponíveis. |
| A navegação entre a reunião e a evidência detalhada depende do retorno à tela anterior. | O participante demonstrou preocupação com a possibilidade de precisar selecionar novamente o período e o indicador após consultar uma evidência. | Preservar o período, os indicadores e o ponto da apresentação durante a abertura de evidências, retornando ao estado anterior. | Reduzir retrabalho e evitar interrupções desnecessárias durante a comunicação dos resultados à equipe. |
| A tela de configuração de treinamento apresenta hiperparâmetros técnicos sem explicações complementares. | O participante demonstrou insegurança para modificar valores como learning rate, batch size e gamma. | Acrescentar descrições curtas, valores padrão e informações sobre a finalidade de cada parâmetro. | Facilitar a compreensão da configuração e reduzir a possibilidade de alterações realizadas sem entendimento de suas consequências. |
| A ação "Iniciar treinamento" aparece diretamente após o preenchimento das configurações. | O participante demonstrou receio de iniciar uma execução demorada sem revisar as informações. | Adicionar uma confirmação com resumo dos parâmetros antes da execução e propor uma tela posterior de acompanhamento do treinamento. | Permitir a revisão das configurações e fornecer feedback sobre o início e o andamento de uma operação potencialmente demorada. |


## Checklist

- [X] O protótipo cobre tarefas relevantes da Entrega 5.
- [X] Cada tela/estado pode ser justificado por uma tarefa, decisão ou informação necessária.
- [X] O projeto não criou dashboard/CRUD/login apenas para parecer “completo”.
- [X] Telas/estados estão numerados e navegáveis na documentação.
- [X] Há pelo menos uma simulação/walkthrough documentado.
- [X] Críticas não foram apenas listadas: geraram decisão de revisão.
- [X] O protótipo continua em baixa fidelidade; detalhes visuais não mascaram problemas de fluxo.

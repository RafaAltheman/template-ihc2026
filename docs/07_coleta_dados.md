# Entrega 7 — Coleta de dados, necessidades e aspectos éticos

**Data:** {{04/11/2026}}  
**Status:** 🟦 revisada após feedback

## Objetivo da atividade

Planejar dados necessários para compreender usuários e requisitos de IHC, escolher técnicas adequadas e documentar instrumentos de modo que a aplicação possa ser reproduzida por pessoas diferentes.

## Para escopos de IHC derivados de TCC técnico

Quando o usuário e a interface foram propostos pela disciplina, uma prioridade da coleta é investigar se esse **cenário de uso realmente faz sentido**. Não trate o exercício de comercialização da Entrega 1 como validação de mercado.

Perguntas úteis incluem:

- esse perfil realmente realiza a atividade imaginada?
- quais ferramentas usa hoje?
- quais informações consulta?
- quais decisões toma?
- que vocabulário utiliza?
- quais parâmetros compreende e quais deveriam ser abstraídos?
- precisa de dashboard, histórico, filtros, relatórios ou comparação? Por quê?
- quais erros são frequentes e quais são críticos?
- existem papéis/permissões diferentes?
- que resultados do algoritmo/modelo seriam úteis ou difíceis de interpretar?

Quando o acesso ao perfil profissional for difícil, discuta com o docente alternativas metodológicas (especialistas próximos, dados secundários, literatura, participantes proxy) e registre as limitações. **Não esconda a limitação da amostra.**

## Hipóteses e lacunas prioritárias herdadas da Entrega 1

As hipóteses foram recuperadas do arquivo `RASTREABILIDADE.md`, considerando seu estado atual e as evidências registradas nas entregas anteriores.

A hipótese H01a já foi fechada com base nas experiências da própria equipe durante os experimentos do TCC. Entretanto, ainda é necessário investigar se as mesmas dificuldades ocorrem em outras equipes de robótica, além de verificar a utilidade da solução proposta e a familiaridade dos usuários com as informações técnicas apresentadas.

| ID | Hipótese/lacuna | Evidência atual | Decisão que depende da resposta | Prioridade |
|---|---|---|---|---|
| H01b | Outras equipes de robótica têm dificuldade em reunir e comparar diferentes métricas e informações de desempenho dos robôs ao longo de testes e competições. | A dificuldade foi identificada na experiência da própria equipe e documentada nas Entregas 1 e 4. A Entrega 3 incorporou essa possibilidade às necessidades das personas, mas ainda não houve validação direta com usuários externos. | Verificar se a centralização das informações atende a uma dificuldade real de outras equipes e quais atividades de consulta e comparação devem ser priorizadas. | Alta |
| H02 | Centralizar e comparar resultados de diferentes testes, versões ou robôs ajudaria as equipes a identificar melhorias, pioras e limitações de desempenho. | A Entrega 2 identificou padrões de visualização, histórico e comparação em ferramentas semelhantes. As Entregas 3, 4, 5 e 6 desenvolveram personas, cenários, tarefas e protótipos relacionados à hipótese, mas sua utilidade ainda não foi validada diretamente com usuários. | Definir a organização das métricas, a necessidade de comparação lado a lado, os mecanismos de histórico e a apresentação das informações necessárias à tomada de decisão. | Alta |
| H03 | Os usuários possuem familiaridade suficiente com métricas e vocabulário técnico de robótica para utilizar uma interface de análise de desempenho. | A Entrega 3 considerou familiaridade técnica na construção das personas. A Entrega 2 analisou ferramentas que apresentam métricas especializadas, mas o conhecimento dos usuários ainda não foi investigado diretamente. | Definir a terminologia utilizada na interface, a necessidade de legendas, explicações de indicadores, identificação de unidades e diferentes níveis de detalhamento técnico. | Alta |




## Parte A — necessidades e requisitos de IHC

### A01 — Letizia Lowatzki Baptistella

**Autor(a):** Letizia Lowatzki Baptistella — 22.125.063-2

**Tarefa relacionada:** T01 — Avaliar se um treinamento melhorou o desempenho do robô.

**Persona/cenário:** P01 — Rafael Martins / C01.

#### Que dados coletar?

| Dado/informação | Hipótese/lacuna relacionada | Por que é necessário | Qual decisão de design pode afetar |
|---|---|---|---|
| Frequência com que o usuário avalia resultados e compara treinamentos. | H01b, H02 | Verificar se essa atividade é recorrente e relevante para os integrantes de outras equipes de robótica. | Prioridade da funcionalidade de avaliação e do acesso ao histórico. |
| Métricas utilizadas para avaliar o desempenho do robô. | H02, H03 | Identificar quais indicadores são realmente utilizados na análise e quais são considerados mais importantes. | Seleção de métricas, organização dos gráficos e apresentação dos resultados. |
| Critérios utilizados para determinar se um treinamento apresentou melhoria. | H02 | Compreender como o usuário interpreta ganhos e regressões em diferentes indicadores. | Organização da comparação e opções de classificação do resultado. |
| Procedimento utilizado para selecionar uma execução de referência (baseline). | H02, H03 | Verificar quais condições tornam duas execuções comparáveis e quais diferenças comprometem a análise. | Identificação da execução de referência e apresentação de diferenças relevantes para a comparação. |
| Utilização de vídeos, simulações e outras evidências comportamentais. | H02 | Investigar se os indicadores numéricos são suficientes ou se o usuário precisa observar o comportamento do robô. | Necessidade de acesso a evidências visuais durante a avaliação. |
| Familiaridade com termos técnicos e parâmetros dos experimentos. | H03 | Identificar quais conceitos são compreendidos e quais precisam de explicações adicionais. | Terminologia, legendas, unidades e ajuda contextual. |
| Ferramentas e fontes utilizadas atualmente para consultar resultados. | H01b, H02 | Verificar se as informações estão distribuídas entre diferentes ferramentas e como são recuperadas. | Organização do histórico e apresentação integrada das informações. |

#### De quem coletar?

| Perfil/stakeholder | Critério de inclusão | Relação com persona/público |
|---|---|---|
| Estudantes integrantes de equipes de robótica humanoide. | Participar da análise de treinamentos, testes ou experimentos com robôs. | Representam o perfil prioritário da persona P01. |
| Integrantes com menor experiência em análise de resultados. | Participar de atividades de acompanhamento, mesmo sem realizar os treinamentos diretamente. | Permitem investigar diferenças de familiaridade técnica relacionadas à H03. |

#### Aspectos éticos

A coleta será realizada de maneira voluntária, após a apresentação dos objetivos da pesquisa e das condições de participação. Os participantes poderão recusar perguntas ou interromper sua participação a qualquer momento.

O questionário não exigirá nome, matrícula, telefone ou outras informações pessoais que não sejam necessárias para a investigação. Serão coletados apenas dados relacionados às atividades, à experiência com ferramentas e às dificuldades de interpretação dos resultados.

Como os participantes podem fazer parte de equipes que desenvolvem projetos técnicos e participam de competições, será solicitado que não compartilhem informações confidenciais, códigos privados, credenciais ou detalhes estratégicos.

As respostas serão identificadas por códigos, como Q01 e Q02, e armazenadas em ambiente de acesso restrito às integrantes. Na documentação serão utilizadas apenas informações agregadas e respostas anonimizadas. Os registros brutos serão descartados após o prazo estabelecido para o estudo, respeitando eventuais orientações institucionais.

### A02 — Manuella Filipe Peres

**Autor(a):** Manuella Filipe Peres — 22.224.029-3

**Tarefa relacionada:** T02 — Localizar e comparar execuções anteriores para explicar diferenças de desempenho.

**Persona/cenário:** P02 — Marina Oliveira / C02.

#### Que dados coletar?

| Dado/informação | Hipótese/lacuna relacionada | Por que é necessário | Qual decisão de design pode afetar |
|---|---|---|---|
| Processo utilizado para localizar resultados de experimentos anteriores. | H01b, H02 | Compreender como os usuários recuperam informações e quais dificuldades encontram nessa atividade. | Busca por identificador, filtros e organização do histórico. |
| Ferramentas utilizadas para armazenar e consultar resultados e configurações. | H01b, H02 | Identificar se os dados ficam distribuídos entre arquivos e sistemas diferentes. | Estrutura dos registros e apresentação integrada dos resultados. |
| Informações necessárias para identificar corretamente uma execução. | H02 | Verificar quais metadados permitem confirmar que o resultado encontrado corresponde ao experimento desejado. | Exibição de ID, data, versão, ambiente e parâmetros. |
| Critérios utilizados para comparar diferentes execuções. | H02, H03 | Identificar quais condições tornam os experimentos comparáveis e quais diferenças comprometem a análise. | Apresentação de parâmetros e sinalização de diferenças que podem limitar a comparação. |
| Dificuldades para recuperar configurações e resultados antigos. | H01b, H02 | Investigar problemas de rastreabilidade e situações em que informações anteriores não são encontradas. | Filtros, preservação de seleções e detalhamento das execuções. |
| Forma como hipóteses e conclusões são registradas após uma comparação. | H02 | Entender se os usuários precisam documentar as interpretações e disponibilizá-las para outras pessoas. | Campos de justificativa, ressalvas e confirmação de salvamento. |
| Conhecimento dos termos utilizados em métricas e configurações. | H03 | Verificar se o vocabulário técnico é compreendido pelos diferentes integrantes. | Nomenclatura e explicações das informações exibidas. |

#### De quem coletar?

| Perfil/stakeholder | Critério de inclusão | Relação com persona/público |
|---|---|---|
| Pesquisadores de robótica que realizam experimentos. | Ter experiência na comparação de resultados ou configurações de treinamentos anteriores. | Representam o perfil da persona P02. |
| Integrantes responsáveis por registrar parâmetros e resultados. | Participar da organização do histórico ou da documentação de experimentos. | Conhecem as dificuldades relacionadas à rastreabilidade. |

#### Aspectos éticos

Antes da entrevista, os participantes serão informados sobre os objetivos da pesquisa e a utilização das respostas.

Caso a entrevista seja gravada, será solicitado consentimento específico para o áudio. Caso o participante não autorize a gravação, poderão ser realizadas apenas anotações, mediante seu consentimento.

Não serão solicitados arquivos privados, códigos-fonte, senhas ou dados confidenciais das equipes.

Os registros serão armazenados em ambiente privado, com acesso restrito à equipe de pesquisa, e posteriormente descartados conforme o prazo informado.


### A03 — Rafaela Altheman de Campos

**Autor(a):** Rafaela Altheman de Campos — 22.125.062-4

**Tarefa relacionada:** T03 — Consultar uma síntese do desempenho e comunicar à equipe os pontos que precisam de investigação.

**Persona/cenário:** P03 — Carlos Almeida / C03.

#### Que dados coletar?

| Dado/informação | Hipótese/lacuna relacionada | Por que é necessário | Qual decisão de design pode afetar |
|---|---|---|---|
| Procedimento utilizado para preparar uma apresentação dos resultados de treinamentos. | H01b, H02 | Compreender como os usuários organizam informações antes de reuniões técnicas. | Organização do painel de desempenho e seleção de períodos. |
| Indicadores e métricas priorizados durante as reuniões. | H02, H03 | Identificar quais informações são consideradas relevantes para comunicar a evolução do robô. | Escolha dos indicadores e organização dos gráficos. |
| Ferramentas utilizadas para reunir e apresentar resultados. | H01b, H02 | Investigar se a preparação exige consultar diferentes arquivos ou sistemas. | Necessidade de visualização consolidada dos resultados. |
| Forma de interpretar tendências e identificar problemas de desempenho. | H02, H03 | Compreender como os participantes reconhecem melhorias, regressões e pontos que precisam de investigação. | Organização temporal das métricas e identificação de pontos de atenção. |
| Situações em que informações complementares precisam ser consultadas durante uma apresentação. | H02 | Investigar a necessidade de acessar evidências detalhadas sem interromper o acompanhamento dos resultados. | Navegação entre o painel, a apresentação e as evidências. |
| Dificuldades para recuperar o contexto após consultar informações detalhadas. | H01b, H02 | Verificar se a alternância entre informações compromete a continuidade das atividades. | Preservação do período, indicador e estado da navegação. |
| Forma como os resultados discutidos orientam as próximas investigações. | H02 | Compreender como a análise das informações contribui para as decisões da equipe. | Organização dos pontos de atenção e apresentação das conclusões, mantendo a decisão com os usuários. |

#### De quem coletar?

| Perfil/stakeholder | Critério de inclusão | Relação com persona/público |
|---|---|---|
| Professores e orientadores que acompanham projetos de robótica. | Participar da análise ou discussão dos resultados de experimentos. | Perfil próximo da persona P03. |
| Líderes técnicos de equipes de robótica. | Participar de reuniões de acompanhamento e decisões relacionadas ao desempenho do robô. | Permitem investigar o uso de indicadores na comunicação técnica. |
| Estudantes responsáveis por apresentar resultados experimentais. | Preparar ou apresentar gráficos, relatórios e comparações para outros integrantes. | Permitem observar o processo de comunicação e suas dificuldades. |

#### Aspectos éticos

A observação será realizada somente após o consentimento do participante e, caso envolva outras pessoas durante uma reunião, também será solicitada autorização dos envolvidos.

O objetivo será compreender a realização das atividades e as dificuldades de interação, não avaliar o desempenho pessoal dos participantes. Serão registradas ações como consultar métricas, alternar ferramentas, abrir evidências e retornar a uma análise.

Não será obrigatória a gravação de áudio ou vídeo. Caso seja necessária, será solicitada autorização específica antes da coleta.

Também serão evitados registros de informações confidenciais de equipes, resultados ainda não divulgados, códigos privados ou dados pessoais de terceiros.

---


## Parte B — ferramentas de coleta

Cada integrante será responsável pela elaboração de um instrumento de coleta diferente, conforme as técnicas apresentadas nas aulas de Identificação de Necessidades dos Usuários e Requisitos de IHC.

### Instrumento I01 — Questionário estruturado sobre análise de resultados

**Autor(a):** Letizia Lowatzki Baptistella — 22.125.063-2

**Técnica:** Questionário com perguntas abertas e fechadas.

**Objetivo:** Investigar como integrantes de equipes de robótica analisam resultados de treinamentos, quais métricas utilizam, quais dificuldades encontram para comparar execuções e como compreendem os termos técnicos relacionados ao desempenho do robô.

**Público:** Estudantes, pesquisadores e integrantes de equipes de robótica que participam da execução, acompanhamento ou análise de experimentos.

**Hipóteses relacionadas:** H01b, H02 e H03.

**Duração estimada:** 8 a 12 minutos.

#### Procedimento padronizado de aplicação

1. **Preparação:** elaborar o questionário em uma ferramenta digital, como Google Forms, mantendo a ordem e as alternativas definidas neste documento. Realizar uma verificação prévia para identificar perguntas ambíguas ou problemas de compreensão.
2. **Apresentação e consentimento:** apresentar os objetivos da pesquisa, informar que a participação é voluntária e solicitar o consentimento antes de iniciar o preenchimento.
3. **Aplicação:** disponibilizar o questionário aos participantes que se enquadrem no público definido. As perguntas deverão ser apresentadas sem explicações que possam induzir determinadas respostas.
4. **Encerramento:** agradecer pela participação e informar que as respostas serão utilizadas exclusivamente para compreender as necessidades dos usuários no contexto acadêmico.
5. **Armazenamento e anonimização:** exportar as respostas e armazená-las em ambiente privado, identificadas por códigos. Não coletar automaticamente e-mails nem dados pessoais desnecessários.

#### Instrumento — Questionário

link para Google Forms: https://forms.gle/dz8nd6X6n1UnEjFR8 

**Texto de apresentação:**

Este questionário faz parte de uma atividade acadêmica da disciplina de Interação Humano-Computador. Nosso objetivo é compreender como equipes de robótica consultam, interpretam e comparam resultados de treinamentos e experimentos.

O preenchimento tem duração estimada de 8 a 12 minutos. Algumas perguntas podem exigir que você relembre experiências ou dificuldades técnicas, o que pode gerar um pequeno desconforto. Caso não queira responder alguma questão não obrigatória, poderá deixá-la em branco.

Não existem respostas certas ou erradas. A participação é voluntária, e você pode interromper o preenchimento a qualquer momento, sem qualquer prejuízo.

As respostas serão utilizadas apenas para fins acadêmicos, sem identificação pessoal. Não solicitamos informações confidenciais das equipes.

Ao continuar, você poderá indicar se concorda ou não em participar da pesquisa.


**Q00 — Consentimento**

Você concorda em participar desta pesquisa?

- ( ) Sim.
- ( ) Não.

Caso a resposta seja "Não", o questionário deverá ser encerrado.

**Q01 — Experiência com robótica**

Qual alternativa descreve melhor sua experiência?

- ( ) Participo atualmente de uma equipe de robótica.
- ( ) Já participei de uma equipe de robótica.
- ( ) Trabalho ou estudo robótica em outro contexto.
- ( ) Tenho experiência com análise experimental de outra área.
- ( ) Não tenho experiência com essas atividades.

**Q02 — Atividades realizadas**

Com quais atividades você já trabalhou? (Marque todas as opções aplicáveis.)

- [ ] Configuração ou execução de treinamentos e testes.
- [ ] Consulta de métricas de desempenho.
- [ ] Comparação de resultados de experimentos.
- [ ] Observação de vídeos ou simulações.
- [ ] Apresentação de resultados para outras pessoas.
- [ ] Registro de conclusões ou hipóteses.
- [ ] Nenhuma dessas atividades.
- [ ] Outra: __________.

**Q03 — Frequência de análise**

Com que frequência você consulta resultados de treinamentos ou testes?

- ( ) Diariamente.
- ( ) Algumas vezes por semana.
- ( ) Algumas vezes por mês.
- ( ) Menos de uma vez por mês.
- ( ) Nunca.

**Q04 — Ferramentas utilizadas**

Quais ferramentas você utiliza para consultar resultados?

- [ ] Terminal e arquivos de log.
- [ ] Arquivos CSV, JSON ou relatórios.
- [ ] Planilhas.
- [ ] Gráficos produzidos por scripts.
- [ ] Simuladores ou vídeos.
- [ ] Dashboards ou ferramentas de monitoramento.
- [ ] Não consulto resultados.
- [ ] Outra: __________.

**Q05 — Informações utilizadas na avaliação**

Quais informações você utiliza ou considera necessárias para avaliar o desempenho de um robô?

- [ ] Recompensa do treinamento.
- [ ] Velocidade média.
- [ ] Distância percorrida.
- [ ] Taxa de quedas.
- [ ] Estabilidade.
- [ ] Desempenho em situações de jogo.
- [ ] Comportamento observado em vídeo ou simulação.
- [ ] Parâmetros e versão do experimento.
- [ ] Não sei.
- [ ] Outra: __________.

**Q06 — Dificuldades na avaliação**

Quando você precisa avaliar se um experimento apresentou melhoria, qual situação ocorre com maior frequência?

- ( ) Não encontro as informações necessárias.
- ( ) Encontro os dados, mas tenho dificuldade para compará-los.
- ( ) Os indicadores apresentam resultados conflitantes.
- ( ) Não conheço o significado de algumas métricas.
- ( ) Não costumo ter dificuldades.
- ( ) Não realizo essa atividade.
- ( ) Outra: __________.

**Q07 — Recuperação de experimentos anteriores**

Você já precisou recuperar um resultado antigo para compará-lo com um experimento recente?

- ( ) Sim, frequentemente.
- ( ) Sim, algumas vezes.
- ( ) Não.
- ( ) Não me lembro.

**Q08 — Escolha de referência**

Quando precisa comparar dois treinamentos, como escolhe qual execução será utilizada como referência?

*Resposta aberta.*

**Q09 — Interpretação de métricas**

Imagine que um treinamento aumentou a velocidade média de 0,28 m/s para 0,32 m/s, mas a taxa de quedas passou de 8% para 12%.

Quais informações adicionais você consultaria para decidir se houve uma melhoria no desempenho?

*Resposta aberta.*

**Q10 — Informações ausentes**

O que você costuma fazer quando faltam dados importantes para comparar experimentos?

- [ ] Consulto outros arquivos ou ferramentas.
- [ ] Solicito informações para outro integrante.
- [ ] Repito ou planejo outro teste.
- [ ] Registro a limitação e evito uma conclusão definitiva.
- [ ] Continuo a análise somente com os dados disponíveis.
- [ ] Nunca passei por essa situação.
- [ ] Outra: __________.

**Q11 — Familiaridade com termos técnicos**

Para cada termo abaixo, indique seu nível de familiaridade.

| Termo | Conheço e utilizo | Conheço parcialmente | Não conheço |
|---|---|---|---|
| Baseline | ( ) | ( ) | ( ) |
| Recompensa | ( ) | ( ) | ( ) |
| Taxa de quedas | ( ) | ( ) | ( ) |
| Estabilidade | ( ) | ( ) | ( ) |
| Learning rate | ( ) | ( ) | ( ) |
| Timesteps | ( ) | ( ) | ( ) |
| Batch size | ( ) | ( ) | ( ) |

**Q12 — Apresentação das informações**

Ao comparar dois treinamentos, qual forma de apresentação você preferiria utilizar?

- ( ) Tabela com valores lado a lado.
- ( ) Gráficos de evolução.
- ( ) Vídeos ou registros de simulação.
- ( ) Combinação de tabelas, gráficos e registros visuais.
- ( ) Não sei.
- ( ) Outra: __________.

**Q13 — Fontes de consulta dos resultados**

Onde você costuma consultar ou recuperar resultados de treinamentos? (Marque todas as opções aplicáveis.)

- [ ] Arquivos locais ou compartilhados.
- [ ] Terminal e logs.
- [ ] Planilhas.
- [ ] Ferramentas de acompanhamento de experimentos.
- [ ] Relatórios ou gráficos exportados.
- [ ] Não consulto resultados.
- [ ] Outra: __________.

**Q14 — Necessidades adicionais**

Existe alguma dificuldade relacionada à consulta, interpretação ou comparação de resultados de treinamentos que não foi abordada neste questionário?

*Resposta aberta.*

#### Como os dados serão analisados

As respostas fechadas serão organizadas por frequência e distribuição das alternativas selecionadas, permitindo identificar padrões relacionados às atividades realizadas, às ferramentas utilizadas e às dificuldades de interpretação.

As perguntas abertas serão analisadas por agrupamento temático, considerando problemas mencionados, necessidades de informação, critérios de avaliação e sugestões apresentadas.

A hipótese H01b será investigada pelas dificuldades relatadas na recuperação e comparação de informações. A H02 será analisada a partir das práticas e necessidades de visualização e comparação. A H03 será examinada por meio das respostas relacionadas ao conhecimento dos termos técnicos.

A análise também considerará diferenças entre participantes com maior e menor experiência, sem pressupor que os resultados de uma amostra pequena representem todas as equipes de robótica.

---

### Instrumento I02 — Entrevista semiestruturada

**Autor(a):** Manuella Filipe Peres — 22.224.029-3

**Técnica:** Entrevista semiestruturada.

**Objetivo:** Compreender como pesquisadores e integrantes de equipes de robótica recuperam resultados anteriores, comparam experimentos e interpretam diferenças de desempenho, identificando dificuldades e informações necessárias para realizar essas atividades.

**Público:** Pesquisadores e integrantes de equipes de robótica que realizam ou acompanham experimentos e análises de resultados.

**Hipóteses relacionadas:** H01b, H02 e H03.

**Duração estimada:** 20 a 30 minutos.

#### Procedimento padronizado de aplicação

1. Preparação: selecionar participantes que tenham experiência com experimentos ou análise de resultados. Preparar o roteiro, os materiais de anotação e, quando autorizado, um dispositivo para gravação de áudio. 
2. Apresentação e consentimento: explicar o objetivo da entrevista e informar que a participação é voluntária. Solicitar autorização específica para gravação, deixando claro que a pessoa pode recusar.
3. Aplicação: conduzir a conversa utilizando as perguntas do roteiro. O entrevistador poderá fazer perguntas adicionais para esclarecer respostas, desde que não induzam o participante.
4. Encerramento: permitir comentários adicionais, agradecer pela colaboração e informar como as respostas serão utilizadas.
5. Armazenamento e anonimização: transcrever as respostas, substituir nomes e informações identificáveis por códigos e armazenar os registros em ambiente privado.

#### Instrumento — roteiro completo

**Abertura da entrevista:**

"Queremos entender como você trabalha com os resultados dos experimentos de robótica, principalmente quando precisa encontrar treinamentos anteriores e comparar o desempenho.

Esta entrevista terá duração aproximada de 20 a 30 minutos. Não estamos avaliando seu conhecimento. A ideia é compreender como essas atividades acontecem na prática, quais ferramentas você utiliza e quais dificuldades aparecem.

Algumas perguntas podem fazer você lembrar de situações difíceis ou desconfortáveis no trabalho. Sua participação é voluntária e você pode deixar de responder qualquer pergunta ou encerrar a entrevista a qualquer momento, sem qualquer prejuízo.

Suas respostas serão utilizadas exclusivamente para fins acadêmicos, preservando sua identidade. Não solicitaremos informações confidenciais, senhas ou códigos privados.

Caso seja necessário gravar o áudio, solicitaremos sua autorização separadamente. Você poderá participar mesmo que não autorize a gravação.

Você concorda em participar da entrevista?"

**Bloco 1 — Contexto e experiência**

**E01.** Qual é o seu papel na equipe ou no projeto de robótica? Quais atividades você realiza com mais frequência?

**E02.** Em quais situações você precisa consultar resultados de treinamentos ou experimentos anteriores?

**E03.** Quais ferramentas você utiliza para acessar métricas, parâmetros e registros de treinamentos?

**Bloco 2 — Localização e comparação**

**E04.** Quando precisa encontrar uma execução antiga, como costuma realizar essa busca?

**E05.** Quais informações você utiliza para confirmar que encontrou o experimento correto?

**E06.** Quando precisa comparar duas execuções, quais informações considera indispensáveis para que a comparação seja válida?

**E07.** Você já teve dificuldade para recuperar parâmetros ou resultados de um treinamento anterior? Como resolveu a situação?

**Bloco 3 — Interpretação dos resultados**

**E08.** Quando duas métricas apresentam resultados diferentes, por exemplo, maior velocidade e menor estabilidade, como você decide se houve melhoria?

**E09.** Como você diferencia uma diferença realmente observada nos resultados de uma possível explicação para essa diferença?

**E10.** Depois de comparar experimentos, como costuma registrar suas conclusões, hipóteses ou ressalvas?

**Bloco 4 — Necessidades e linguagem**

**E11.** Se pudesse modificar alguma etapa do processo atual de consulta ou comparação dos resultados, qual modificaria? Por quê?

**E12.** Existem métricas, parâmetros ou termos técnicos que geram dúvidas? Quais?

**E13.** Quando precisa recuperar resultados e parâmetros de uma execução, quais ferramentas ou fontes consulta? Como lida com informações armazenadas em locais diferentes?

**Encerramento:**

"Existe alguma dificuldade ou necessidade relacionada à análise de resultados de experimentos que você considera importante e que não perguntamos?"

#### Como os dados serão analisados

As entrevistas serão transcritas e analisadas por meio de categorização temática.

Os relatos serão agrupados em temas como busca de execuções, dificuldades de rastreabilidade, comparação de métricas, recuperação de parâmetros, interpretação dos resultados e familiaridade com termos técnicos.

A análise buscará identificar situações recorrentes e exemplos concretos relacionados às hipóteses H01b, H02 e H03.

Os resultados serão relacionados às tarefas T01 e T02 da Entrega 5, permitindo verificar se os fluxos de avaliação, histórico e comparação correspondem às necessidades descritas pelos participantes.

As respostas também poderão indicar que determinadas funcionalidades não são necessárias ou que os processos atuais já atendem às necessidades dos usuários. Essas evidências serão consideradas para refinar ou refutar as hipóteses existentes.

---

### Instrumento I03 — Estudo de Campo


**Autor(a):** Rafaela Altheman de Campos — 22.125.062-4

**Técnica:** Estudo de Campo, por meio de observação guiada e registro estruturado das atividades realizadas pelo participante.

**Objetivo:** Observar como integrantes de equipes de robótica consultam, interpretam e apresentam resultados de experimentos, identificando as informações utilizadas, as dificuldades encontradas e as estratégias adotadas para recuperar dados e comunicar conclusões.

**Público:** Professores, orientadores, pesquisadores, líderes técnicos e estudantes responsáveis por acompanhar ou apresentar resultados de experimentos de robótica.

**Hipóteses relacionadas:** H01b, H02 e H03.

**Duração estimada:** 20 a 40 minutos.

#### Procedimento padronizado de aplicação

1. **Preparação:** selecionar um participante que realize atividades de acompanhamento ou apresentação de resultados experimentais. Combinar a observação em um contexto adequado (reunião semanal da equipe de robótica, por exemplo) e preparar a ficha de registro.
2. **Apresentação e consentimento:** antes de iniciar, o observador apresentará ao participante o seguinte texto: "Esta atividade faz parte de uma pesquisa acadêmica de Interação Humano-Computador. Queremos compreender como você consulta, interpreta e apresenta resultados de experimentos. A observação terá duração aproximada de 20 a 40 minutos. Não estamos avaliando seu desempenho pessoal. Você poderá sentir algum desconforto ao comentar dificuldades do seu trabalho, mas poderá recusar perguntas, solicitar uma pausa ou encerrar sua participação a qualquer momento, sem qualquer prejuízo. Não solicitaremos senhas, códigos privados ou informações confidenciais. Sua identidade será preservada e os registros serão utilizados apenas para fins acadêmicos. Você concorda em participar?" A observação somente será iniciada após o consentimento. Caso a atividade envolva uma reunião com outras pessoas, também será solicitada autorização dos demais envolvidos.
3. **Aplicação:** acompanhar a atividade realizada pelo participante, observando como ele seleciona informações, consulta métricas, interpreta resultados e busca evidências adicionais. O observador deverá evitar interferir na execução da tarefa.
4. **Encerramento:** realizar perguntas breves para esclarecer pontos observados e permitir comentários adicionais do participante.
5. **Armazenamento e anonimização:** organizar as notas por códigos, retirar informações identificáveis e manter os registros em ambiente de acesso restrito.

#### Instrumento — protocolo de observação

**Identificação da sessão**

- Código do participante: O___
- Data: __/__/__
- Contexto da observação: __________________
- Atividade observada: __________________

**Aspectos a observar**

| Item | Aspecto observado | O que registrar |
|---|---|---|
| O01 | Início da atividade | O que motivou a necessidade de consultar ou apresentar resultados. |
| O02 | Seleção das informações | Como o participante escolhe períodos, execuções e indicadores relevantes. |
| O03 | Consulta de resultados | Quais ferramentas, arquivos, gráficos ou relatórios são utilizados. |
| O04 | Interpretação | Como o participante identifica tendências, melhorias, regressões e pontos de atenção. |
| O05 | Consulta de evidências | Em quais situações procura informações adicionais ou detalhes de uma execução. |
| O06 | Navegação entre informações | Se precisa alternar ferramentas, repetir buscas ou recuperar informações anteriores. |
| O07 | Comunicação | Como organiza e explica os resultados para outras pessoas. |
| O08 | Encaminhamentos | Como os resultados são utilizados para discutir possíveis investigações futuras. |
| O09 | Dificuldades | Erros, dúvidas, interrupções, informações ausentes ou estratégias de recuperação. |

**Ficha para registro durante a observação**

| Momento | Ação observada | Informação/ferramenta consultada | Dificuldade identificada | 
|---|---|---|---|
| 00:00 | A preencher | A preencher | A preencher |
| ... | ... | ... | ... |

**Perguntas de esclarecimento após a observação**

**O01.** Qual era o principal objetivo da atividade realizada?

**O02.** Quais informações você considerou mais importantes durante a análise?

**O03.** Houve algum momento em que precisou procurar informações adicionais? Por quê?

**O04.** Como decide quais resultados devem ser apresentados ou discutidos com a equipe?

**O05.** Quando precisa consultar uma informação detalhada, como retorna ao ponto anterior da análise ou apresentação?

**O06.** Existe alguma etapa desse processo que você considera desnecessariamente demorada ou difícil?

#### Como os dados serão analisados

As observações serão organizadas em uma sequência cronológica das ações realizadas pelo participante.

Serão identificados os principais passos da atividade, as ferramentas consultadas, as dificuldades encontradas e as estratégias utilizadas para recuperar informações.

Os registros permitirão investigar se os participantes precisam reunir resultados de diferentes fontes, contribuindo para H01b, e se a visualização e comparação das informações auxiliam a interpretação e comunicação dos resultados, contribuindo para H02.

A familiaridade demonstrada com indicadores e terminologias também poderá fornecer evidências relacionadas à H03.

Os resultados serão relacionados à tarefa T03 da Entrega 5, principalmente à consulta de uma síntese do desempenho, à identificação de pontos que precisam de investigação e à comunicação das informações durante reuniões técnicas.

---

## Síntese

A proposta de coleta de dados foi estruturada a partir das hipóteses H01b, H02 e H03, registradas na Entrega 1 e mantidas abertas no arquivo `RASTREABILIDADE.md`.

As três técnicas selecionadas procuram investigar diferentes aspectos das atividades realizadas por integrantes de equipes de robótica humanoide.

O questionário busca identificar padrões relacionados à frequência de análise, às ferramentas utilizadas, às dificuldades de comparação e à familiaridade com métricas técnicas.

A entrevista semiestruturada permite aprofundar a compreensão dos procedimentos utilizados para localizar execuções anteriores, recuperar configurações, comparar resultados e registrar conclusões.

O Estudo de Campo, realizado por meio de observação guiada, pretende identificar como as informações são consultadas, interpretadas e comunicadas em situações de trabalho. A técnica permitirá registrar as ações e dificuldades observadas durante a atividade, sem interferência direta do pesquisador, complementando os registros com perguntas de esclarecimento ao final.

O conjunto dos instrumentos busca verificar se o cenário de uso proposto pela disciplina corresponde a necessidades reais, sem pressupor que as funcionalidades inicialmente desenhadas sejam necessariamente adequadas.

| Hipótese | Dados que serão utilizados | Possíveis decisões após a análise |
|---|---|---|
| **H01b** | Ferramentas utilizadas, frequência de recuperação de resultados, dificuldades de localização e comparação e situações observadas durante as atividades. | Sustentar a hipótese caso as dificuldades sejam identificadas em outras equipes; refutar ou refinar caso não sejam observadas ou ocorram apenas em determinados contextos. |
| **H02** | Critérios de comparação, informações consideradas relevantes, dificuldades na interpretação de métricas e necessidade de reunir resultados de diferentes execuções. | Sustentar, refutar ou refinar a necessidade de centralização e comparação de informações, ajustando as funcionalidades priorizadas. |
| **H03** | Familiaridade com métricas e parâmetros, interpretação de termos técnicos e dificuldades demonstradas ou relatadas durante a análise. | Definir se a interface pode utilizar terminologia especializada diretamente ou se precisa oferecer explicações, legendas e diferentes níveis de detalhamento. |


## Checklist

- [x] Hipóteses prioritárias da Entrega 1 e seus estados na rastreabilidade foram revisitados.
- [x] A coleta investiga a plausibilidade dos usuários, das tarefas e dos contextos adotados.
- [x] As perguntas não pressupõem que dashboards, históricos ou outras funcionalidades sejam necessários.
- [x] Cada dado a coletar está relacionado às hipóteses existentes.
- [x] A Parte A identifica dados e perfis específicos de coleta.
- [x] Os aspectos éticos foram contextualizados para o projeto.
- [x] Foi definida uma técnica diferente por integrante.
- [x] O questionário está incluído entre as técnicas.
- [x] Cada instrumento apresenta objetivo, público, procedimento e conteúdo completo.
- [x] As perguntas foram elaboradas para evitar indução e coleta desnecessária de informações pessoais.
- [x] Está definido como os dados serão analisados e utilizados nas decisões de design.

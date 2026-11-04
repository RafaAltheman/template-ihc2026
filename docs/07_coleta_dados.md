# Entrega 7 — Coleta de dados, necessidades e aspectos éticos

**Data:** {{04/11/2026}}  
**Status:** 🟨 em andamento

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

Antes de decidir “que dados coletar”, retome os itens `[H]` e `[?]` da Entrega 1 e o registro de hipóteses em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md). A coleta deve responder perguntas reais do projeto, e não apenas produzir um formulário porque a técnica foi solicitada.

## Hipóteses e lacunas prioritárias herdadas da Entrega 1

A numeração abaixo mantém a adotada na seção 10 da Entrega 1. As evidências existentes são principalmente a experiência da própria equipe, os cenários elaborados e a análise de interfaces análogas; elas ainda não representam uma validação com outras equipes de robótica.


## Hipóteses e lacunas prioritárias herdadas da Entrega 1

As hipóteses foram recuperadas do arquivo `RASTREABILIDADE.md`, considerando seu estado atual e as evidências registradas nas entregas anteriores.

A hipótese H01a já foi fechada com base nas experiências da própria equipe durante os experimentos do TCC. Entretanto, ainda é necessário investigar se as mesmas dificuldades ocorrem em outras equipes de robótica, além de verificar a utilidade da solução proposta e a familiaridade dos usuários com as informações técnicas apresentadas.

| ID | Hipótese/lacuna | Evidência atual | Decisão que depende da resposta | Prioridade |
|---|---|---|---|---|
| H01b | Outras equipes de robótica têm dificuldade em reunir e comparar diferentes métricas e informações de desempenho dos robôs ao longo de testes e competições. | A dificuldade foi identificada na experiência da própria equipe e documentada nas Entregas 1 e 4. A Entrega 3 incorporou essa possibilidade às necessidades das personas, mas ainda não houve validação direta com usuários externos. | Verificar se a centralização das informações atende a uma dificuldade real de outras equipes e quais atividades de consulta e comparação devem ser priorizadas. | Alta |
| H02 | Centralizar e comparar resultados de diferentes testes, versões ou robôs ajudaria as equipes a identificar melhorias, pioras e limitações de desempenho. | A Entrega 2 identificou padrões de visualização, histórico e comparação em ferramentas semelhantes. As Entregas 3, 4, 5 e 6 desenvolveram personas, cenários, tarefas e protótipos relacionados à hipótese, mas sua utilidade ainda não foi validada diretamente com usuários. | Definir a organização das métricas, a necessidade de comparação lado a lado, os mecanismos de histórico e a apresentação das informações necessárias à tomada de decisão. | Alta |
| H03 | Os usuários possuem familiaridade suficiente com métricas e vocabulário técnico de robótica para utilizar uma interface de análise de desempenho. | A Entrega 3 considerou familiaridade técnica na construção das personas. A Entrega 2 analisou ferramentas que apresentam métricas especializadas, mas o conhecimento dos usuários ainda não foi investigado diretamente. | Definir a terminologia utilizada na interface, a necessidade de legendas, explicações de indicadores, identificação de unidades e diferentes níveis de detalhamento técnico. | Alta |



## Parte A — necessidades e requisitos de IHC

> **Responsabilidade:** solução individual por integrante.

### A01 — {{autor}}

**Autor(a):** {{nome — matrícula}}

#### Que dados coletar?

| Dado/informação | Hipótese/lacuna relacionada | Por que é necessário | Qual decisão de design pode afetar |
|---|---|---|---|
| {{...}} | {{H01/H02/...}} | {{...}} | {{...}} |

#### De quem coletar?

| Perfil/stakeholder | Critério de inclusão | Relação com persona/público |
|---|---|---|
| {{...}} | {{...}} | {{...}} |

#### Aspectos éticos

Analise voluntariedade, consentimento, minimização de dados, privacidade, riscos, gravação, anonimização, armazenamento e descarte. Não responda apenas “sim, por causa da LGPD”: explique **quais dados e riscos existem neste projeto**.

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

> Cada integrante deve preparar uma técnica/instrumento completo. As técnicas devem ser diferentes entre si e **questionário deve estar entre as técnicas escolhidas**, conforme o enunciado da disciplina.

### Instrumento I01 — {{nome da técnica}}

**Autor(a):** {{nome — matrícula}}  
**Técnica:** questionário / entrevista semiestruturada / observação / grupo focal / outra autorizada  
**Objetivo:** {{...}}  
**Público:** {{...}}

#### Procedimento padronizado de aplicação

1. {{preparação}}
2. {{apresentação/consentimento}}
3. {{aplicação}}
4. {{encerramento}}
5. {{armazenamento/anonimização}}

#### Instrumento

Cole aqui o questionário/roteiro completo ou forneça link **mais uma cópia textual no repositório**.

#### Como os dados serão analisados

{{ex.: distribuição de respostas, codificação temática, agrupamento de problemas}}



### Instrumento I03 — Observação contextual

**Autor(a):** Rafaela Altheman de Campos — 22.125.062-4

**Técnica:** Observação contextual com registro estruturado.

**Objetivo:** Observar como integrantes de equipes de robótica consultam, interpretam e apresentam resultados de experimentos, identificando as informações utilizadas, as dificuldades encontradas e as estratégias adotadas para recuperar dados e comunicar conclusões.

**Público:** Professores, orientadores, pesquisadores, líderes técnicos e estudantes responsáveis por acompanhar ou apresentar resultados de experimentos de robótica.

**Hipóteses relacionadas:** H01b, H02 e H03.

**Duração estimada:** 20 a 40 minutos.

#### Procedimento padronizado de aplicação

1. **Preparação:** selecionar um participante que realize atividades de acompanhamento ou apresentação de resultados experimentais. Combinar a observação em um contexto adequado e preparar a ficha de registro.
2. **Apresentação e consentimento:** explicar que a atividade pretende compreender a rotina de análise e comunicação de resultados. Informar que a participação é voluntária e solicitar autorização antes de iniciar.
3. **Aplicação:** acompanhar a atividade realizada pelo participante, observando como ele seleciona informações, consulta métricas, interpreta resultados e busca evidências adicionais. O observador deverá evitar interferir na execução da tarefa.
4. **Encerramento:** realizar perguntas breves para esclarecer pontos observados e permitir comentários adicionais do participante.
5. **Armazenamento e anonimização:** organizar as notas por códigos, retirar informações identificáveis e manter os registros em ambiente de acesso restrito.

#### Instrumento — protocolo de observação

**Identificação da sessão**

- Código do participante: O___
- Data: ___/___/_____
- Contexto da observação: __________________
- Atividade observada: __________________
- Ferramentas utilizadas: __________________

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

| Momento | Ação observada | Informação/ferramenta consultada | Dificuldade identificada | Estratégia utilizada |
|---|---|---|---|---|
| 00:00 | A preencher | A preencher | A preencher | A preencher |
| ... | ... | ... | ... | ... |

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

Caso a observação ocorra com um participante proxy ou por meio de uma atividade representativa, essa condição será documentada como limitação metodológica.
---

## Síntese

Explique quais lacunas de conhecimento sobre usuários o conjunto de técnicas pretende reduzir. Indique explicitamente quais hipóteses da Entrega 1 deverão ficar **sustentadas, refutadas ou refinadas** após a análise dos dados. Quando os dados forem coletados/analisados, atualize o histórico em `RASTREABILIDADE.md`.

## Checklist

- [ ] Hipóteses/lacunas prioritárias da Entrega 1 foram revisitadas.
- [ ] Se o escopo de IHC foi derivado de TCC técnico, a coleta investiga a plausibilidade do usuário, tarefa e contexto adotados.
- [ ] Perguntas não pressupõem que dashboard, CRUD, filtros ou relatórios sejam necessários; investigam a necessidade.
- [ ] Cada dado a coletar responde uma dúvida concreta do projeto ou justifica outra necessidade de informação.
- [ ] Parte A identifica dados e perfis de coleta de forma específica.
- [ ] Aspectos éticos são contextualizados para o projeto.
- [ ] Há uma técnica completa por integrante e técnicas distintas.
- [ ] Questionário está incluído entre as técnicas.
- [ ] Cada instrumento possui objetivo, público, procedimento e conteúdo integral.
- [ ] Perguntas evitam indução e coletam apenas dados necessários.
- [ ] Está claro como os dados serão analisados e usados no design.

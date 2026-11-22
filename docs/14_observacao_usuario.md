# Entrega 14 — Avaliação de usabilidade por observação de usuários

**Data:** {{22/11/2026}}  
**Status:**  em andamento 
**Responsabilidade:** solução consolidada por equipe. O número de participantes finais observados deve ser igual ao número de integrantes, conforme o modelo da disciplina; recomenda-se que cada integrante seja responsável por conduzir/analisar ao menos um participante.

## Objetivo da atividade

Observar usuários representativos realizando tarefas reais ou realisticamente simuladas para identificar problemas de eficácia, eficiência, compreensão e satisfação que não podem ser inferidos apenas por inspeção.

> **Participantes finais não devem ser membros da equipe.** Um integrante pode participar do teste piloto apenas para validar roteiro/equipamentos, sem contar na amostra final.

### Quando o usuário é um perfil profissional especializado

Em TCCs técnicos, o público pode ser DBA, analista, pesquisador, administrador, técnico ou outro especialista. Priorize participantes que possuam relação real com as tarefas. Se não for possível recrutar o perfil ideal, qualquer participante aproximado/proxy deve ser **justificado previamente e tratado como limitação**; não apresente o resultado como equivalente ao de especialistas reais.

O teste avalia a **interação com o protótipo**. Não é necessário que o participante valide o desempenho científico do algoritmo. Resultados simulados podem ser usados quando declarados e coerentes com a tarefa.

Tarefas podem envolver, por exemplo, interpretar um dashboard, configurar uma análise, encontrar uma execução no histórico usando filtros, comparar resultados, gerar relatório, revisar alerta ou administrar permissões.

## A. Fluxograma do processo — equipe

![Fluxograma](../assets/14_testes/fluxograma.svg)

O fluxograma deve representar, no mínimo: planejamento → recrutamento → consentimento → preparação → execução das tarefas/observação → pós-teste → consolidação/análise → recomendações.


## B. Procedimento de preparação e execução — equipe

### Passo 1 — Objetivos e versão avaliada

**Versão/commit/Figma:** Protótipo navegável da Entrega 11, disponível em [Figma — IHC](https://www.figma.com/proto/qHpoJxQF4Sthdy99w7Scul/IHC?node-id=32-2023&p=f&scaling=min-zoom&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=32%3A2023).

**Metas de usabilidade relacionadas:** MU01, MU02, MU03, MU04, MU05, MU06, MU07 e MU08, definidas na Entrega 8 e utilizadas no planejamento DECIDE da Entrega 12.

A avaliação tem como objetivo observar a interação de usuários com o protótipo da plataforma de análise de desempenho de robôs humanoides, verificando a eficácia, eficiência, compreensão das informações, satisfação e capacidade de recuperação de erros.

Serão avaliadas as três tarefas principais do projeto:

- **T01 — Avaliar o desempenho de um treinamento:** verificar se o usuário consegue interpretar diferentes indicadores e concluir se houve melhoria no desempenho do robô.
- **T02 — Localizar e comparar execuções anteriores:** verificar se o usuário consegue recuperar treinamentos, comparar resultados e reconhecer possíveis limitações dos dados.
- **T03 — Apresentar resultados em reunião:** verificar se o usuário consegue consultar indicadores, observar evidências e retornar à apresentação sem perder o contexto.

A avaliação considera os cenários de interação CI01, CI02 e CI03 da Entrega 9 e os modelos MoLIC M01, M02 e M03 da Entrega 10.

O protótipo utiliza dados demonstrativos e interações simuladas. O teste avalia a usabilidade da interface, não o desempenho científico do algoritmo de aprendizado por reforço.

**Versão de referência:** registrar a data e a versão efetivamente utilizadas antes da primeira sessão, mantendo o mesmo protótipo para todos os participantes.

### Passo 2 — Participantes

A avaliação será realizada com **três participantes externos à equipe**, correspondendo ao número de integrantes, conforme o enunciado da disciplina.

Foram selecionados participantes com diferentes níveis de familiaridade com tecnologia e conceitos de usabilidade. Os dois primeiros não possuem conhecimento prévio sobre robótica ou análise de desempenho de robôs, enquanto a terceira participante é estudante da disciplina de Interação Humano-Computador (IHC), mas não participou do desenvolvimento do projeto.

Como os participantes não representam diretamente os profissionais especializados que compõem o público-alvo da plataforma, serão considerados **usuários aproximados (proxy)**. Essa condição será registrada como limitação da avaliação. Ainda assim, a participação permite observar aspectos como clareza das informações, compreensão dos indicadores, navegação e facilidade de uso do protótipo.

| ID | Perfil | Critérios que justificam participação | Integrante responsável |
|---|---|---|---|
| U01 | Participante sem conhecimento prévio na área | Pessoa sem familiaridade com robótica ou análise de desempenho de treinamentos. Sua participação permite observar a compreensão inicial da interface, a clareza dos indicadores e possíveis dificuldades de navegação por usuários não especializados. | Letizia Lowatzki Baptistella |
| U02 | Participante sem conhecimento prévio na área | Pessoa sem experiência com robótica ou sistemas de análise de treinamentos. Sua participação permite identificar dificuldades de interpretação das informações, localização de execuções e comparação de resultados sem conhecimento técnico prévio. | Manuella Filipe Peres |
| U03 | Estudante da disciplina de IHC | Colega de turma que possui conhecimentos básicos sobre usabilidade e avaliação de interfaces, mas não participou do desenvolvimento do projeto. Sua participação permite avaliar a interface sem influência das decisões tomadas pela equipe durante o desenvolvimento. | Rafaela Altheman de Campos |

Cada participante realizará as tarefas UT01, UT02 e UT03, totalizando até nove execuções de tarefas observadas.

### Passo 3 — Consentimento e privacidade

- **Termo/registro de consentimento:** utilizar o modelo preparado na Entrega 12, com aceite obtido antes do início de cada sessão. Inserir aqui o link definitivo do termo utilizado.
- **Gravação de tela/áudio/vídeo:** a definir conforme autorização específica de cada participante. Caso não haja autorização, a equipe realizará somente registros escritos de observação e cronometragem.
- **Forma de anonimização:** os participantes serão identificados exclusivamente pelos códigos `U01`, `U02` e `U03`, sem divulgação de nomes reais.
- **Local e período de armazenamento:** definir antes da aplicação; os registros devem permanecer em local de acesso restrito à equipe, pelo período informado no consentimento.

Antes de iniciar a avaliação, o participante será informado sobre o objetivo acadêmico da atividade, a natureza voluntária da participação, o uso das informações coletadas e o direito de interromper o teste.

### Passo 4 — Teste piloto

**Data:** PENDENTE — realizar antes das sessões finais.

**O que será validado:**

O teste piloto será realizado para verificar se o procedimento de avaliação está adequado antes da participação dos usuários finais.

Serão verificados o funcionamento dos links e fluxos do Figma, a clareza das instruções, o tempo necessário para cada tarefa, a aplicação dos questionários, a cronometragem e o registro das observações.

Também será verificado se os estados de erro e recuperação necessários aos cenários estão navegáveis e se as informações demonstrativas são suficientes para a interpretação dos resultados.

O piloto poderá ser realizado por um integrante da equipe, exclusivamente para validar o procedimento, sem ser contabilizado como participante final.

**Mudanças após piloto:** PENDENTE — registrar os ajustes efetivamente realizados no roteiro, nas instruções ou no ambiente de teste. Caso nenhuma alteração seja necessária, registrar essa constatação.

### Passo 5 — Tarefas

As tarefas foram definidas com base no planejamento DECIDE da Entrega 12 e serão apresentadas aos participantes sem indicar os botões ou caminhos que devem utilizar no Figma.

| ID | Cenário/instrução apresentada | Critério de sucesso | Métricas | Ligação com modelo |
|---|---|---|---|---|
| UT01 | "Sua equipe terminou um treinamento e quer decidir se o resultado representa uma melhoria real. Use as informações disponíveis para examinar a execução e chegar a uma conclusão que possa ser comunicada ao grupo." | Identificar a execução, analisar pelo menos dois indicadores, reconhecer possíveis melhorias e pioras e apresentar uma classificação coerente. Confirmar o registro quando a interação estiver disponível. Limite operacional: 8 minutos. | Sucesso, tempo, erros, ajudas, satisfação e interpretação dos indicadores. | T01 / CI01 / M01 / O02, O03, O04, O09 e O11 / F02, F03, F04, F08 e F09. |
| UT02 | "Um resultado antigo parece promissor, mas vocês não sabem se ele pode servir de referência para um experimento recente. Encontre os dois registros, examine as informações disponíveis e deixe documentada sua interpretação e eventuais limitações." | Localizar duas execuções distintas, comparar métricas e condições, reconhecer informações ausentes e registrar hipótese ou ressalvas quando disponível. Limite operacional: 8 minutos. | Sucesso, tempo, erros, ajudas, satisfação e reconhecimento das limitações. | T02 / CI02 / M02 / O01 e O05–O12 / F02, F03, F04, F05, F06, F07 e F10. |
| UT03 | "Durante uma reunião de orientação, surge uma dúvida sobre um resultado apresentado. Consulte os dados necessários, aprofunde a evidência e depois retome a discussão exatamente do ponto em que estava." | Consultar o indicador, abrir a evidência detalhada e retornar preservando a execução, o período e o indicador apresentado. Limite operacional: 6 minutos. | Sucesso, tempo, erros, ajudas, satisfação e preservação do contexto da apresentação. | T03 / CI03 / M03 / O02, O09 e O13–O16 / F14, F15 e F48. |

Os critérios de sucesso devem ser mantidos durante todas as sessões. Caso alguma ação essencial não esteja implementada no protótipo, a tarefa será identificada como **não avaliável (NA)** quando necessário, registrando-se a limitação do Figma sem atribuir a falha ao participante.

A satisfação será registrada após cada tarefa, utilizando escala de 1 a 5, conforme o planejamento da Entrega 12.

### Passo 6 — Protocolo do moderador

1. **Receber o participante:** explicar brevemente o objetivo da avaliação e esclarecer que o produto está sendo avaliado, não a capacidade da pessoa.

2. **Obter consentimento:** apresentar o termo, esclarecer dúvidas e confirmar a autorização antes de iniciar qualquer observação ou gravação.

3. **Aplicar questionário pré-teste:** registrar informações relevantes sobre familiaridade com tecnologia, interpretação de gráficos, sistemas de análise e experiência com robótica, sem solicitar dados pessoais desnecessários.

4. **Apresentar as instruções:** informar que o participante utilizará um protótipo navegável no Figma e que algumas funcionalidades são simulações. Explicar a dinâmica do teste sem ensinar os caminhos da interface.

5. **Executar as tarefas:** apresentar UT01, UT02 e UT03 individualmente, observando a navegação sem indicar onde clicar. Registrar sucesso, erros, tempo, dúvidas, dificuldades e solicitações de ajuda.

6. **Aplicar verbalização do pensamento, quando adotada:** solicitar que o participante explique o que está tentando fazer e o que compreendeu das informações apresentadas, sem interferir em suas decisões.

7. **Registrar satisfação:** após cada tarefa, perguntar o nível de satisfação com a interação, utilizando escala de 1 a 5.

8. **Realizar pós-teste:** fazer perguntas breves sobre facilidade de navegação, compreensão dos indicadores, dificuldades encontradas, mensagens de erro e percepção geral da interface.

9. **Encerrar a sessão:** agradecer a participação, esclarecer a finalidade dos registros e explicar que os resultados serão analisados de forma anônima para identificar oportunidades de melhoria.

Ao término das três sessões, a equipe consolidará os resultados quantitativos e qualitativos para comparação com as metas MU01–MU08 e com os problemas identificados na inspeção heurística da Entrega 13.

## C. Resultados — por participante

### U02 — Participante sem conhecimento prévio na área

| Tarefa | Grau de sucesso | Erros | Tipos de erro/dificuldade | Ajudas | Tempo | Satisfação | Evidência/observação |
|---|---|---:|---|---:|---|---|---|
| UT02 | total | Reconhecimento de telas e entendimento dos gráficos | Erro de reconhecimento da interface, nível iniciante | Foi necessário ajudar no entendimento das tarefas e dos gráficos e métricas | 13:27 | 5 | {{Demonstrou satisfação apesar dos pontos que acreditou que poderiam ser melhorados como legenda nos gráficos e melhor explicação de qual tela o usuário está |

**Link da gravação (se autorizado):** {{[link](https://www.youtube.com/watch?v=_Eauqhbo4q0)}}  
**Resposta pós-teste:** 

# Questionário Pós-Teste — Avaliação de Usabilidade

**Projeto:** Plataforma de Análise de Desempenho de Robôs Humanoides
**Participante:** Juliana Silva do Nascimento
**Data:** 22/11/2026

**Objetivo:** Identificar a percepção geral do participante sobre a facilidade de uso, compreensão das informações e dificuldades encontradas durante a interação com o protótipo.
### 1. De maneira geral, como você avalia a facilidade de utilização da interface?
- [ ] 1 — Muito difícil
- [ ] 2 — Difícil
- [ ] 3 — Nem fácil, nem difícil
- [x] 4 — Fácil
- [ ] 5 — Muito fácil
### 2. Qual das três atividades você considerou mais difícil? Por quê?
- [ ] UT01 — Avaliar o desempenho de um treinamento
- [x] UT02 — Localizar e comparar treinamentos anteriores
- [ ] UT03 — Consultar evidências durante uma reunião
**Por quê?**
Achou difícil entender em qual tela estava, se confundiu com a tela inicial
### 3. Os indicadores e as informações apresentados na interface foram fáceis de compreender?
- [x] Sim
- [ ] Parcialmente
- [ ] Não
**Houve algum termo, número ou informação que causou dúvida?**
Não
### 4. Você conseguiu identificar facilmente para onde deveria navegar durante as atividades?
- [x] Sim
- [ ] Parcialmente
- [ ] Não
**Em algum momento ficou sem saber como continuar?**
Não
### 5. O que você mais gostou na interface?
A parte visual, como a foto do robô, deixando mais claro sobre qual treinamento e modelo de robô estamos falando
### 6. O que você mudaria para tornar a interface mais fácil de utilizar?
Deixaria mais colorido e mais claro sobre em que página está, quais métricas estamos comparando (como legenda nos gráficos)
### 7. Considerando toda a experiência, qual é sua satisfação geral com o protótipo?
- [ ] 1 — Muito insatisfeito(a)
- [ ] 2 — Insatisfeito(a)
- [ ] 3 — Neutro(a)
- [ ] 4 — Satisfeito(a)
- [x] 5 — Muito satisfeito(a)
### Comentários adicionais (opcional)
N/A


> Repita para U02, U03...

## D. Consolidação por tarefa

| Tarefa | Taxa de sucesso | Tempo típico | Erros recorrentes | Satisfação | Meta atendida? | Problemas prioritários |
|---|---:|---|---|---|---|---|
| UT01 | {{...}} | {{...}} | {{...}} | {{...}} | sim/não | {{...}} |

## E. Achados e recomendações

| ID | Achado | Evidência (quant. + qual.) | Impacto | Recomendação | Artefatos a revisar |
|---|---|---|---|---|---|
| AU01 | {{...}} | {{2/4 falharam + fala U03...}} | {{...}} | {{...}} | {{MoLIC/Figma/signos...}} |

## F. Comparação com a avaliação heurística

| Problema | Detectado na heurística? | Detectado por usuários? | O que aprendemos |
|---|---|---|---|
| {{...}} | sim/não | sim/não | {{...}} |

## G. Conclusão

A conclusão deve responder:

1. Quais metas de usabilidade foram atingidas?
2. Quais problemas foram recorrentes e com quais perfis/tarefas?
3. O que surpreendeu a equipe?
4. Quais mudanças são prioritárias?
5. Que limitações do teste impedem generalizações amplas?

## Checklist

- [ ] Número de participantes finais atende ao enunciado.
- [ ] Participantes são representativos do público e não são membros da equipe.
- [ ] Se foram usados participantes proxy, a justificativa e a limitação estão explícitas.
- [ ] O teste avalia a interação; não confunde usabilidade do protótipo com desempenho técnico do TCC.
- [ ] Tarefas administrativas/analíticas usadas no teste são rastreáveis a objetivos e cenários.
- [ ] Há consentimento e anonimização.
- [ ] Foi realizado teste piloto.
- [ ] Tarefas têm critérios de sucesso definidos antes do teste.
- [ ] Moderadores não ensinaram o caminho durante a tarefa.
- [ ] Resultados estão separados por usuário e por tarefa.
- [ ] Foram registrados sucesso, erros, ajudas, tempo e satisfação quando aplicáveis.
- [ ] Conclusão combina evidência quantitativa e qualitativa.
- [ ] Achados geram recomendações e atualização da rastreabilidade.

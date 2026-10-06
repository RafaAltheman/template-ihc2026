# Entrega 1 — Conhecendo o projeto, o usuário e o problema

**Data:** 12/08/2026

**Status:** 🟦 revisada após feedback

**Responsabilidade:** 1 solução consolidada por equipe

Equipe nº 27
## Objetivo da atividade

Reinterpretar o tema do TCC sob a perspectiva de Interação Humano-Computador e construir um **entendimento comum entre os integrantes da equipe**.

A disciplina utiliza preferencialmente o tema do TCC para os exercícios de IHC. Isso vale tanto para TCCs que já preveem uma interface quanto para trabalhos cujo resultado principal é algoritmo, modelo, API, biblioteca, análise de dados, infraestrutura, estudo experimental ou outro artefato técnico.

> **Importante:** a interface projetada na disciplina é um artefato de aprendizagem de IHC. Ela **não se torna automaticamente uma obrigação do TCC**. Sua incorporação ao trabalho de conclusão depende de decisão da equipe e do orientador.

Antes de preencher, leia [`../GUIA_ESCOPO_IHC.md`](../GUIA_ESCOPO_IHC.md).

Nesta primeira semana a equipe **não deve começar desenhando telas**. Primeiro deverá compreender:

- o que o TCC realmente produz;
- quem poderia obter valor dessa contribuição;
- quais pessoas interagem, administram, configuram, interpretam ou são afetadas;
- o que essas pessoas precisam alcançar;
- como atividades relacionadas acontecem hoje;
- problemas, limitações e contexto;
- alternativas existentes;
- qual recorte de interação fará sentido para a disciplina.

Ao final desta entrega, a equipe deve diferenciar:

- **tema do TCC** × **escopo formal do TCC** × **escopo de IHC da disciplina**;
- **objetivo do projeto** × **objetivo do usuário**;
- **problema do usuário** × **solução tecnológica**;
- **fato conhecido** × **hipótese** × **lacuna de conhecimento**;
- **capacidade técnica** × **forma de uso dessa capacidade**;
- **funcionalidade** × **atividade/resultado que o usuário precisa alcançar**;
- **usuário direto** × **stakeholders**.

---

## Como classificar as respostas

Sempre que a resposta fizer uma afirmação sobre usuários, problemas, atividades, necessidades, contexto ou mercado, use:

- **[F] Fato conhecido** — existe evidência/fonte.
- **[H] Hipótese** — afirmação plausível que ainda precisa ser investigada.
- **[?] Não sabemos ainda** — lacuna relevante.

Quando usar `[F]`, informe a origem. Hipóteses prioritárias devem receber IDs (`H01`, `H02`...) e também ser registradas em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

> **Exemplo:** `[H] H01 — DBAs considerariam útil comparar automaticamente o plano atual de execução com uma recomendação produzida pelo algoritmo.`

Uma hipótese explicitada é melhor do que uma suposição escondida.

---

# 0. Identificação do TCC e da equipe

## 0.1 Membros

| Nome completo | Matrícula | GitHub |

| Rafaela Altheman de Campos | 22.125.062-4 | RafaAltheman |

| Manuella Filipe Peres | 24.224.039-3 | manu3lla |

| Letizia Lowatzki Baptistella | 22.125.063-2 | le-bap |

## 0.2 Título atual do TCC

**Aprendizado por reforço profundo para locomoção bípede de um robô humanoide em simulação**

## 0.3 Orientador(a)

Orientador: Isaac Jesus

Coorientador: Reinaldo Bianchi

## 0.4 Qual é o resultado principal atualmente previsto no TCC?

Marque e descreva:

- [ ] sistema/aplicação interativa;
- [ ] algoritmo;
- [X] modelo de IA/ML/LLM;
- [ ] biblioteca/API/framework;
- [ ] análise de dataset;
- [ ] estudo/benchmark/avaliação experimental;
- [ ] infraestrutura/backend;
- [ ] componente embarcado/IoT;
- [ ] outro: {{...}}.

**Descrição:** Modelo de aprendizado por reforço profundo responsável por aprender uma política de controle para a locomoção bípede do robô humanoide Atom, buscando uma caminhada estável e eficiente em ambiente simulado da RoboCup 3D.

## 0.5 O TCC já previa desenvolvimento de interface com usuário?

- [ ] Sim, a interface já faz parte do TCC.
- [ ] Parcialmente; existe alguma interação, mas ainda não está bem definida.
- [X] Não. O TCC é predominantemente técnico e não previa interface.

**Explique o que está formalmente previsto no TCC:** O TCC prevê a modelagem do robô humanoide Atom e sua integração à plataforma de simulação MuJoCo, onde serão realizados o treinamento e a avaliação do modelo de aprendizado por reforço profundo. A interação ocorre com o ambiente de simulação para configurar, executar e analisar os experimentos, mas não está previsto o desenvolvimento de uma interface específica voltada ao usuário.

> Esta resposta serve para separar o compromisso do TCC do projeto da disciplina. Mesmo quando a opção for **não**, a equipe irá definir uma interface para exercitar IHC.

---

# 1. Entendendo a contribuição do projeto

## 1.1 Explique o TCC em uma frase, sem citar linguagem de programação, framework ou banco de dados.

O TCC busca desenvolver uma estratégia de locomoção bípede estável e eficiente para o robô humanoide Atom por meio de aprendizado por reforço profundo em ambiente simulado.

## 1.2 Qual situação, atividade ou problema do mundo real motivou o TCC?

[F] A motivação surgiu a partir da experiência das integrantes em competições de robótica, principalmente no Brasil, onde foi possível observar a dificuldade das equipes em desenvolver um walking estável e eficiente. Problemas na locomoção, como quedas e baixa velocidade, acabam prejudicando diretamente o desempenho do robô durante as partidas.

Origem: experiência das integrantes da equipe em competições de robótica e literatura utilizada no TCC sobre o impacto da locomoção no desempenho competitivo.

Fonte: MacAlpine e Stone (2018), referência [19] do TCC — https://link.springer.com/chapter/10.1007/978-3-030-00308-1_39

## 1.3 Qual é a capacidade/contribuição central produzida pelo TCC?

[F] Nosso TCC busca melhorar a forma como o robô humanoide Atom caminha, usando aprendizado por reforço profundo para que ele aprenda uma política de controle capaz de manter o equilíbrio, se deslocar com mais estabilidade e velocidade e lidar melhor com situações inesperadas durante a simulação. A ideia é que esse walking contribua para um desempenho melhor do robô nas partidas.

Origem: objetivo e metodologia do próprio TCC.

## 1.4 O que se espera que esteja diferente para pessoas, organizações ou processos se essa contribuição for bem-sucedida?

[H] Se a proposta funcionar bem, ela pode contribuir não só para a RoboFEI, mas também servir como referência para outras equipes de futebol de robôs humanoides que enfrentam dificuldades parecidas com locomoção. O estudo pode ajudar no desenvolvimento de walkings mais estáveis e eficientes e mostrar como o aprendizado por reforço profundo pode ser aplicado nesse tipo de problema.

## 1.5 O que é mérito técnico/científico do TCC e o que seria uma possível aplicação prática?

| Mérito/contribuição técnica                                                                                                  | Possível aplicação/valor em uso                                                     |
| ---------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| Desenvolvimento e avaliação de uma política de controle com aprendizado por reforço profundo para a locomoção bípede do Atom | Melhorar o walking do Atom e contribuir para uma locomoção mais estável e eficiente |
| Avaliação por diferentes métricas de desempenho                                                                              | Permitir uma análise mais completa da qualidade da locomoção                        |
| Estudo do DRL como alternativa aos métodos tradicionais de controle                                                          | Servir como referência para outras equipes e pesquisas de robótica humanoide        |

---

# 2. Entendendo as pessoas envolvidas

## 2.1 Quem interage diretamente com o produto, se já existe interface prevista?

NÃO SE APLICA AO ESCOPO ORIGINAL

[F] O TCC não prevê uma interface própria para usuário. A interação atual acontece diretamente com o ambiente de simulação já existente (MuJoCo).

## 2.2 Quem poderia usar, configurar, administrar, operar, interpretar ou tomar decisões a partir da contribuição técnica?

Considere perfis profissionais e stakeholders, não apenas consumidores finais.

| Perfil                                                                   | Relação com a contribuição                                                               | O que faria                                                                                                                                                          | Status/evidência                                |
| ------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------- |
| Integrante da equipe responsável pelo desenvolvimento da locomoção       | Participa diretamente dos treinamentos e da avaliação do robô                            | Executaria treinamentos, analisaria métricas, observaria o comportamento do robô, compararia resultados e decidiria quais ajustes realizar nos próximos experimentos | [F] — experiência direta das integrantes no TCC |
| Responsável pelo acompanhamento técnico                                  | Acompanha os resultados e orienta decisões relacionadas ao desenvolvimento do TCC        | Interpretaria resultados e discutiria com a equipe possíveis ajustes ou próximos experimentos                                                                        | [F] — participação no projeto                   |
| Pesquisador ou estudante de robótica que utilize os resultados do estudo | Poderia utilizar os resultados e aprendizados do TCC como referência para outros estudos | Analisaria os resultados apresentados e poderia comparar diferentes abordagens em trabalhos futuros                                                                  | [H] — ainda não investigado                     |

## 2.3 Existem pessoas afetadas que não usariam a interface diretamente?

| Stakeholder                                   | Como é afetado                                                                                                  | Usa interface?      | Status/evidência              |
| --------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | ------------------- | ----------------------------- |
| Demais integrantes da equipe RoboFEI          | Podem ser beneficiados caso melhorias nos treinos contribuam para o desempenho do robô nas competições          | não                 | [F] — participação no projeto |
| Professores e orientadores                    | Acompanham o desenvolvimento e podem utilizar os resultados para orientar decisões técnicas e trabalhos futuros | não necessariamente | [F] — participação no projeto |
| Outras equipes de futebol de robôs humanoides | Podem utilizar os resultados e aprendizados do trabalho como referência para seus próprios projetos             | não                 | [H] — ainda não investigado   |
| Pesquisadores da área de robótica humanoide   | Podem utilizar os resultados como referência para comparação e continuidade de pesquisas                        | não                 | [H] — ainda não investigado   |

## 2.4 Que características desses perfis podem influenciar a interação?

Considere conhecimento do domínio, experiência tecnológica, frequência de uso, necessidades de acessibilidade, responsabilidade profissional, familiaridade com métricas, linguagem técnica, urgência etc.

[H] O usuário prioritário provavelmente terá conhecimento técnico em robótica e familiaridade com métricas de desempenho, embora o nível de experiência possa variar entre estudantes e integrantes mais experientes da equipe.

[F] O TCC utiliza diferentes métricas para avaliar a locomoção, como distância percorrida, velocidade média, altura do centro de massa e taxa de quedas, já que a recompensa isolada não é suficiente para avaliar o comportamento do agente.

Origem: metodologia do TCC.

[H] O acompanhamento dos experimentos pode ocorrer de forma recorrente durante períodos de desenvolvimento e preparação para competições, podendo haver pressão de tempo para interpretar resultados e decidir quais ajustes realizar.

[H] Organizar essas informações de forma visual e comparável pode facilitar a interpretação dos resultados.

---

# 3. Entendendo objetivos e atividades

## 3.1 O que o usuário está tentando conseguir no mundo real?

Não responda “usar o algoritmo”, “clicar no sistema” ou “ver o dashboard”.

[F] O usuário busca interpretar os resultados dos experimentos de treinamento do robô humanoide, identificar se as alterações realizadas produziram melhorias ou comportamentos indesejados e decidir quais ajustes devem ser realizados nos próximos treinamentos.

Origem: experiência das integrantes durante os experimentos do TCC e processo de treinamento e avaliação da locomoção.

## 3.2 Quais são as atividades mais importantes?

| ID  | Atividade/objetivo                                                     | Quem realiza                      | Frequência/criticidade inicial | Status/evidência         |
| --- | ---------------------------------------------------------------------- | --------------------------------- | ------------------------------ | ------------------------ |
| A01 | Configurar e iniciar treinamentos do agente                            | Integrantes da equipe de robótica | Frequente / alta               | [F] — metodologia do TCC |
| A02 | Acompanhar e interpretar métricas de desempenho do treinamento         | Integrantes da equipe             | Frequente / alta               | [F] — metodologia do TCC |
| A03 | Comparar resultados dos treinamentos e avaliar o comportamento do robô | Integrantes da equipe             | Frequente / alta               | [F] — metodologia do TCC |
| A04 | Ajustar parâmetros                                                     | Integrantes da equipe             | Frequente / alta               | [F] — metodologia do TCC |

## 3.3 Qual atividade parece mais frequente? Por quê?

[F] A atividade que parece mais frequente é acompanhar os treinamentos e analisar seus resultados, porque o desenvolvimento envolve vários ciclos de treinamento, avaliação e ajuste de parâmetros até chegar a um comportamento bom para o robô.

Origem: processo de treinamento e avaliação descrito no TCC.

## 3.4 Qual parece mais crítica? Que consequência existe se for mal executada?

[F] A atividade mais crítica é acompanhar e interpretar corretamente os resultados do treinamento (A02), pois essa interpretação subsidia a comparação dos resultados e a decisão sobre quais ajustes realizar nos próximos experimentos. Uma interpretação errada pode levar a equipe a manter parâmetros ou uma função de recompensa inadequados, fazendo o agente aprender comportamentos que parecem bons pelas métricas, mas que não representam uma caminhada eficiente.

Origem: metodologia e métricas de avaliação do TCC.

---

# 4. Entendendo o problema ou processo atual

## 4.1 Como essas atividades são realizadas hoje, antes da interface imaginada na disciplina?

[F] Atualmente, a equipe realiza o processo de treinamento diretamente no ambiente de simulação MuJoCo. Primeiro, as integrantes configuram no código os parâmetros do experimento e iniciam o treinamento pelo terminal. Dependendo da quantidade de timesteps, um treinamento pode levar aproximadamente de 10 a 48 horas.

[F] Durante e após a execução, são observadas as métricas geradas pelo treinamento, como recompensa, distância percorrida e velocidade. Também é realizada uma análise visual do comportamento do robô no simulador, utilizando a melhor execução obtida no treinamento (best_model.zip).

[F] Após analisar os resultados, a equipe compara o comportamento e as métricas obtidas com resultados de treinamentos anteriores. Para isso, são consultados separadamente os resultados dos experimentos, os arquivos e registros associados e a visualização do comportamento do robô no simulador.

[F] O histórico dos experimentos e das configurações utilizadas também precisa ser registrado pela equipe para permitir a comparação entre diferentes execuções e a recuperação das decisões tomadas anteriormente.

[F] A decisão sobre quais parâmetros ou aspectos do treinamento devem ser alterados é tomada a partir da interpretação conjunta das métricas, das configurações utilizadas e do comportamento observado no simulador. Em seguida, uma nova execução é iniciada.

[?] Ainda não sabemos como outras equipes de robótica humanoide registram, organizam e comparam seus experimentos de treinamento.

Origem: experiência direta das integrantes nos experimentos do TCC e metodologia do projeto.

## 4.2 O que é difícil, demorado, confuso, repetitivo, arriscado ou pouco transparente?

[F] O processo exige vários ciclos de treinamento, análise e ajuste de parâmetros. Como as informações de diferentes experimentos não ficam centralizadas, a equipe precisa consultar separadamente métricas, arquivos, registros e observações do comportamento do robô.

[F] Comparar diferentes treinamentos e entender quais alterações realmente contribuíram para uma melhoria pode ser difícil quando os resultados e as configurações utilizadas em cada execução precisam ser recuperados manualmente.

[F] A equipe também precisa registrar manualmente informações sobre os experimentos para conseguir lembrar quais configurações foram utilizadas e quais resultados foram obtidos anteriormente.

[F] Essa dificuldade pode aumentar o risco de uma interpretação incompleta dos resultados. Por exemplo, observar apenas a recompensa pode fazer um treinamento parecer melhor mesmo quando outras métricas e o comportamento visual indicam que o robô praticamente não está caminhando.

Origem: experiência direta das integrantes nos experimentos do TCC.

## 4.3 Que informações o profissional precisa interpretar para tomar decisão?

[F] O profissional precisa interpretar informações como:

* recompensa obtida durante o treinamento;
* distância percorrida;
* velocidade média;
* taxa de quedas;
* estabilidade e equilíbrio do robô;
* comportamento visual do walking;
* configurações e parâmetros utilizados em cada treinamento;
* consumo da bateria.

Essas informações ajudam a decidir se o treinamento está evoluindo e quais ajustes devem ser feitos para os próximos experimentos.

Origem: metodologia e métricas de avaliação do TCC.

## 4.4 O que acontece quando a atividade falha ou quando o resultado é interpretado incorretamente?

[F] Uma interpretação incorreta pode fazer a equipe considerar um treinamento como bom mesmo quando o agente aprendeu um comportamento inadequado. Por exemplo, o agente pode aumentar sua recompensa mantendo-se parado e equilibrado, sem realmente aprender a caminhar de forma eficiente.

[F] Nesse caso, a equipe pode utilizar como referência um treinamento inadequado ou realizar ajustes nos parâmetros com base em uma interpretação incompleta dos resultados, comprometendo os treinamentos seguintes.

[F] A função de recompensa, a escolha das observações do agente e a convergência do treinamento também podem produzir problemas técnicos, mas esses aspectos pertencem principalmente ao desenvolvimento do algoritmo e à infraestrutura do TCC, não constituindo diretamente problemas de interação da interface proposta.

Origem: metodologia e avaliação de resultados gerados no TCC.

## 4.5 Conte uma situação concreta.

Escreva uma pequena narrativa com pessoa, objetivo, atividade, contexto, dificuldade e consequência. Não descreva ainda a futura solução.

[F] Durante um dos experimentos de treinamento da locomoção do Atom, uma integrante analisou os resultados de uma execução após o término do treinamento. O objetivo era verificar se aquela execução apresentava uma evolução em relação aos treinamentos anteriores.

[F] Ao consultar inicialmente a recompensa, foi observado um aumento em relação a execuções anteriores, o que poderia indicar uma evolução positiva do treinamento.

[F] Em seguida, a integrante comparou esse resultado com outras métricas e observou o comportamento do robô no simulador. Foi possível perceber que o agente estava mais equilibrado, mas quase não se deslocava.

[F] A situação exigiu analisar conjuntamente diferentes métricas, os parâmetros utilizados e o comportamento visual do robô antes de decidir se o treinamento deveria ser considerado uma evolução. Uma interpretação baseada apenas na recompensa poderia levar a equipe a utilizar como referência um treinamento inadequado e realizar novos experimentos a partir de uma conclusão incorreta.

## 4.6 Que evidência existe hoje?

| Evidência/fonte                                         | O que sustenta                                                                          | Limitação                                                     |
| ------------------------------------------------------- | --------------------------------------------------------------------------------------- | ------------------------------------------------------------- |
| Experimentos preliminares realizados no TCC             | Mostram que configurações e treinamentos precisam ser acompanhados e avaliados          | Representam principalmente o processo da própria equipe       |
| Metodologia e literatura utilizada no TCC               | Sustentam a necessidade de analisar várias métricas e não apenas recompensa             | Não mostram como outras equipes organizam essa análise        |
| Experiência das integrantes com a RoboFEI e competições | Sustenta a dificuldade prática relacionada ao desenvolvimento de um walking competitivo | A experiência não representa necessariamente todas as equipes |

---

# 5. Entendendo o contexto de uso

## 5.1 Onde e em quais situações a interação poderia ocorrer?

[H] A interação poderia ocorrer principalmente em laboratórios de robótica e durante períodos de desenvolvimento, testes e preparação para competições. A análise dos resultados também pode acontecer após testes ou partidas, quando a equipe precisa decidir quais ajustes serão feitos.

## 5.2 Em quais dispositivos/equipamentos?

[H] Principalmente em computadores ou notebooks utilizados para executar o ambiente de simulação, realizar os treinamentos e analisar os resultados.

## 5.3 Existem condições físicas relevantes?

Considere iluminação, ruído, mobilidade, conexão, privacidade, uso compartilhado, interrupções, pressão de tempo etc.

[H] Não foram identificadas condições físicas muito específicas para o uso. Como a interação deve ocorrer principalmente em computadores, podem existir interrupções e pressão de tempo durante períodos de testes ou preparação para competições.

## 5.4 Existem fatores sociais ou organizacionais?

Considere papéis, chefias, equipes, permissões, aprovação, responsabilidade profissional, auditoria, turnos e colaboração.

[H] Sim. O desenvolvimento acontece dentro de uma equipe de robótica, então diferentes integrantes podem participar da configuração dos experimentos, análise dos resultados e tomada de decisões.

[F] Também existe acompanhamento de professores e orientadores, que participam das decisões técnicas do projeto.

## 5.5 Existe necessidade de histórico, rastreabilidade ou auditoria?

[F] Existe necessidade de histórico dos experimentos, pois a equipe precisa recuperar configurações, métricas e resultados anteriores para comparar diferentes execuções e compreender a evolução do treinamento.

[F] Uma interpretação inadequada dos resultados pode levar a equipe a tomar decisões incorretas sobre os próximos experimentos e gerar perda de tempo computacional.

[F] Para interpretar corretamente um treinamento, é necessário considerar diferentes métricas e o comportamento observado do robô, pois uma única métrica pode não representar adequadamente a qualidade da locomoção.

## 5.6 Um erro pode produzir consequência relevante? Qual?

[F] Sim. Uma configuração inadequada ou uma interpretação errada dos resultados pode fazer a equipe realizar novos experimentos a partir de uma avaliação incorreta, gerando perda de tempo computacional.

[F] A interface poderia influenciar principalmente problemas relacionados à visibilidade, comparação, recuperação de informações e interpretação dos resultados. Já problemas como função de recompensa inadequada, escolha das observações do agente, convergência do treinamento e necessidade de hardware adequado permanecem como questões técnicas do TCC e restrições do contexto.

Origem: metodologia e discussão do TCC.

---

## 6. Entendendo mercado e alternativas existentes

Nesta entrega faça apenas um levantamento inicial. A análise aprofundada ocorre na Entrega 2.

## 6.1 Como pessoas resolvem problemas semelhantes hoje?

| Alternativa atual                                                                         | Quem usa                                           | Para quê                                                                             | Status/evidência                |
| ----------------------------------------------------------------------------------------- | -------------------------------------------------- | ------------------------------------------------------------------------------------ | ------------------------------- |
| Relatórios e gráficos gerados pelos treinamentos                                          | Integrantes da equipe que executam os experimentos | Acompanhar a evolução das métricas durante e após o treinamento                      | [F] — experiência direta no TCC |
| Arquivos e registros dos experimentos                                                     | Integrantes da equipe                              | Recuperar configurações e resultados de execuções anteriores                         | [F] — experiência direta no TCC |
| Observação visual no simulador                                                            | Integrantes da equipe                              | Verificar se o comportamento aprendido corresponde ao que as métricas indicam        | [F] — experiência direta no TCC |
| Análise manual combinando métricas, configurações e comportamento visual                  | Integrantes da equipe                              | Interpretar os resultados e decidir quais ajustes realizar nos próximos treinamentos | [F] — experiência direta no TCC |
| Ferramentas de organização de dados, planilhas ou registros utilizados por outras equipes | Outras equipes de robótica                         | Registrar, organizar e comparar experimentos de treinamento                          | [?] — ainda não investigado     |

## 6.2 Existem produtos que atuam na mesma área, mesmo sem serem equivalentes ao TCC?

[F] No processo atual do TCC, os resultados dos treinamentos são acompanhados por meio dos próprios arquivos e gráficos gerados durante as execuções, pelos registros das configurações utilizadas e pela visualização do robô no simulador.

[F] Ambientes de simulação, como MuJoCo e PyBullet, também fazem parte do contexto técnico em que experimentos de robótica e aprendizado por reforço podem ser executados. Entretanto, eles não constituem soluções equivalentes à interface de análise proposta nesta disciplina.

[F] No contexto atual do TCC, o MuJoCo é utilizado para executar os experimentos de locomoção e observar o comportamento aprendido pelo robô.

Fonte: metodologia do TCC e literatura utilizada no projeto.

## 6.3 Quais interfaces profissionais esse público já conhece?

[F] No processo atual da equipe, as principais interfaces utilizadas para acompanhar os experimentos são o terminal, os arquivos e gráficos gerados pelo treinamento e a visualização do robô no simulador.

[?] Ainda não foi investigado quais ferramentas específicas outras equipes utilizam para organizar, registrar e comparar seus experimentos.

## 6.4 O que essas soluções parecem fazer bem?

[F] Os arquivos e gráficos gerados pelos treinamentos permitem acompanhar as métricas produzidas durante as execuções e recuperar resultados para análise posterior.

[F] A visualização do robô no simulador permite observar diretamente o comportamento aprendido e verificar se ele corresponde ao que as métricas indicam.

[F] A combinação dessas fontes permite que a equipe realize atualmente a análise dos resultados dos treinamentos, ainda que de forma distribuída entre diferentes artefatos.

[?] Ainda não foi investigado quais ferramentas ou formas de organização utilizadas por outras equipes apresentam melhores resultados para comparação de experimentos.

## 6.5 O que parecem fazer mal, dificultar ou não atender?

[F] No processo atual da equipe, as informações necessárias para interpretar um treinamento estão distribuídas entre diferentes fontes, como métricas, arquivos de configuração, registros e observação do simulador. Isso exige que a equipe faça manualmente a relação entre essas informações.

[F] A comparação entre diferentes treinamentos também depende da recuperação manual dos resultados e das configurações utilizadas em cada execução.

[H] Essa organização distribuída pode dificultar uma comparação rápida entre experimentos e aumentar o esforço necessário para recuperar o contexto de um treinamento anterior.

## 6.6 Que padrões de interface ou vocabulário parecem familiares a esse público?

[F] No processo atual, o público já está familiarizado com métricas de treinamento, gráficos de resultados, arquivos de configuração, registros de experimentos e visualização do robô no simulador.

[F] Também é familiar a necessidade de relacionar diferentes métricas para interpretar o comportamento do robô, já que a recompensa isolada não é suficiente para avaliar adequadamente a locomoção.

[?] Ainda não foi investigado quais padrões específicos de interfaces de análise e comparação são utilizados por outras equipes de robótica humanoide.


---

# 7. Derivando o escopo de IHC da disciplina

## 7.1 Escolha o caminho do projeto

### Caminho A — TCC já possui interface

Explique qual parte da interface será usada como recorte da disciplina e por que esse fluxo é relevante.

Não possui interface, vamos seguir o caminho B.

### Caminho B — TCC não possui interface prevista

Faça o exercício de transferência de uso:

> **Imagine que o TCC foi concluído com sucesso e uma empresa, laboratório ou organização quer transformar a contribuição em algo utilizável. Quem precisaria interagir com ela e para quê?**


Responda:

NOTA: Como o TCC não possui interface, validamos com o professor sobre modificar a proposta do projeto para além do escopo de locomoção do robô: As respostas agora dizem respeito ao treinamento de um robô humanoide que joga futebol.


1. quem poderia contratar/adotar a solução? 

Equipes de robótica, laboratórios de pesquisa, universidades e organizações que desenvolvem robôs humanoides.

2. quem seria o usuário direto? 

Estudantes que participam de equipes de robótica, pesquisadores e desenvolvedores responsáveis por acompanhar o desempenho do robô.

3. quem administraria/configuraria? 

Integrantes técnicos da equipe, responsáveis por inserir parâmetros de testes, extrair os dados de diferentes experimentos, configurar métricas de comparação e realizar treinos

4. quem interpretaria resultados?

Desenvolvedores, pesquisadores, professores e responsáveis técnicos pela evolução do robô.

5. quem tomaria decisões?

A própria equipe de desenvolvimento, que utilizaria os resultados para decidir quais aspectos do robô precisam ser melhorados e evoluir

6. quais dados/entradas seriam necessários? 

Dados de desempenho do robô, como velocidade, força exercida nos motores, agrecividade nas investidas, nível de colaboração e nível de confiança.

7. quais resultados deveriam ser compreendidos? 

O desempenho geral do robô, seus pontos fortes e fracos, evolução ao longo do tempo,  comparação com outros experimentos, entendendo  quantas faltas foram feitas, quantos gols marcados, quantos gols tomados, velocidade média e consumo da bateria

8. que erros/rupturas seriam possíveis? 

Inserção de dados incorretos, comparação entre testes realizados em condições diferentes, interpretação errada das métricas ou ausência de informações importantes para avaliar o desempenho.

## 7.2 Qual perfil será priorizado no projeto de IHC?

Estudante de uma equipe de robótica humanoide responsável por analisar e melhorar o desempenho do robô que joga futebol.

**Por que esse perfil foi escolhido?** 

Porque esse usuário participa diretamente do processo de desenvolvimento e precisa interpretar diferentes informações sobre o comportamento e o desempenho do robô ao longo de testes, treinamentos e competições. Isso pode envolver métricas como velocidade, estabilidade, quedas, desempenho em partidas, evolução entre versões e resultados de diferentes execuções. A partir dessas informações, ele precisa identificar pontos fortes, limitações e possíveis melhorias, além de comparar resultados para apoiar decisões da equipe, no contexto da faculdade. A interface pode ajudar a reunir e organizar esses dados, facilitando a análise do desempenho e o acompanhamento da evolução do robô ao longo do tempo.

## 7.3 Qual objetivo desse usuário será priorizado?

O objetivo priorizado será analisar e interpretar o desempenho do robô a partir dos resultados de seus treinamentos e partidas, identificando problemas, pontos de melhoria e possíveis relações entre as métricas observadas para apoiar decisões sobre os próximos ajustes do robô.
Esse objetivo está relacionado à atividade crítica A02: Acompanhar e interpretar métricas de desempenho. Essa atividade é crítica porque uma interpretação incorreta dos resultados pode levar a equipe a considerar um treinamento como adequado quando o comportamento aprendido não representa uma boa locomoção, resultando em ajustes inadequados nos experimentos seguintes.

## 7.4 Que interface será explorada na disciplina?

Complete:

> **Para fins da disciplina de IHC, será projetada uma interface que permita a `{{perfil}}` utilizar `{{capacidade/resultado do TCC}}` para `{{objetivo}}`, no contexto de `{{situação}}`.**

*Para fins da disciplina de IHC, será projetada uma interface que permite* um estudante de uma equipe de robótica humanoide responsável por analisar e melhorar o desempenho do robô que joga futebol *utilizar* a comparação entre experimentos, iniciação de treinamentos, ajustes de parâmetros e análise de métricas *para* entender o desempenho do robô humanoide, identificar seus principais pontos de melhoria, acompanhar sua evolução ao longo dos testes e coletar estatísticas dele durante as partidas, *no contexto de* competições nacionais e internacionais de robótica humanoide.

## 7.5 Qual é a relação dessa interface com o TCC?

- [ ] Já fazia parte do TCC.
- [ ] É um aprofundamento de algo parcialmente previsto.
- [X] É uma extensão conceitual criada para a disciplina.
- [] É um protótipo demonstrativo de aplicação potencial.
- [ ] Outra: {{...}}.

> **Declaração:** a interface desenvolvida nesta disciplina é um artefato de aprendizagem de IHC baseado no tema do TCC. Sua inclusão ou implementação no TCC somente ocorrerá se isso for posteriormente decidido pela equipe e pelo orientador.

A interface não faz parte do escopo formal do TCC. Ela utiliza o contexto de robótica humanoide e avaliação de desempenho como ponto de partida, mas amplia o foco para permitir que equipes acompanhem, comparem e interpretem o desempenho de seus robôs de forma mais geral.

# 8. Levantando possibilidades de interação — sem desenhar ainda

A equipe pode registrar possibilidades para investigação. **Não significa que todas serão implementadas.**

Marque apenas as que parecem plausíveis e explique o objetivo correspondente.

| Possibilidade | Pode fazer sentido? | Objetivo/tarefa que justificaria | Evidência atual |

| Possibilidade                       | Pode fazer sentido? | Objetivo/tarefa que justificaria                                                                                        | Evidência atual |
| ----------------------------------- | ------------------- | ----------------------------------------------------------------------------------------------------------------------- | --------------- |
| Dashboard/visão geral               | Sim                 | Ter uma visão rápida do desempenho geral do robô e das principais métricas                                              | [H]             |
| Configuração/parametrização         | Talvez              | Permitir escolher quais métricas, robôs, testes ou competições serão analisados                                         | [H]             |
| Entrada/upload/seleção de dados     | Sim                 | Inserir ou selecionar resultados de testes, treinamentos e competições para análise                                     | [H]             |
| Acompanhamento de processamento     | Talvez              | Acompanhar o carregamento e o processamento de novos resultados                                                         | [H]             |
| Relatório/resultados                | Sim                 | Visualizar os resultados de forma organizada e apoiar a tomada de decisão                                               | [H]             |
| Histórico com busca/filtros         | Sim                 | Consultar resultados anteriores e localizar informações por robô, data, competição ou tipo de teste                     | [H]             |
| Comparação de resultados            | Sim                 | Comparar diferentes robôs, versões, testes ou execuções e identificar onde houve melhora ou piora                       | [H]             |
| Explicabilidade/detalhamento        | Sim                 | Entender melhor as métricas, os resultados e os pontos fortes e fracos do robô                                          | [H]             |
| Administração/configurações globais | Não                 | Neste momento, não foi identificada uma necessidade clara para esse tipo de administração                               | [?]             |
| Usuários/perfis/permissões          | Talvez              | Pode ser útil caso diferentes integrantes ou públicos tenham responsabilidades e níveis de acesso distintos             | [?]             |
| CRUD de entidade do domínio         | Talvez              | Permitir cadastrar e atualizar robôs, equipes, testes ou competições, caso isso seja necessário para organizar os dados | [H]             |
| Auditoria/logs                      | Não                 | Neste momento, não foi identificada uma necessidade clara de auditoria ou registro detalhado das alterações             | [?]             |
| Alertas/ocorrências                 | Talvez              | Destacar quedas de desempenho, resultados fora do esperado ou acontecimentos importantes durante testes e competições   | [H]             |
| Ajuda/documentação                  | Sim                 | Explicar métricas, informações da interface e facilitar o uso por pessoas com diferentes níveis de conhecimento técnico | [H]             |


> **Atenção:** “login + dashboard + CRUD” não é uma solução universal. Cada padrão deve surgir de uma tarefa real.

---

# 9. Benefícios e ações iniciais

## 9.1 Qual benefício concreto o projeto de IHC pretende oferecer?

| Benefício esperado | Problema/necessidade | Usuário | Status/evidência |

| Benefício esperado                                    | Problema/necessidade                                                                                                                | Usuário                                            | Status/evidência |
| ----------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------- | ---------------- |
| Facilitar a análise do desempenho do robô             | As informações de desempenho podem estar espalhadas entre diferentes métricas, testes e observações                                 | Integrantes de equipes de robótica humanoide       | [H]              |
| Facilitar a comparação entre testes e versões do robô | Pode ser difícil perceber rapidamente se uma mudança realmente melhorou ou piorou o desempenho                                      | Integrantes de equipes de robótica humanoide       | [H]              |
| Ajudar a identificar pontos de melhoria               | A equipe precisa entender em quais aspectos o robô apresenta melhor ou pior desempenho                                              | Integrantes de equipes de robótica humanoide       | [H]              |
| Acompanhar a evolução do robô ao longo do tempo       | As informações obtidas durante testes e partidas podem não ficar organizadas de forma que facilite a análise e comparação posterior | Integrantes de equipes de robótica e pesquisadores | [H]              |


## 9.2 Que ações o usuário deverá conseguir realizar?

| **ID** | **O usuário precisa conseguir...**                                                   | **Para alcançar...**                                                                                                                                                           | **Prioridade inicial** |
| ------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------- |
| AC01    | Visualizar as principais métricas de desempenho do robô em um treinamento ou partida (A02) | Compreender rapidamente o comportamento do robô e apoiar a atividade crítica, evitando depender de uma única métrica | alta                   |
| AC02    | Comparar resultados de diferentes treinamentos, versões ou partidas (A03)                  | Identificar se uma alteração realmente melhorou ou piorou o desempenho do robô e apoiar a decisão sobre os próximos ajustes                                                    | alta                   |
| AC03    | Consultar o histórico de treinamentos, testes e partidas (A03)                             | Acompanhar a evolução do robô ao longo do tempo e recuperar resultados anteriores para comparação                                                                              | alta                   |
| AC04    | Filtrar resultados por robô, período, versão, treinamento ou competição (A02)               | Encontrar com mais facilidade as informações relevantes para uma análise específica, reduzindo a dificuldade de consultar diferentes resultados                                | média                  |
| AC05    | Visualizar detalhes de um resultado, incluindo suas métricas e configurações (A02)         | Entender o contexto em que determinado desempenho foi obtido e evitar interpretações incorretas dos resultados                                                                 | média                  |
| AC06    | Relacionar diferentes métricas de desempenho (A02)                                         | Avaliar o resultado de forma mais completa, evitando considerar apenas a recompensa quando ela não representa adequadamente o comportamento do robô                            | alta                   |
| AC07    | Identificar pontos de melhoria a partir dos resultados analisados (A04)                    | Decidir quais aspectos do robô devem ser investigados ou ajustados nos próximos treinamentos e testes                                                                          | alta                   |
| AC08    | Consultar e comparar estatísticas de desempenho durante partidas (A02)                     | Analisar o desempenho do robô no contexto competitivo e relacioná-lo às características da performance apresentada                                                                       | média                  |


## 9.3 Tecnologias/restrições já definidas no TCC

A tecnologia aparece **agora**, depois do entendimento do uso.

| Tecnologia/restrição                                          | Por que existe                                                                                     | Possível impacto na interação                                                                          |
| ------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| MuJoCo                                                        | É o simulador utilizado para modelar e executar os experimentos de locomoção                       | A interface pode precisar trabalhar com dados e resultados gerados nesse ambiente                      |
| RoboCup 3D                                                    | É o ambiente de competição utilizado para avaliar o comportamento do robô                          | Os resultados analisados podem estar relacionados a partidas e testes realizados nesse ambiente        |
| Aprendizado por Reforço Profundo                              | É a abordagem utilizada para treinar a política de locomoção do robô                               | A interação pode envolver métricas específicas de treinamento, como recompensa, episódios e desempenho |
| Modelo do robô em formato compatível com o MuJoCo             | O robô precisa estar representado no simulador para que os experimentos possam ser executados      | Pode limitar quais robôs conseguem ser utilizados diretamente no mesmo fluxo                           |
| Necessidade de hardware com capacidade computacional adequada | Os treinamentos podem exigir grande quantidade de processamento                                    | Pode afetar o tempo de execução dos experimentos e a disponibilidade dos resultados                    |
| Execução em Linux                                             | O ambiente e as ferramentas utilizadas no projeto foram configurados para esse sistema operacional | Limita a execução dos treinamentos e experimentos a máquinas compatíveis com Linux                     |



---

# 10. Hipóteses e dúvidas prioritárias

| ID  | Hipótese/dúvida                                                                                                                                                     | Por que importa                                                   | Como poderá ser investigada |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------- | --------------------------- |
| H01 | Estudantes de equipes de robótica têm dificuldade em reunir e comparar diferentes métricas e informações de desempenho dos robôs ao longo de testes e competições. | É o principal problema que justificaria a criação da plataforma.  | Entregas 3, 4 e 7           |
| H02 | Centralizar e comparar resultados de diferentes testes, versões ou robôs ajudaria as equipes a identificar melhorias, pioras e limitações de desempenho.            | Sustenta uma das principais propostas de interação da plataforma. | Entregas 5, 6 e 7           |
| H03 | Os usuários possuem familiaridade suficiente com métricas e vocabulário técnico de robótica para utilizar uma interface de análise de desempenho.                   | Influencia a linguagem e o nível de detalhamento da interface.    | Entregas 3 e 7              |



Registre em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

---

# 11. Síntese da equipe

| Pergunta                               | Síntese atual                                                                                                                                                                                                          |
| -------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Qual é a contribuição central do TCC?  | Desenvolver e avaliar uma política de controle baseada em aprendizado por reforço profundo para melhorar a locomoção bípede do robô humanoide Atom.                                                                    |
| O TCC já previa interface?             | Não. O TCC é predominantemente técnico e utiliza ferramentas e ambientes de simulação já existentes.                                                                                                                   |
| Quem é o usuário prioritário de IHC?   | Integrantes de equipes de robótica humanoide responsáveis por acompanhar, analisar e contribuir para a melhoria do desempenho dos robôs.                                                                               |
| O que ele precisa alcançar?            | Entender o desempenho do robô, identificar pontos fortes, limitações e oportunidades de melhoria e acompanhar sua evolução ao longo do tempo.                                                                          |
| Qual problema/atividade será estudado? | A análise, organização e comparação de métricas e resultados de desempenho obtidos em testes, treinamentos e competições.                                                                                              |
| Como isso acontece hoje?               | No contexto do TCC, os resultados são avaliados por métricas e observação do comportamento do robô. Ainda será investigado como outras equipes organizam e comparam informações de desempenho em diferentes situações. |
| Qual é o contexto de uso?              | Equipes e laboratórios de robótica durante desenvolvimento, testes, treinamentos e competições.                                                                                                                        |
| Que interface/recorte será explorado?  | Uma plataforma para visualizar, acompanhar e comparar métricas e resultados de desempenho de robôs humanoides.                                                                                                         |
| Como a interface se relaciona ao TCC?  | É uma extensão conceitual que parte do contexto de locomoção e avaliação de desempenho estudado no TCC e amplia esse uso para uma análise mais geral do desempenho de robôs humanoides.                                |
| Quais pontos ainda são hipóteses?      | H01 — dificuldade em reunir e comparar informações; H02 — valor da centralização e comparação; H03 — familiaridade técnica dos usuários.                                                                               |


### Delimitação

**Dentro do escopo de IHC:** Projetar e avaliar uma interface que permita visualizar métricas, consultar históricos, comparar resultados e identificar pontos de melhoria no desempenho de robôs humanoides.

**Fora do escopo de IHC:** Desenvolver ou modificar algoritmos de locomoção, controlar diretamente o robô, criar um novo simulador ou implementar o sistema completo de coleta automática dos dados.

**Dentro do escopo formal do TCC:** Modelagem do Atom, treinamento de uma política de locomoção utilizando aprendizado por reforço profundo e avaliação do desempenho do robô em ambiente simulado.

**Interface da disciplina será implementada no TCC?** não definido — Não definido — a interface é uma extensão conceitual criada para a disciplina de IHC e sua implementação no TCC não está prevista atualmente.

---

# 12. Como esta entrega alimenta as próximas

- **Entrega 2:** verifica mercado, concorrentes e interfaces profissionais representativas.
- **Entrega 3:** detalha perfis e contexto.
- **Entrega 4:** aprofunda situações problemáticas.
- **Entrega 5:** modela tarefas centrais.
- **Entrega 6:** experimenta alternativas em baixa fidelidade.
- **Entrega 7:** investiga hipóteses com dados.
- **Entrega 8:** define restrições e metas de usabilidade.
- **Entregas 9–11:** transformam o recorte em modelo de interação e protótipo.
- **Entregas 12–14:** avaliam a interface construída na disciplina.

A Entrega 1 é uma **fotografia inicial do conhecimento**. Ela pode e deve ser revisada quando surgirem evidências.

---

# 13. Relação com INOVA e comunicação do projeto

Prepare uma explicação de até três frases:

1. **Problema/atividade humana:** Equipes de robótica precisam acompanhar e comparar diferentes informações para entender o desempenho de locomoção de seus robôs e identificar o que pode ser melhorado.

2. **Contribuição técnica do TCC:** O TCC busca desenvolver uma política de controle baseada em aprendizado por reforço profundo para melhorar a locomoção bípede do robô humanoide Atom.

3. **Como uma pessoa poderia utilizar essa contribuição:** Uma equipe poderia acompanhar e comparar os resultados de desempenho do robô para identificar pontos fortes, limitações e orientar decisões sobre seu desenvolvimento, para competir ou melhorar os estudos acadêmicos sobre isso.

Essa síntese ajuda a apresentar o projeto para público não especializado sem reduzir seu mérito técnico.

---

# Checklist de qualidade

- [X] Está clara a diferença entre tema do TCC, escopo formal do TCC e escopo de IHC.
- [X] A equipe declarou se o TCC já previa interface.
- [X] Se não previa, foi derivado um usuário plausível e um objetivo de uso.
- [X] A interface de IHC não foi apresentada como obrigação automática do TCC.
- [X] A contribuição do TCC foi descrita sem começar por tecnologias de implementação.
- [X] Usuários diretos e stakeholders foram diferenciados.
- [X] Foram considerados profissionais que configuram, administram, interpretam ou decidem, quando pertinente.
- [X] Objetivo do usuário não foi confundido com objetivo do projeto.
- [X] Processo/problema atual foi descrito antes da solução.
- [X] Existe situação concreta de uso/problema.
- [X] Contexto físico, social/organizacional, dispositivos e consequências de erro foram considerados.
- [X] Mercado/alternativas existentes foram levantados inicialmente.
- [X] Possibilidades como dashboard, relatório, histórico, filtros e CRUD foram tratadas como hipóteses de solução, não como requisitos automáticos.
- [X] Cada possibilidade de interface tem um objetivo/tarefa que poderia justificá-la.
- [X] Afirmações relevantes estão marcadas `[F]`, `[H]` ou `[?]`.
- [X] Hipóteses prioritárias receberam IDs e foram para a rastreabilidade.
- [X] O recorte de IHC é viável para modelar, prototipar e avaliar no semestre.
- [X] A equipe consegue explicar problema humano → contribuição computacional → forma de uso.

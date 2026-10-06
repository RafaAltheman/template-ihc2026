# Matriz de rastreabilidade de IHC

A matriz deve ser atualizada ao longo do semestre. Ela ajuda a demonstrar que a interface não surgiu arbitrariamente e registra **como o conhecimento da equipe evoluiu**.

Para projetos cujo TCC não previa interface, esta matriz é especialmente importante: deve ficar visível a passagem da **contribuição técnica do TCC** para um **cenário de uso plausível**, e desse cenário para as decisões de interação.

## 1. Derivação do escopo de IHC a partir do TCC

| Elemento | Registro da equipe | Evidência/justificativa | Estado |
|---|---|---|---|
| Tema do TCC | Aprendizado por reforço profundo para locomoção bípede de um robô humanoide em simulação | Tema definido no TCC | definido |
| Resultado técnico esperado | Modelo de aprendizado por reforço profundo capaz de aprender uma política de controle para a locomoção bípede do robô humanoide Atom | Objetivo e metodologia do TCC | definido |
| O TCC previa interface? | Não | O TCC é predominantemente técnico e utiliza ferramentas e ambientes de simulação já existentes | definido |
| Capacidade/contribuição central | Desenvolver e avaliar uma política de controle que permita ao Atom realizar uma locomoção mais estável e eficiente | Objetivo e metodologia do TCC | definido |
| Possíveis beneficiários/stakeholders | Integrantes de equipes de robótica humanoide, pesquisadores, desenvolvedores, professores e orientadores; como públicos secundários, narradores, comentaristas e pessoas que acompanham competições | Perfis levantados na Entrega 1 | H |
| Usuário escolhido para IHC | Integrante de uma equipe de robótica humanoide responsável por acompanhar, analisar e contribuir para a melhoria do desempenho do robô | Perfil priorizado pela equipe na Entrega 1 para orientar o projeto de IHC. As características específicas desse usuário continuam sendo tratadas como hipóteses. | definido |
| Objetivo principal do usuário | Entender o desempenho do robô, identificar pontos fortes, limitações e oportunidades de melhoria e acompanhar sua evolução | Hipótese definida na Entrega 1 | H |
| Contexto de uso adotado | Laboratórios de robótica e situações de desenvolvimento, testes, treinamentos e competições | Hipótese de contexto definida na Entrega 1 | H |
| Interface/recorte de IHC | Plataforma para reunir, visualizar, acompanhar e comparar métricas e resultados de desempenho de robôs humanoides | Derivada do contexto técnico do TCC e da necessidade de análise de resultados | proposta |
| Relação com o TCC | Extensão conceitual e protótipo demonstrativo de aplicação potencial | A interface não faz parte do escopo formal do TCC, mas utiliza seu contexto de robótica humanoide e avaliação de desempenho como ponto de partida | definido |

> Se o escopo de IHC mudar ao longo do semestre, preserve a decisão anterior no histórico e registre **qual evidência motivou a mudança**.

## 2. Registro de hipóteses e lacunas da Entrega 1

Use esta tabela para itens importantes marcados como `[H]` ou `[?]`. Preserve o histórico: não apague uma hipótese refutada.

| ID | Afirmação / dúvida inicial | Tipo | Por que importa | Como/onde investigar | Evidência obtida | Estado atual | Impacto no projeto |
|---|---|---|---|---|---|---|---|
| H01 | Integrantes de equipes de robótica têm dificuldade em reunir e comparar diferentes métricas e informações de desempenho dos robôs ao longo de testes e competições. | H | É o principal problema que justificaria a criação da plataforma. | Entregas 3, 4 e 7 | Na Entrega 3, essa possível dificuldade foi incorporada às dores e à jornada da persona P01, mas ainda não houve validação direta com usuários. Na Entrega 4, os cenários C02 e C03 registraram situações da própria equipe relacionadas a essa dificuldade: a reconstrução da configuração de um treinamento anterior leva mais tempo do que a análise das métricas, quando a configuração não pode ser confirmada é preciso escolher entre repetir o treinamento ou continuar sem ter certeza da comparação, e decisões de reunião já foram adiadas porque as comparações não puderam ser feitas a tempo, deixando uma semana sem novo experimento. Essa evidência vem da experiência da própria equipe e ainda precisa ser verificada com outros integrantes e equipes. | aberta | Pode confirmar, refinar ou enfraquecer a necessidade de centralização das informações. |
| H02 | Centralizar e comparar resultados de diferentes testes, versões ou robôs ajudaria as equipes a identificar melhorias, pioras e limitações de desempenho. | H | Sustenta uma das principais propostas de interação da plataforma. | Entregas 5, 6 e 7 | Na Entrega 3, comparação, histórico e identificação de melhorias foram incorporados como necessidades e oportunidades de design da persona P01. A hipótese ainda não foi validada diretamente com usuários. Na Entrega 2, foram identificados padrões de visualização, histórico e comparação em ferramentas semelhantes (Jupyter Notebook e GitHub), que deram origem às recomendações RC03 e RC06. Na Entrega 4, os cenários C01, C02 e C03 mostram a comparação entre treinamentos como parte da atividade atual. | aberta | Influencia comparação de resultados, histórico e organização das informações. |
| H03 | Os usuários possuem familiaridade suficiente com métricas e vocabulário técnico de robótica para utilizar uma interface de análise de desempenho. | H | Influencia a linguagem e o nível de detalhamento da interface. | Entregas 3 e 7 | Na Entrega 3, a persona P01 foi construída considerando familiaridade com métricas e ferramentas técnicas, mas essa característica continua sendo uma hipótese a ser validada. Na Entrega 2, a análise de concorrentes mostrou o uso de interfaces e ferramentas técnicas nesse contexto, mas não houve validação direta com usuários. | aberta | Pode alterar terminologia, explicações, ajuda e nível de detalhamento da interface. |

## 2.1 Registro de personas da Entrega 3

| ID | Persona | Tipo | Papel no projeto | Hipóteses relacionadas | Estado |
|---|---|---|---|---|---|
| P01 | Rafael Martins | Primária | Integrante técnico de equipe de robótica humanoide que acompanha treinamentos, analisa métricas, compara resultados e participa das decisões sobre os próximos experimentos. | H01, H02, H03 | Persona prioritária |
| P02 | Marina Oliveira | Primária | Pesquisadora de robótica que realiza experimentos, compara parâmetros e analisa resultados do robô. | H01, H02, H03 | Proto-persona a validar. |
| P03 | Carlos Almeida | Primária | Professor, orientador ou responsável técnico que acompanha a evolução dos experimentos e auxilia nas decisões técnicas. | H01, H02 | Proto-persona a validar. |

## 2.2 Registro de recomendações da Entrega 2

| ID | Recomendação | Origem | Hipóteses relacionadas | Tarefa | Tela | Estado |
|---|---|---|---|---|---|---|
| RC01 | Manter o estado do treinamento e do robô visível durante a execução | C01 (NuSight), C03 (GameController) | PENDENTE | PENDENTE | PENDENTE | registrada |
| RC02 | Organizar o fluxo de treinamento em etapas claras de configuração, execução e análise dos resultados | C02 (MARIO), C03 (GameController) | PENDENTE | PENDENTE | PENDENTE | registrada |
| RC03 | Apresentar métricas e resultados do treinamento por meio de visualizações que facilitem sua interpretação | C02 (MARIO), Jupyter Notebook | PENDENTE | PENDENTE | PENDENTE | registrada |
| RC04 | Validar os parâmetros antes do início do treinamento e apresentar mensagens claras quando houver configurações inválidas | C03 (GameController) | PENDENTE | PENDENTE | PENDENTE | registrada |
| RC05 | Centralizar informações relacionadas ao treinamento em uma mesma interface, reduzindo a necessidade de alternar entre diferentes ferramentas | C01 (NuSight), VS Code | PENDENTE | PENDENTE | PENDENTE | registrada |
| RC06 | Manter histórico dos treinamentos e dos resultados obtidos para permitir comparação e rastreabilidade dos experimentos | GitHub | PENDENTE | PENDENTE | PENDENTE | registrada |

## 2.3 Registro de cenários da Entrega 4

| ID | Cenário | Autor(a) | Persona | Necessidade relacionada | Situação concreta da Entrega 1 | Hipóteses relacionadas | Estado |
|---|---|---|---|---|---|---|---|
| C01 | Análise de Performance do Robô | Letizia L. Baptistella | P01 | Visualizar métricas de forma rápida, comparar diferentes treinamentos e versões, consultar histórico e relacionar métricas com o comportamento observado do robô. | Interpretação incorreta dos resultados de treinamento; situação concreta em que a recompensa aumenta, mas o robô apresenta pouco deslocamento. | H01, H02 | concluído |
| C02 | Recuperação da configuração de um treinamento anterior | Manuella Filipe Peres | P02 | Acessar rapidamente os resultados dos treinamentos, comparar diferentes experimentos e consultar os parâmetros utilizados em cada execução. | O histórico dos experimentos e das configurações é registrado manualmente pela equipe e não fica centralizado; risco de comparar testes realizados em condições diferentes. | H01, H02 | concluído |
| C03 | Avaliação de treinamentos em reunião de orientação | Rafaela Altheman de Campos | P03 | Obter uma visão consolidada do desempenho, comparar resultados importantes e compreender rapidamente quais aspectos evoluíram ou pioraram. | Situação em que a recompensa aumenta, mas o robô fica equilibrado e quase não se desloca; professores e orientadores acompanham os resultados e participam das decisões técnicas. | H01, H02 | concluído |

## 3. Rastreabilidade entre contribuição técnica, necessidades e artefatos

| ID | Capacidade do TCC utilizada | Necessidade/problema | Persona | Cenário problema | Objetivo/tarefa | HTA/GOMS/CTT | Cenário de interação / signos | MoLIC | Tela(s) Figma | Heurística / problema | Tarefa no teste | Decisão/melhoria |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| R01 | Métricas de avaliação do treinamento (recompensa, distância percorrida, velocidade média e taxa de quedas) | A melhora em uma métrica pode ocorrer junto à piora de outras, dificultando concluir se o treinamento foi bem-sucedido | P01 | C01 | PENDENTE | PENDENTE | PENDENTE | PENDENTE | PENDENTE | PENDENTE | PENDENTE | PENDENTE |
| R02 | Configurações e parâmetros utilizados em cada treinamento | As anotações não reúnem todos os valores configurados no código e nem sempre é possível confirmar a configuração usada em um treinamento anterior | P02 | C02 | PENDENTE | PENDENTE | PENDENTE | PENDENTE | PENDENTE | PENDENTE | PENDENTE | PENDENTE |
| R03 | Métricas do treinamento e visualização do melhor modelo no simulador | A recompensa aumenta sem que a caminhada melhore e a apresentação não traz as métricas necessárias para avaliar o treinamento na reunião | P03 | C03 | PENDENTE | PENDENTE | PENDENTE | PENDENTE | PENDENTE | PENDENTE | PENDENTE | PENDENTE |

## 4. Rastreabilidade de padrões de interface

Use esta tabela quando o projeto incorporar padrões como dashboard, relatório, histórico, filtros ou administração. O objetivo é **justificar o padrão**, não apenas listar telas.

| ID da tela/fluxo | Padrão de interface | Objetivo/tarefa que justifica | Informação/ação principal | Evidência de necessidade | Artefatos relacionados |
|---|---|---|---|---|---|
| F01 | dashboard/visão geral | PENDENTE | Ter uma visão rápida do desempenho geral do robô e das principais métricas | Possibilidade marcada como "sim" na Entrega 1 (seção 8), ainda hipótese; RC03 (Entrega 2) | C01, C03 |
| F02 | histórico com busca/filtros | PENDENTE | Consultar resultados anteriores e localizar informações por robô, data, competição ou tipo de teste | Possibilidade marcada como "sim" na Entrega 1 (seção 8), ainda hipótese; RC06 (Entrega 2) | C02 |
| F03 | comparação de resultados | PENDENTE | Comparar diferentes robôs, versões, testes ou execuções e identificar onde houve melhora ou piora | Possibilidade marcada como "sim" na Entrega 1 (seção 8), ainda hipótese; RC06 (Entrega 2) | C01, C02 |
| F04 | administração/CRUD | - | Cadastrar e atualizar robôs, equipes, testes ou competições | Não incorporado: marcado como "talvez" na Entrega 1 (seção 8) e, até o momento, não há tarefa que justifique | - |

## 5. Registro de mudanças de escopo

| Data | O que mudou | Evidência/feedback que motivou | Artefatos afetados | Responsável |
|---|---|---|---|---|
| - | Nenhuma mudança de escopo registrada até a Entrega 4. | - | - | - |

## Como usar

- Use identificadores estáveis (`H01`, `P01`, `C01`, `T01`, `M01`, `F01`, `UT01`).
- Quando uma necessidade/problema tiver origem em hipótese da Entrega 1, cite o ID correspondente.
- Em TCC sem interface original, pelo menos uma linha deve mostrar claramente **como uma capacidade técnica chega até uma tarefa de usuário e uma tela/fluxo**.
- Uma linha pode se desdobrar quando um objetivo possui múltiplos caminhos.
- Não force relação inexistente: se algo ainda não foi modelado, marque `PENDENTE`.
- Ao remover uma funcionalidade, registre a decisão em vez de apagar silenciosamente o histórico.
- Dashboard, CRUD, filtros e relatórios só devem aparecer quando houver objetivo/tarefa que os justifique.

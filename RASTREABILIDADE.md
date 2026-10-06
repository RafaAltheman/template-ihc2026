# Matriz de rastreabilidade de IHC

A matriz deve ser atualizada ao longo do semestre. Ela ajuda a demonstrar que a interface não surgiu arbitrariamente e registra **como o conhecimento da equipe evoluiu**.

Para projetos cujo TCC não previa interface, esta matriz é especialmente importante: deve ficar visível a passagem da **contribuição técnica do TCC** para um **cenário de uso plausível**, e desse cenário para as decisões de interação.

## 1. Derivação do escopo de IHC a partir do TCC

| Elemento | Registro da equipe | Evidência/justificativa | Estado |
|---|---|---|---
| Tema do TCC                          | Aprendizado por reforço profundo para locomoção bípede de um robô humanoide em simulação                                                                                                            | Tema definido no TCC                                                                                                                              | definido |
| Resultado técnico esperado           | Modelo de aprendizado por reforço profundo capaz de aprender uma política de controle para a locomoção bípede do robô humanoide Atom                                                                | Objetivo e metodologia do TCC                                                                                                                     | definido |
| O TCC previa interface?              | Não                                                                                                                                                                                                 | O TCC é predominantemente técnico e utiliza ferramentas e ambientes de simulação já existentes                                                    | definido |
| Capacidade/contribuição central      | Desenvolver e avaliar uma política de controle que permita ao Atom realizar uma locomoção mais estável e eficiente                                                                                  | Objetivo e metodologia do TCC                                                                                                                     | definido |
| Possíveis beneficiários/stakeholders | Estudantes de equipes de robótica humanoide, pesquisadores, desenvolvedores, professores e orientadores | Perfis levantados na Entrega 1                                                                                                                    | H        |
| Usuário escolhido para IHC | Estudante de uma equipe de robótica humanoide responsável por acompanhar, analisar e contribuir para a melhoria do desempenho do robô | Perfil priorizado pela equipe na Entrega 1 para orientar o projeto de IHC. As características específicas desse usuário continuam sendo tratadas como hipóteses. | definido |
| Objetivo principal do usuário        | Entender o desempenho do robô, identificar pontos fortes, limitações e oportunidades de melhoria e acompanhar sua evolução                                                                          | Hipótese definida na Entrega 1                                                                                                                    | H        |
| Contexto de uso adotado              | Laboratórios de robótica e situações de desenvolvimento, testes, treinamentos e competições                                                                                                         | Hipótese de contexto definida na Entrega 1                                                                                                        | H        |
| Interface/recorte de IHC             | Plataforma para reunir, visualizar, acompanhar e comparar métricas e resultados de desempenho de robôs humanoides                                                                                   | Derivada do contexto técnico do TCC e da necessidade de análise de resultados                                                                     | proposta |
| Relação com o TCC                    | Extensão conceitual e protótipo demonstrativo de aplicação potencial                                                                                                                                | A interface não faz parte do escopo formal do TCC, mas utiliza seu contexto de robótica humanoide e avaliação de desempenho como ponto de partida | definido |


> Se o escopo de IHC mudar ao longo do semestre, preserve a decisão anterior no histórico e registre **qual evidência motivou a mudança**.

## 2. Registro de hipóteses e lacunas da Entrega 1

Use esta tabela para itens importantes marcados como `[H]` ou `[?]`. Preserve o histórico: não apague uma hipótese refutada.

| ID | Afirmação / dúvida inicial | Tipo | Por que importa | Como/onde investigar | Evidência obtida | Estado atual | Impacto no projeto |
|---|---|---|---|---|---|---|---|
| H01 | Estudantes de equipes de robótica têm dificuldade em reunir e comparar diferentes métricas e informações de desempenho dos robôs ao longo de testes e competições. | H | É o principal problema que justificaria a criação da plataforma. | Entregas 4 e 7 | Na Entrega 3, essa possível dificuldade foi incorporada às dores e à jornada da persona P01, mas ainda não houve validação direta com usuários. | aberta | Pode confirmar, refinar ou enfraquecer a necessidade de centralização das informações. |
| H02 | Centralizar e comparar resultados de diferentes testes, versões ou robôs ajudaria as equipes a identificar melhorias, pioras e limitações de desempenho. | H | Sustenta uma das principais propostas de interação da plataforma. | Entregas 5, 6 e 7 | Na Entrega 3, comparação, histórico e identificação de melhorias foram incorporados como necessidades e oportunidades de design da persona P01. A hipótese ainda não foi validada diretamente com usuários. | aberta | Influencia comparação de resultados, histórico e organização das informações. |
| H03 | Os usuários possuem familiaridade suficiente com métricas e vocabulário técnico de robótica para utilizar uma interface de análise de desempenho. | H | Influencia a linguagem e o nível de detalhamento da interface. | Entrega 7 | Na Entrega 3, a persona P01 foi construída considerando familiaridade com métricas e ferramentas técnicas, mas essa característica continua sendo uma hipótese a ser validada. | aberta | Pode alterar terminologia, explicações, ajuda e nível de detalhamento da interface. |

## 3. Registro de personas da Entrega 3

| ID | Persona | Tipo | Papel no projeto | Hipóteses relacionadas | Estado |
|---|---|---|---|---|---|
| P01 | Rafael Martins | Primária | Estudante técnico de equipe de robótica humanoide que acompanha treinamentos, analisa métricas, compara resultados e participa das decisões sobre os próximos experimentos. | H01, H02, H03 | Persona prioritária |
| P02 | Marina Oliveira | Primária | Pesquisadora de robótica que realiza experimentos, compara parâmetros e analisa resultados do robô. | H01, H02, H03 | Proto-persona a validar. |
| P03 | Carlos Almeida | Primária | Professor, orientador ou responsável técnico que acompanha a evolução dos experimentos e auxilia nas decisões técnicas. | H01, H02 | Proto-persona a validar. |

## 3. Rastreabilidade entre contribuição técnica, necessidades e artefatos

| ID | Capacidade do TCC utilizada | Necessidade/problema | Persona | Cenário problema | Objetivo/tarefa | HTA/GOMS/CTT | Cenário de interação / signos | MoLIC | Tela(s) Figma | Heurística / problema | Tarefa no teste | Decisão/melhoria |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| R01 | {{ex.: recomendação de otimização}} | {{...}} | {{P01}} | {{C01}} | {{T01}} | {{links}} | {{...}} | {{M01}} | {{F01...}} | {{V01 ou —}} | {{UT01}} | {{...}} |
| R02 |  |  |  |  |  |  |  |  |  |  |  |  |

## 4. Rastreabilidade de padrões de interface

Use esta tabela quando o projeto incorporar padrões como dashboard, relatório, histórico, filtros ou administração. O objetivo é **justificar o padrão**, não apenas listar telas.

| ID da tela/fluxo | Padrão de interface | Objetivo/tarefa que justifica | Informação/ação principal | Evidência de necessidade | Artefatos relacionados |
|---|---|---|---|---|---|
| F01 | dashboard | {{T01}} | {{...}} | {{H01/evidência...}} | {{C01/M01}} |
| F02 | histórico com filtros | {{T02}} | {{...}} | {{...}} | {{...}} |
| F03 | administração/CRUD | {{T03}} | {{...}} | {{...}} | {{...}} |

## 5. Registro de mudanças de escopo

| Data | O que mudou | Evidência/feedback que motivou | Artefatos afetados | Responsável |
|---|---|---|---|---|
| {{...}} | {{...}} | {{...}} | {{...}} | {{...}} |

## Como usar

- Use identificadores estáveis (`H01`, `P01`, `C01`, `T01`, `M01`, `F01`, `UT01`).
- Quando uma necessidade/problema tiver origem em hipótese da Entrega 1, cite o ID correspondente.
- Em TCC sem interface original, pelo menos uma linha deve mostrar claramente **como uma capacidade técnica chega até uma tarefa de usuário e uma tela/fluxo**.
- Uma linha pode se desdobrar quando um objetivo possui múltiplos caminhos.
- Não force relação inexistente: se algo ainda não foi modelado, marque `PENDENTE`.
- Ao remover uma funcionalidade, registre a decisão em vez de apagar silenciosamente o histórico.
- Dashboard, CRUD, filtros e relatórios só devem aparecer quando houver objetivo/tarefa que os justifique.

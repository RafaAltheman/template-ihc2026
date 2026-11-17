
# Entrega 12 — Planejamento da avaliação de usabilidade (DECIDE)

**Data:** 16/11/2026  
**Status:** 🟩 concluída
**Responsabilidade:** 1 solução por equipe

**Equipe 27:**
- Letizia Lowatzki Baptistella — 22.125.063-2
- Manuella Filipe Peres — 22.224.029-3
- Rafaela Altheman de Campos — 22.125.062-4

## Objetivo da atividade

Planejar a avaliação antes de executá-la, ligando perguntas de avaliação a métodos, participantes, tarefas, métricas, aspectos práticos, ética e forma de análise.

O planejamento será realizado por meio do método DECIDE, conforme apresentado nas aulas de Planejamento da Avaliação de IHC, com base em Barbosa e Silva (2010).

A avaliação será aplicada ao protótipo de alta fidelidade da plataforma de análise de resultados de treinamentos de robôs humanoides, desenvolvido na Entrega 11.

O objetivo é verificar a compreensão dos indicadores, a facilidade de localização e comparação de execuções, o registro de avaliações e hipóteses e a continuidade da navegação durante a apresentação de resultados.

## O que está sendo avaliado

Em projetos cuja interface foi criada ou ampliada para a disciplina, o plano deve declarar explicitamente que a avaliação investiga **a qualidade da interação/protótipo**, não a validade científica ou o desempenho técnico do algoritmo/modelo do TCC.

A avaliação investigará a qualidade da interação com o protótipo, considerando os cinco atributos de usabilidade definidos na Entrega 8:

- Facilidade de aprendizado.
- Facilidade de memorização.
- Eficiência.
- Baixa taxa de erros.
- Satisfação.

Não serão avaliados a validade científica do TCC, o desempenho do algoritmo PPO ou a qualidade técnica da política de locomoção do robô Atom.

**Protótipo da Entrega 11:**

[Figma — Projeto de IHC](https://www.figma.com/design/qHpoJxQF4Sthdy99w7Scul/IHC?node-id=0-1&t=AqgOAOI2AlypX9Q3-1)

O protótipo utiliza dados ilustrativos ou simulados para representar execuções, métricas, parâmetros e evidências de treinamentos já realizados.

Esses dados permitem avaliar a interação, sem necessidade de integração com o simulador ou execução real dos algoritmos.

A interface não configura nem inicia novos treinamentos.

A avaliação será exploratória, com **um participante externo à equipe**, utilizando observação de uso e inspeção heurística.

A quantidade reduzida de participantes limita a generalização dos resultados. As metas quantitativas da Entrega 8 serão mantidas como referência, sem afirmar validação populacional com uma única pessoa.

---

## A. Método DECIDE

| Etapa | Aplicação no projeto |
|---|---|
| **D — Determine the goals** | Avaliar se o participante consegue realizar as tarefas T01, T02 e T03, compreendendo os indicadores, comparando execuções, registrando conclusões e consultando evidências. Verificar os aspectos de eficácia, eficiência, erros, satisfação e aprendizado definidos nas metas MU01–MU10 da Entrega 8. |
| **E — Explore the questions** | Investigar se o participante consegue localizar treinamentos, interpretar diferenças, identificar informações ausentes, registrar uma hipótese e compreender os resultados. Verificar também se consegue consultar evidências e retornar à apresentação sem perder o contexto. |
| **C — Choose the evaluation paradigm and techniques** | Serão utilizadas avaliação heurística, realizada pela equipe, e observação de uso com um participante externo. O teste será complementado por questionário pré-teste e perguntas pós-tarefa. A combinação permite identificar problemas previstos pelos avaliadores e dificuldades efetivamente observadas. |
| **I — Identify the practical issues** | Uma sessão individual com um participante, preferencialmente presencial, utilizando computador e protótipo no Figma. A equipe verificará os links, realizará um ensaio interno, preparará os instrumentos e dividirá as funções de moderação, observação e registro. Será planejado um retorno após sete dias para MU10, fora do prazo da aplicação inicial. |
| **D — Decide how to deal with ethical issues** | A participação será voluntária e ocorrerá após consentimento informado. O participante poderá interromper o teste sem consequências. Os registros serão identificados por código e utilizados exclusivamente para fins acadêmicos. Qualquer gravação dependerá de autorização específica. |
| **E — Evaluate, interpret and present the data** | Serão registrados conclusão das tarefas, tempos, erros, dúvidas, ajuda solicitada, facilidade percebida e observações. Os resultados serão comparados individualmente às metas da Entrega 8 e apresentados como estudo exploratório, com limitações explícitas. Os problemas serão classificados por gravidade e associados a sugestões de melhoria. |

---

## B. Perguntas de avaliação

| ID | Pergunta | Método | Métrica/evidência | Critério esperado |
|---|---|---|---|---|
| QA01 | O participante consegue avaliar corretamente um treinamento, considerando melhorias e pioras? | Observação UT01 | Conclusão, interpretação e registro sem ajuda. | MU01 — meta original ≥ 80%; registrar sucesso ou falha individual. |
| QA02 | O participante consegue localizar duas execuções, compará-las e registrar uma hipótese com evidências e ressalvas? | Observação UT02 | Localização, comparação, hipótese e registro. | MU02 — meta original ≥ 80%; registrar resultado individual. |
| QA03 | O participante consegue consultar a síntese, identificar um ponto relevante e consultar uma evidência? | Observação UT03 | Conclusão correta da tarefa. | MU03 — meta original ≥ 80%. |
| QA04 | A avaliação e a comparação podem ser realizadas em tempo adequado? | Observação UT01/UT02 | Tempo de cada tarefa bem-sucedida. | MU04 — até 6 minutos por tarefa. |
| QA05 | O participante consegue consultar uma evidência e retornar à apresentação rapidamente? | Observação UT03 | Tempo da consulta e retorno. | MU05 — até 2 minutos por consulta. |
| QA06 | O participante considera as tarefas fáceis de realizar? | Questionário pós-tarefa | Escala de 1 a 5. | MU06 — referência ≥ 4/5. |
| QA07 | A interação evita erros críticos de interpretação ou registro? | Observação e inspeção | Quantidade e descrição de erros críticos. | MU07 — zero erros críticos. |
| QA08 | O participante retorna ao contexto anterior sem refazer seleções? | Observação UT03 | Preservação de período, indicador e apresentação. | MU08 — meta original ≥ 80%. |
| QA09 | No primeiro contato, o participante consegue localizar uma execução após orientação inicial? | Observação inicial UT02 | Consulta correta sem ajuda adicional. | MU09 — meta original ≥ 80%. |
| QA10 | Após sete dias, o participante consegue repetir a consulta ao histórico? | Observação posterior UT04 | Consulta correta sem novo tutorial. | MU10 — meta original ≥ 75%; verificação posterior. |
| QA11 | Existem problemas de feedback, consistência, clareza ou recuperação de erros? | Avaliação heurística | Violações identificadas e sua gravidade. | Registrar e priorizar problemas encontrados. |

Os critérios percentuais correspondem à Entrega 8. Com apenas um participante, as taxas observadas serão 0% ou 100%, não permitindo comprovar o atendimento das metas para a população-alvo.

---

## C. Escopo e participantes

| Item | Planejamento |
|---|---|
| **Perfis** | Um participante adulto externo à equipe, preferencialmente com familiaridade com computação, análise de dados ou robótica. |
| **Critérios de inclusão/exclusão** | Ter 18 anos ou mais, aceitar voluntariamente participar, possuir familiaridade básica com computadores e não ter participado do desenvolvimento da interface. |
| **Nº de participantes** | **1 participante**, identificado como PT01. Amostra exploratória por conveniência. |
| **Ambiente** | Presencial, em local silencioso, ou remoto caso necessário. |
| **Dispositivo** | Computador ou notebook com navegador atualizado e acesso ao Figma. |
| **Protótipo/versão** | Protótipo da Entrega 11, com versão e frame inicial registrados antes da sessão. |
| **Teste piloto** | Ensaio interno realizado pela própria equipe, verificando os caminhos, instruções, cronometragem e instrumentos. O ensaio não será contabilizado como teste com usuário. |

### Organização da aplicação

A avaliação será conduzida em uma sessão individual de aproximadamente 25 a 35 minutos.

**Procedimento:**

1. Apresentar os objetivos da avaliação.
2. Explicar que o objeto do teste é a interface, não o participante.
3. Solicitar consentimento.
4. Aplicar questionário pré-teste.
5. Oferecer orientação inicial padronizada de até 5 minutos, sem ensinar a execução das tarefas.
6. Aplicar UT02 primeiro, para observar o aprendizado no primeiro contato com o histórico (MU09).
7. Aplicar UT01 e UT03.
8. Registrar tempo, conclusão, erros, dúvidas e ajuda.
9. Aplicar pergunta de facilidade após cada tarefa.
10. Realizar perguntas finais e encerrar a sessão.

As três integrantes dividirão as funções:

| Integrante | Responsabilidade |
|---|---|
| Letizia | Moderação da sessão e condução das instruções. |
| Manuella | Cronometragem e registro de erros, dúvidas e ajuda. |
| Rafaela | Observação, questionários, organização das evidências e consolidação. |

### Retorno para avaliação da memorização

A meta MU10, definida na Entrega 8, prevê repetir a consulta ao histórico após **sete dias sem utilizar a interface**, sem reapresentar tutorial ou fornecer ajuda.

Como o prazo disponível é inferior a sete dias, essa medição não poderá ser concluída na aplicação inicial.

O retorno será mantido como etapa planejada e classificado como **não avaliado** até sua realização. Não será utilizado um intervalo menor como se atendesse ao requisito original.

### Limitações

A amostra de um participante permite identificar dificuldades e obter evidências preliminares, mas não oferece base suficiente para generalizar os resultados.

Caso o participante não represente diretamente o público da robótica, isso será informado na análise.

Não serão atribuídos resultados fictícios nem consideradas como falhas do participante as interações que não estiverem funcionais no Figma.

---

## D. Lista de tarefas de avaliação

| ID | Cenário neutro entregue ao usuário | Objetivo oculto da avaliação | Critério de sucesso | Tempo-limite (se houver) |
|---|---|---|---|---|
| **UT02** | "Você precisa recuperar informações de dois treinamentos realizados em momentos diferentes. Encontre essas execuções, compare os resultados e registre uma explicação para as diferenças observadas, considerando informações que não puderam ser confirmadas." | T02 / CI02 / M02 — localizar, comparar e registrar hipótese. MU02, MU04, MU07 e MU09. | Localizar duas execuções, comparar indicadores, identificar limitações e registrar uma hipótese distinguindo evidências e ressalvas. A primeira consulta ao histórico será observada separadamente para MU09. | Limite operacional de 8 minutos; meta MU04 de até 6 minutos. |
| **UT01** | "Sua equipe concluiu um treinamento e precisa decidir se ele realmente apresentou melhoria em relação aos anteriores. Analise os resultados disponíveis e registre sua conclusão." | T01 / CI01 / M01 — interpretar indicadores e registrar avaliação. MU01, MU04 e MU07. | Identificar ganhos e regressões, selecionar uma classificação coerente e concluir o registro associado à execução correta. | Limite operacional de 8 minutos; meta MU04 de até 6 minutos. |
| **UT03** | "Durante uma reunião de orientação, surge uma dúvida sobre o resultado de um treinamento. Consulte uma evidência mais detalhada e retome a apresentação de onde estava." | T03 / CI03 / M03 — apresentar resultados, consultar evidências e preservar contexto. MU03, MU05 e MU08. | Selecionar o período, identificar um ponto relevante, consultar uma evidência e retornar ao mesmo contexto da apresentação. | Limite operacional de 6 minutos; consulta e retorno devem atender MU05 de até 2 minutos. |
| **UT04** | "Retome a atividade de localizar um treinamento anterior que você realizou em sua primeira participação." | T02 — memorização após sete dias. MU10. | Localizar corretamente a execução sem novo tutorial ou ajuda após sete dias. | Aplicação posterior, sem limite adicional de tempo. |

> Uma boa instrução descreve o objetivo do participante sem dizer **onde clicar** ou usar o rótulo exato do controle que está sendo testado.

Os limites operacionais das tarefas não substituem as metas quantitativas definidas na Entrega 8.

### Situações alternativas

A equipe observará, quando disponíveis no protótipo:

| Situação | Aspecto avaliado |
|---|---|
| Busca sem resultados | Clareza da mensagem e possibilidade de corrigir a pesquisa. |
| Comparação com informações ausentes | Reconhecimento das limitações e interpretação cuidadosa. |
| Avaliação ou hipótese não registrada | Identificação do erro e feedback de salvamento. |
| Evidência detalhada | Preservação do contexto ao retornar à apresentação. |

As tarefas devem utilizar dados e execuções definidos previamente no gabarito do avaliador.

---

## E. Instrumentos

- [Modelo de termo de consentimento](../instrumentos/termo_consentimento_modelo.md)
- [Roteiro de teste](../instrumentos/roteiro_teste_usabilidade.md)
- [Planilha de observação](../instrumentos/planilha_observacao_modelo.md)
- [Formulário de avaliação heurística](../instrumentos/formulario_heuristica_modelo.md)
- [Questionário pré e pós-teste](../instrumentos/questionario_pre_pos_teste.md)
- [Guia do avaliador e gabarito](../instrumentos/guia_avaliador_gabarito.md)

Os instrumentos possuem as seguintes finalidades:

| Instrumento | Finalidade |
|---|---|
| Termo de consentimento | Registrar participação voluntária, informações sobre a pesquisa e autorização específica para gravações. |
| Roteiro de teste | Padronizar a condução da sessão e a apresentação das tarefas. |
| Planilha de observação | Registrar conclusão, tempo, erros, ajuda, dúvidas e comentários. |
| Formulário heurístico | Registrar violações, localização, gravidade e sugestões de melhoria. |
| Questionário pré e pós-teste | Caracterizar o participante e coletar a facilidade percebida após as tarefas. |
| Guia do avaliador | Definir resultados esperados e critérios de sucesso sem revelar as respostas ao participante. |

Os instrumentos deverão ser revisados antes da aplicação, especialmente quanto ao tempo específico da MU05, à primeira consulta da MU09 e ao retorno posterior previsto na MU10.

---

## F. Plano de análise

Defina antes dos testes:

- sucesso total / parcial / falha;
- o que conta como erro, dúvida, ajuda e abandono;
- como tempo será medido;
- escala de satisfação pós-tarefa;
- como observações/falas serão codificadas;
- como problemas serão priorizados;
- como comparar resultados às metas de usabilidade.

### Classificação dos resultados

| Categoria | Definição |
|---|---|
| **Sucesso total (S)** | Todos os critérios essenciais foram cumpridos corretamente, sem ajuda de navegação e dentro do limite operacional, quando aplicável. |
| **Sucesso parcial (P)** | Parte do objetivo foi atingida, mas houve dificuldade que impediu a conclusão completa ou exigiu ajuda. |
| **Falha (F)** | O objetivo não foi alcançado, houve abandono ou conclusão incompatível com as informações apresentadas. |
| **Não avaliável (NA)** | Problema técnico ou funcionalidade ausente no protótipo impediu avaliar a tarefa. |

### Definições operacionais

| Indicador | Registro |
|---|---|
| **Tempo** | Cronometragem desde o final do enunciado até a conclusão ou interrupção. |
| **Erro** | Ação incorreta relacionada à tarefa. |
| **Erro crítico** | Decisão equivocada sem percepção, registro associado à execução errada ou falsa compreensão de salvamento. |
| **Dúvida** | Pergunta, hesitação verbalizada ou dificuldade observável. |
| **Ajuda** | Orientação do moderador sobre navegação, controles ou ações. |
| **Abandono** | Participante declara não conseguir ou não desejar continuar. |
| **Facilidade percebida** | Escala pós-tarefa de 1 (muito difícil) a 5 (muito fácil). |
| **Retorno contextual** | Preservação de período, execução e indicador após consultar a evidência. |

### Métricas quantitativas

As metas originais da Entrega 8 serão preservadas como parâmetros de análise.

**Taxa de sucesso — MU01, MU02, MU03 e MU09**

`Taxa de sucesso = (sucessos totais / tentativas avaliáveis) × 100`

Com um participante, o resultado será 0% ou 100%. Isso representa somente o desempenho observado no caso individual.

**Eficiência — MU04**

Será registrado o tempo de UT01 e UT02.

Os valores serão comparados ao limite de 6 minutos por tarefa. Com uma única execução bem-sucedida, a mediana coincide com o tempo registrado, mas não representa uma estimativa robusta para o público-alvo.

**Consulta de evidências — MU05**

Será medido o tempo entre a solicitação de consulta da evidência e o retorno à apresentação.

Meta original: até 2 minutos.

**Facilidade percebida — MU06**

Após cada tarefa, será utilizada a pergunta:

"Em uma escala de 1 a 5, como você avalia a facilidade de realizar esta tarefa?"

- 1 — Muito difícil.
- 2 — Difícil.
- 3 — Nem fácil, nem difícil.
- 4 — Fácil.
- 5 — Muito fácil.

Meta original: mediana igual ou superior a 4/5.

**Erros críticos — MU07**

Será registrada a quantidade de erros críticos observados em UT01 e UT02.

Meta original: zero erros críticos.

**Retorno contextual — MU08**

Será observado se o participante consegue retornar à apresentação sem refazer as seleções de período, execução e indicador.

Meta original: pelo menos 80%.

**Facilidade de aprendizado — MU09**

Será observada a primeira consulta ao histórico, como etapa inicial da UT02, após orientação padronizada de até 5 minutos.

Meta original: pelo menos 80% de conclusão correta.

**Facilidade de memorização — MU10**

A consulta ao histórico deverá ser repetida após sete dias, sem novo tutorial ou ajuda.

Meta original: pelo menos 75%.

Como a etapa ocorrerá posteriormente, será registrada como não avaliada enquanto não houver coleta.

### Dados qualitativos

As observações serão classificadas nas seguintes categorias:

| Código | Categoria | Exemplo |
|---|---|---|
| NAV | Navegação | Dificuldade para localizar o histórico ou retornar. |
| IND | Indicadores | Confusão sobre unidades, gráficos ou métricas. |
| TER | Terminologia | Dificuldade com termos como "baseline". |
| CMP | Comparação | Dificuldade para interpretar diferenças e limitações. |
| FDB | Feedback | Mensagem de erro ou confirmação pouco clara. |
| CTX | Contexto | Perda de seleções após consultar evidência. |
| REG | Registro | Dificuldade para registrar avaliação ou hipótese. |
| APR | Aprendizado | Dificuldade no primeiro contato. |
| MEM | Memorização | Dificuldade após sete dias. |

### Avaliação heurística

A equipe realizará uma inspeção do protótipo considerando as heurísticas de Nielsen e os princípios apresentados na disciplina.

Serão verificados:

- Visibilidade do estado do sistema.
- Correspondência entre sistema e linguagem do usuário.
- Controle e liberdade.
- Consistência e padronização.
- Prevenção de erros.
- Reconhecimento em vez de memorização.
- Clareza e simplicidade visual.
- Feedback e recuperação de erros.

Os problemas identificados serão classificados por gravidade.

| Gravidade | Classificação | Descrição |
|---|---|---|
| 0 | Não é problema | Não representa violação relevante. |
| 1 | Cosmético | Problema visual de baixo impacto. |
| 2 | Menor | Causa dificuldade, mas permite continuar. |
| 3 | Maior | Compromete significativamente a tarefa. |
| 4 | Crítico | Pode impedir a conclusão ou produzir decisão incorreta sem percepção. |

### Consolidação e interpretação

Após a avaliação, a equipe irá:

1. Organizar os registros do participante.
2. Classificar o resultado de cada tarefa.
3. Registrar os tempos e compará-los aos limites previstos.
4. Verificar a facilidade percebida.
5. Identificar erros críticos e dificuldades observadas.
6. Consolidar os problemas encontrados na avaliação heurística.
7. Relacionar os problemas aos princípios e metas de usabilidade.
8. Propor melhorias para a interface.
9. Registrar limitações da amostra.
10. Atualizar a matriz de rastreabilidade com evidências reais.

### Modelo de resultados

A tabela será preenchida após a aplicação.

| Meta | Resultado observado | Referência da Entrega 8 | Situação |
|---|---|---|---|
| MU01 | — | ≥ 80% | Não avaliada |
| MU02 | — | ≥ 80% | Não avaliada |
| MU03 | — | ≥ 80% | Não avaliada |
| MU04 — UT01 | — | ≤ 6 minutos | Não avaliada |
| MU04 — UT02 | — | ≤ 6 minutos | Não avaliada |
| MU05 | — | ≤ 2 minutos | Não avaliada |
| MU06 | — | ≥ 4/5 | Não avaliada |
| MU07 | — | Zero erros críticos | Não avaliada |
| MU08 | — | ≥ 80% | Não avaliada |
| MU09 | — | ≥ 80% | Não avaliada |
| MU10 | — | ≥ 75% após 7 dias | Aplicação posterior |

Os resultados serão apresentados como evidências individuais exploratórias, sem afirmar que as metas foram validadas para o conjunto dos usuários.

### Atualização da rastreabilidade

| Linha | Tarefa de avaliação | Metas relacionadas |
|---|---|---|
| R01 | UT01 — Avaliar desempenho | MU01, MU04, MU06 e MU07 |
| R02 | UT02 — Recuperar e comparar | MU02, MU04, MU06, MU07 e MU09 |
| R03 | UT03 — Reunião de orientação | MU03, MU05, MU06 e MU08 |
| R02 — acompanhamento | UT04 — Consulta após 7 dias | MU10 |

A matriz será atualizada somente após a obtenção das evidências.

---

## Checklist

- [x] As seis etapas DECIDE foram contextualizadas, não apenas expandidas por sigla.
- [x] Perguntas de avaliação têm método e evidência correspondentes.
- [x] O plano distingue avaliação de IHC de avaliação técnica/científica do TCC.
- [x] Dados ou processamentos simulados no protótipo estão declarados.
- [x] Tarefas vêm de objetivos/cenários relevantes.
- [x] Critérios de sucesso foram definidos antes da coleta.
- [x] Questões práticas e éticas estão resolvidas no planejamento.
- [X] Instrumentos estão prontos antes da Entrega 13/14.
- [x] Plano diz como dados serão analisados e apresentados.


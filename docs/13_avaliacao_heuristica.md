# Entrega 13 — Avaliação de IHC por inspeção heurística

**Data:** 16/11/2026  
**Status:** 🟨 em andamento  
**Responsabilidade:** 1 avaliação completa por integrante, sobre todas as telas/estados relevantes do projeto.

## Objetivo da atividade

Avaliar a interface do sistema por meio de inspeção heurística, identificando problemas de usabilidade que possam prejudicar a interação dos usuários. A avaliação utiliza as dez heurísticas de Nielsen como referência e considera as características de uma interface administrativa e analítica, na qual a apresentação correta dos dados, a comparação entre execuções e a interpretação dos resultados são aspectos importantes.

A inspeção considera os estados disponíveis no protótipo da Entrega 11, incluindo telas principais, comparação de execuções, apresentação de indicadores, mensagens de erro, resultados vazios e confirmações de ações.

## 1. Heurísticas adotadas

1. **Visibilidade do estado do sistema:** o sistema deve manter o usuário informado sobre o que está acontecendo, por meio de retornos adequados e em tempo razoável.
2. **Correspondência entre o sistema e o mundo real:** a interface deve utilizar termos, conceitos e unidades familiares ao usuário, apresentando as informações de maneira lógica e compreensível.
3. **Controle e liberdade do usuário:** o usuário deve conseguir desfazer ações indesejadas e retornar de situações inesperadas sem dificuldade.
4. **Consistência e padronização:** elementos, informações, termos e comportamentos semelhantes devem seguir os mesmos padrões em toda a interface.
5. **Prevenção de erros:** a interface deve evitar situações que possam induzir o usuário ao erro, principalmente em ações importantes ou na interpretação de informações.
6. **Reconhecimento em vez de memorização:** as opções e informações necessárias devem estar visíveis ou facilmente acessíveis, reduzindo a necessidade de memorização.
7. **Flexibilidade e eficiência de uso:** a interface deve oferecer formas eficientes de realizar tarefas, atendendo tanto usuários iniciantes quanto experientes.
8. **Estética e design minimalista:** as informações apresentadas devem ser relevantes para a tarefa, evitando elementos desnecessários e excesso de informações.
9. **Reconhecimento, diagnóstico e recuperação de erros:** mensagens de erro devem ser claras, explicar o problema e orientar o usuário sobre como recuperar-se.
10. **Ajuda e documentação:** quando necessário, o sistema deve oferecer informações que auxiliem o usuário a compreender funcionalidades, indicadores e procedimentos.

## Cobertura especial para interfaces administrativas e analíticas

Por se tratar de uma interface voltada ao acompanhamento e à análise de execuções, a inspeção também considera aspectos específicos desse contexto:

- Clareza dos indicadores e das unidades de medida apresentados.
- Consistência das informações entre o painel principal e as telas de comparação.
- Identificação das condições utilizadas durante o treinamento.
- Facilidade para localizar execuções e consultar seus resultados.
- Clareza na apresentação de dados ausentes ou não confirmados.
- Diferenciação entre ausência de resultados, falhas de carregamento e erros.
- Facilidade de interpretação das informações apresentadas em gráficos, indicadores e comparações.

## 2. Escopo da inspeção

| Item | Definição |
|---|---|
| Versão avaliada | Protótipo da Entrega 11 — Figma IHC |
| Link do protótipo | [Protótipo no Figma](https://www.figma.com/proto/qHpoJxQF4Sthdy99w7Scul/IHC?node-id=32-2023&t=MJOhlZgAfoJJp8Dt-1&scaling=min-zoom&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=32%3A2023) |
| Telas/estados | P01 — Painel principal; P03 — Comparação; P06 — Confirmação; P09 — Filtros sem resultados; P10 — Estado vazio; telas 02, 03, 04, 05, 06, 07, 09, 15, 18, 21, 29, 33, 37, 42, 43 e 45. |
| Fluxos | Localização de treinamentos; seleção de execuções; consulta de indicadores; comparação de execuções; confirmação de registros; aplicação de filtros; tratamento de resultados vazios e recuperação de erros. |
| Dispositivo/viewport | Inspeção do protótipo no Figma. Resolução específica não registrada. |
| Avaliadores | Manuella Filipe Peres; Letizia Lowatzki Baptistella; Rafaela Altheman de Campos. |

A inspeção contempla os estados vazios, de erro, de ausência de resultados e de confirmação presentes no protótipo. Os estados de carregamento e de permissões não foram avaliados nesta inspeção.

## 3. Procedimento individual

Cada integrante deve realizar a inspeção das telas e dos estados relevantes do protótipo, utilizando as dez heurísticas de Nielsen como referência. Durante a avaliação, devem ser observados os elementos da interface, as informações apresentadas, os caminhos de navegação e os retornos fornecidos pelo sistema.

Os problemas identificados devem ser registrados com um identificador, a heurística relacionada, a tela ou o estado em que aparecem, a descrição do problema, a evidência, a severidade e uma recomendação de melhoria.

Quando não houver violação identificada em determinada heurística, deve ser registrado um exemplo de boa prática observado na interface.

### Escala de severidade (0–4)

| Severidade | Classificação | Descrição |
|---|---|---|
| 0 | Sem problema | Não foi identificada violação da heurística. |
| 1 | Cosmético | Problema visual ou textual de baixo impacto, sem prejudicar significativamente a tarefa. |
| 2 | Pequeno | Problema que pode causar alguma dificuldade, mas permite que o usuário conclua a tarefa. |
| 3 | Grave | Problema que prejudica significativamente a compreensão ou a execução de uma tarefa. |
| 4 | Catastrófico | Problema crítico que pode comprometer a tarefa ou levar a uma interpretação incorreta importante. |

---

## Avaliador A01 — Manuella Filipe Peres

### 4. Matriz de cobertura das 10 heurísticas

| Heurística | Telas/fluxos examinados | Houve violação? | IDs dos achados | Exemplo de boa prática se não violada |
|---|---|---|---|---|
| H1 — Visibilidade do estado do sistema | P06; telas 07, 09 e 21 — confirmação de registros. | Não | — | As telas de confirmação apresentam retorno após a realização da ação, permitindo identificar que o registro foi confirmado. |
| H2 — Correspondência entre o sistema e o mundo real | P01 — painel principal; P03 — comparação; tela 04 — comparação de métricas e parâmetros. | Sim | V01 | — |
| H3 — Controle e liberdade do usuário | Tela 15 — apresentação de indicadores; tela 43 — consulta de evidências; tela 45 — recuperação de erro. | Não | — | A interface apresenta caminhos para consultar informações e recuperar-se de situações de erro. |
| H4 — Consistência e padronização | P01; P03; telas 04 e 05 — comparação de execuções e condições de treinamento. | Sim | V01, V02 | — |
| H5 — Prevenção de erros | P03; telas 05 e 06 — comparação e confirmação. | Sim | V02 | — |
| H6 — Reconhecimento em vez de memorização | Tela 02 — localização de treinamento; tela 03 — seleção de execuções; tela 43 — consulta de evidências. | Não | — | As informações e opções necessárias são apresentadas na interface, reduzindo a necessidade de memorização. |
| H7 — Flexibilidade e eficiência de uso | Tela 02 — localização de treinamento; tela 04 — comparação de métricas; telas 15 a 18 — apresentação de indicadores. | Não | — | A organização das telas permite consultar informações e indicadores relacionados às execuções. |
| H8 — Estética e design minimalista | P01 — painel principal; P03 — comparação; P10 — estado vazio. | Sim | V03 | — |
| H9 — Reconhecimento, diagnóstico e recuperação de erros | P09; tela 29 — ausência de resultados; tela 33 — correção e nova tentativa; tela 45 — recuperação de erro. | Não | — | As mensagens e os estados apresentados permitem reconhecer situações de ausência de resultados e erros. |
| H10 — Ajuda e documentação | Tela 02 — localização de treinamento; tela 05 — comparação; tela 37 — investigação de dados ausentes. | Não | — | A organização das informações e dos elementos da interface auxilia a compreensão das funcionalidades. |

### 5. Declaração de violações

| ID | Heurística | Tela/estado | Problema observado | Evidência | Severidade | Justificativa da severidade | Recomendação |
|---|---|---|---|---|---|---|---|
| V01 | H2 — Correspondência entre o sistema e o mundo real; H4 — Consistência e padronização. | P01, P03 e tela 04. | A velocidade da execução EXEC-104 aparece com valores e unidades inconsistentes. No painel principal, é apresentada como “0,32 m/s”, enquanto na comparação aparece como “0.32 cm/s”. | Comparação entre as informações de velocidade apresentadas em P01, P03 e tela 04. | 4 | A divergência de unidade pode alterar completamente a interpretação do indicador e comprometer a comparação entre execuções. | Padronizar a unidade de velocidade em todas as telas, verificar o valor apresentado e manter a mesma convenção de representação numérica. |
| V02 | H4 — Consistência e padronização; H5 — Prevenção de erros. | P03 e telas 04 e 05. | A interface apresenta informações ambíguas sobre as condições de treinamento. Em P03 aparece “Diferença de configuração: Nenhuma”, enquanto na tela 04 aparece “Condições de treinamento: não confirmadas” e na tela 05 “Condições não confirmadas”. | Textos apresentados nas telas de comparação de execuções. | 3 | A informação pode levar o usuário a interpretar que as configurações são iguais, mesmo quando não foi possível confirmar as condições utilizadas. | Diferenciar claramente a ausência de diferenças identificadas da ausência de confirmação das condições. Quando os dados não estiverem disponíveis, informar que não foi possível verificar a equivalência. |
| V03 | H8 — Estética e design minimalista. | P10 — estado vazio. | A mensagem apresentada contém um erro de digitação: “Não há resultados dsponíveis no período escolhido”. | Mensagem exibida no estado vazio de P10. | 1 | O problema não impede a compreensão da mensagem, mas prejudica o acabamento textual e a qualidade percebida da interface. | Corrigir a palavra “dsponíveis” para “disponíveis”. |

**Qualidade do relato:** Os achados foram descritos com identificação, localização, evidência, severidade e recomendação. As violações priorizadas estão relacionadas principalmente à consistência e à interpretação dos dados apresentados pela interface.

### Evidências da avaliação — Avaliador A01

**V01 — Inconsistência na unidade de velocidade**

<!-- INSERIR PRINT 01: P01 — Painel principal, mostrando a velocidade da execução EXEC-104 como 0,32 m/s. -->

<!-- INSERIR PRINT 02: P03 — Comparação, mostrando a velocidade da execução EXEC-104 como 0.32 cm/s. -->

<!-- INSERIR PRINT 03: Tela 04 — Comparação de métricas e condições de treinamento não confirmadas. -->

**V02 — Ambiguidade nas condições de treinamento**

<!-- INSERIR PRINT 04: Tela 05 — Exibição da mensagem "Condições não confirmadas". -->

**V03 — Erro de digitação no estado vazio**

<!-- INSERIR PRINT 05: P10 — Estado vazio, mostrando a mensagem "Não há resultados dsponíveis no período escolhido". -->

### 6. Boas práticas — heurísticas não violadas (atividade didática)

| Heurística sem violação | Exemplo no sistema | Evidência | Por que atende |
|---|---|---|---|
| H1 — Visibilidade do estado do sistema | Telas de confirmação de registros. | P06; telas 07, 09 e 21. | O sistema apresenta um retorno após a confirmação, permitindo que o usuário reconheça o resultado da ação. |
| H3 — Controle e liberdade do usuário | Consulta de evidências e recuperação de situações de erro. | Telas 15, 43 e 45. | A interface oferece caminhos para consultar informações e lidar com situações inesperadas. |
| H6 — Reconhecimento em vez de memorização | Localização de treinamentos e seleção de execuções. | Telas 02 e 03. | As opções necessárias são apresentadas na interface, facilitando a identificação das funcionalidades. |
| H7 — Flexibilidade e eficiência de uso | Consulta de métricas e indicadores. | Tela 04 e telas 15 a 18. | A organização das informações permite que o usuário consulte diferentes indicadores relacionados às execuções. |
| H9 — Reconhecimento, diagnóstico e recuperação de erros | Estados sem resultados e mensagens de erro. | P09; telas 29, 33 e 45. | A interface apresenta estados específicos para situações de ausência de resultados e erro, facilitando o reconhecimento do problema. |
| H10 — Ajuda e documentação | Organização das informações sobre treinamentos, comparações e dados ausentes. | Telas 02, 05 e 37. | A apresentação contextual das informações auxilia o entendimento das funcionalidades disponíveis. |

---

## Avaliador A02 — Letizia Lowatzki Baptistella

### 4. Matriz de cobertura das 10 heurísticas

| Heurística | Telas/fluxos examinados | Houve violação? | IDs dos achados | Exemplo de boa prática se não violada |
|---|---|---|---|---|
| H1 — Visibilidade do estado do sistema | P06; telas 07, 09 e 21 — confirmação de registros. | Não | — | As telas de confirmação apresentam retorno após a realização da ação, permitindo identificar que o registro foi confirmado. |
| H2 — Correspondência entre o sistema e o mundo real | P01 — painel principal; P03 — comparação; tela 04 — comparação de métricas e parâmetros. | Sim | V01 | — |
| H3 — Controle e liberdade do usuário | Tela 15 — apresentação de indicadores; tela 43 — consulta de evidências; tela 45 — recuperação de erro. | Não | — | A interface apresenta caminhos para consultar informações e recuperar-se de situações de erro. |
| H4 — Consistência e padronização | P01; P03; telas 04 e 05 — comparação de execuções e condições de treinamento. | Sim | V01, V02 | — |
| H5 — Prevenção de erros | P03; telas 05 e 06 — comparação e confirmação. | Sim | V02 | — |
| H6 — Reconhecimento em vez de memorização | Tela 02 — localização de treinamento; tela 03 — seleção de execuções; tela 43 — consulta de evidências. | Não | — | As informações e opções necessárias são apresentadas na interface, reduzindo a necessidade de memorização. |
| H7 — Flexibilidade e eficiência de uso | Tela 02 — localização de treinamento; tela 04 — comparação de métricas; telas 15 a 18 — apresentação de indicadores. | Não | — | A organização das telas permite consultar informações e indicadores relacionados às execuções. |
| H8 — Estética e design minimalista | P01 — painel principal; P03 — comparação; P10 — estado vazio. | Sim | V03 | — |
| H9 — Reconhecimento, diagnóstico e recuperação de erros | P09; tela 29 — ausência de resultados; tela 33 — correção e nova tentativa; tela 45 — recuperação de erro. | Não | — | As mensagens e os estados apresentados permitem reconhecer situações de ausência de resultados e erros. |
| H10 — Ajuda e documentação | Tela 02 — localização de treinamento; tela 05 — comparação; tela 37 — investigação de dados ausentes. | Não | — | A organização das informações e dos elementos da interface auxilia a compreensão das funcionalidades. |

### 5. Declaração de violações

| ID | Heurística | Tela/estado | Problema observado | Evidência | Severidade | Justificativa da severidade | Recomendação |
|---|---|---|---|---|---|---|---|
| V01 | H2 — Correspondência entre o sistema e o mundo real; H4 — Consistência e padronização. | P01, P03 e tela 04. | A velocidade da execução EXEC-104 aparece com valores e unidades inconsistentes. No painel principal, é apresentada como “0,32 m/s”, enquanto na comparação aparece como “0.32 cm/s”. | Comparação entre as informações de velocidade apresentadas em P01, P03 e tela 04. | 4 | A divergência de unidade pode alterar completamente a interpretação do indicador e comprometer a comparação entre execuções. | Padronizar a unidade de velocidade em todas as telas, verificar o valor apresentado e manter a mesma convenção de representação numérica. |
| V02 | H4 — Consistência e padronização; H5 — Prevenção de erros. | P03 e telas 04 e 05. | A interface apresenta informações ambíguas sobre as condições de treinamento. Em P03 aparece “Diferença de configuração: Nenhuma”, enquanto na tela 04 aparece “Condições de treinamento: não confirmadas” e na tela 05 “Condições não confirmadas”. | Textos apresentados nas telas de comparação de execuções. | 3 | A informação pode levar o usuário a interpretar que as configurações são iguais, mesmo quando não foi possível confirmar as condições utilizadas. | Diferenciar claramente a ausência de diferenças identificadas da ausência de confirmação das condições. Quando os dados não estiverem disponíveis, informar que não foi possível verificar a equivalência. |
| V03 | H8 — Estética e design minimalista. | P10 — estado vazio. | A mensagem apresentada contém um erro de digitação: “Não há resultados dsponíveis no período escolhido”. | Mensagem exibida no estado vazio de P10. | 1 | O problema não impede a compreensão da mensagem, mas prejudica o acabamento textual e a qualidade percebida da interface. | Corrigir a palavra “dsponíveis” para “disponíveis”. |

**Qualidade do relato:** Os problemas identificados possuem localização definida e estão associados às heurísticas correspondentes. As recomendações propostas buscam melhorar a consistência das informações, evitar interpretações equivocadas e aprimorar a comunicação textual.

### Evidências da avaliação — Avaliador A02

**V01 — Inconsistência na unidade de velocidade**

<!-- INSERIR PRINT 01: P01 — Painel principal, mostrando a velocidade da execução EXEC-104 como 0,32 m/s. -->

<!-- INSERIR PRINT 02: P03 — Comparação, mostrando a velocidade da execução EXEC-104 como 0.32 cm/s. -->

<!-- INSERIR PRINT 03: Tela 04 — Comparação de métricas e condições de treinamento não confirmadas. -->

**V02 — Ambiguidade nas condições de treinamento**

<!-- INSERIR PRINT 04: Tela 05 — Exibição da mensagem "Condições não confirmadas". -->

**V03 — Erro de digitação no estado vazio**

<!-- INSERIR PRINT 05: P10 — Estado vazio, mostrando a mensagem "Não há resultados dsponíveis no período escolhido". -->

### 6. Boas práticas — heurísticas não violadas (atividade didática)

| Heurística sem violação | Exemplo no sistema | Evidência | Por que atende |
|---|---|---|---|
| H1 — Visibilidade do estado do sistema | Telas de confirmação de registros. | P06; telas 07, 09 e 21. | O sistema apresenta um retorno após a confirmação, permitindo que o usuário reconheça o resultado da ação. |
| H3 — Controle e liberdade do usuário | Consulta de evidências e recuperação de situações de erro. | Telas 15, 43 e 45. | A interface oferece caminhos para consultar informações e lidar com situações inesperadas. |
| H6 — Reconhecimento em vez de memorização | Localização de treinamentos e seleção de execuções. | Telas 02 e 03. | As opções necessárias são apresentadas na interface, facilitando a identificação das funcionalidades. |
| H7 — Flexibilidade e eficiência de uso | Consulta de métricas e indicadores. | Tela 04 e telas 15 a 18. | A organização das informações permite que o usuário consulte diferentes indicadores relacionados às execuções. |
| H9 — Reconhecimento, diagnóstico e recuperação de erros | Estados sem resultados e mensagens de erro. | P09; telas 29, 33 e 45. | A interface apresenta estados específicos para situações de ausência de resultados e erro, facilitando o reconhecimento do problema. |
| H10 — Ajuda e documentação | Organização das informações sobre treinamentos, comparações e dados ausentes. | Telas 02, 05 e 37. | A apresentação contextual das informações auxilia o entendimento das funcionalidades disponíveis. |

---

## Avaliador A03 — Rafaela Altheman de Campos

### 4. Matriz de cobertura das 10 heurísticas

| Heurística | Telas/fluxos examinados | Houve violação? | IDs dos achados | Exemplo de boa prática se não violada |
|---|---|---|---|---|
| H1 — Visibilidade do estado do sistema | P06; telas 07, 09 e 21 — confirmação de registros. | Não | — | As telas de confirmação apresentam retorno após a realização da ação, permitindo identificar que o registro foi confirmado. |
| H2 — Correspondência entre o sistema e o mundo real | P01 — painel principal; P03 — comparação; tela 04 — comparação de métricas e parâmetros. | Sim | V01 | — |
| H3 — Controle e liberdade do usuário | Tela 15 — apresentação de indicadores; tela 43 — consulta de evidências; tela 45 — recuperação de erro. | Não | — | A interface apresenta caminhos para consultar informações e recuperar-se de situações de erro. |
| H4 — Consistência e padronização | P01; P03; telas 04 e 05 — comparação de execuções e condições de treinamento. | Sim | V01, V02 | — |
| H5 — Prevenção de erros | P03; telas 05 e 06 — comparação e confirmação. | Sim | V02 | — |
| H6 — Reconhecimento em vez de memorização | Tela 02 — localização de treinamento; tela 03 — seleção de execuções; tela 43 — consulta de evidências. | Não | — | As informações e opções necessárias são apresentadas na interface, reduzindo a necessidade de memorização. |
| H7 — Flexibilidade e eficiência de uso | Tela 02 — localização de treinamento; tela 04 — comparação de métricas; telas 15 a 18 — apresentação de indicadores. | Não | — | A organização das telas permite consultar informações e indicadores relacionados às execuções. |
| H8 — Estética e design minimalista | P01 — painel principal; P03 — comparação; P10 — estado vazio. | Sim | V03 | — |
| H9 — Reconhecimento, diagnóstico e recuperação de erros | P09; tela 29 — ausência de resultados; tela 33 — correção e nova tentativa; tela 45 — recuperação de erro. | Não | — | As mensagens e os estados apresentados permitem reconhecer situações de ausência de resultados e erros. |
| H10 — Ajuda e documentação | Tela 02 — localização de treinamento; tela 05 — comparação; tela 37 — investigação de dados ausentes. | Não | — | A organização das informações e dos elementos da interface auxilia a compreensão das funcionalidades. |

### 5. Declaração de violações

| ID | Heurística | Tela/estado | Problema observado | Evidência | Severidade | Justificativa da severidade | Recomendação |
|---|---|---|---|---|---|---|---|
| V01 | H2 — Correspondência entre o sistema e o mundo real; H4 — Consistência e padronização. | P01, P03 e tela 04. | A velocidade da execução EXEC-104 aparece com valores e unidades inconsistentes. No painel principal, é apresentada como “0,32 m/s”, enquanto na comparação aparece como “0.32 cm/s”. | Comparação entre as informações de velocidade apresentadas em P01, P03 e tela 04. | 4 | A divergência de unidade pode alterar completamente a interpretação do indicador e comprometer a comparação entre execuções. | Padronizar a unidade de velocidade em todas as telas, verificar o valor apresentado e manter a mesma convenção de representação numérica. |
| V02 | H4 — Consistência e padronização; H5 — Prevenção de erros. | P03 e telas 04 e 05. | A interface apresenta informações ambíguas sobre as condições de treinamento. Em P03 aparece “Diferença de configuração: Nenhuma”, enquanto na tela 04 aparece “Condições de treinamento: não confirmadas” e na tela 05 “Condições não confirmadas”. | Textos apresentados nas telas de comparação de execuções. | 3 | A informação pode levar o usuário a interpretar que as configurações são iguais, mesmo quando não foi possível confirmar as condições utilizadas. | Diferenciar claramente a ausência de diferenças identificadas da ausência de confirmação das condições. Quando os dados não estiverem disponíveis, informar que não foi possível verificar a equivalência. |
| V03 | H8 — Estética e design minimalista. | P10 — estado vazio. | A mensagem apresentada contém um erro de digitação: “Não há resultados dsponíveis no período escolhido”. | Mensagem exibida no estado vazio de P10. | 1 | O problema não impede a compreensão da mensagem, mas prejudica o acabamento textual e a qualidade percebida da interface. | Corrigir a palavra “dsponíveis” para “disponíveis”. |

**Qualidade do relato:** Os achados foram organizados de acordo com as heurísticas violadas, considerando o impacto dos problemas na compreensão dos dados e na utilização da interface. As recomendações priorizam a correção de inconsistências que podem comprometer a interpretação dos resultados.

### Evidências da avaliação — Avaliador A03

**V01 — Inconsistência na unidade de velocidade**

<!-- INSERIR PRINT 01: P01 — Painel principal, mostrando a velocidade da execução EXEC-104 como 0,32 m/s. -->

<!-- INSERIR PRINT 02: P03 — Comparação, mostrando a velocidade da execução EXEC-104 como 0.32 cm/s. -->

<!-- INSERIR PRINT 03: Tela 04 — Comparação de métricas e condições de treinamento não confirmadas. -->

**V02 — Ambiguidade nas condições de treinamento**

<!-- INSERIR PRINT 04: Tela 05 — Exibição da mensagem "Condições não confirmadas". -->

**V03 — Erro de digitação no estado vazio**

<!-- INSERIR PRINT 05: P10 — Estado vazio, mostrando a mensagem "Não há resultados dsponíveis no período escolhido". -->

### 6. Boas práticas — heurísticas não violadas (atividade didática)

| Heurística sem violação | Exemplo no sistema | Evidência | Por que atende |
|---|---|---|---|
| H1 — Visibilidade do estado do sistema | Telas de confirmação de registros. | P06; telas 07, 09 e 21. | O sistema apresenta um retorno após a confirmação, permitindo que o usuário reconheça o resultado da ação. |
| H3 — Controle e liberdade do usuário | Consulta de evidências e recuperação de situações de erro. | Telas 15, 43 e 45. | A interface oferece caminhos para consultar informações e lidar com situações inesperadas. |
| H6 — Reconhecimento em vez de memorização | Localização de treinamentos e seleção de execuções. | Telas 02 e 03. | As opções necessárias são apresentadas na interface, facilitando a identificação das funcionalidades. |
| H7 — Flexibilidade e eficiência de uso | Consulta de métricas e indicadores. | Tela 04 e telas 15 a 18. | A organização das informações permite que o usuário consulte diferentes indicadores relacionados às execuções. |
| H9 — Reconhecimento, diagnóstico e recuperação de erros | Estados sem resultados e mensagens de erro. | P09; telas 29, 33 e 45. | A interface apresenta estados específicos para situações de ausência de resultados e erro, facilitando o reconhecimento do problema. |
| H10 — Ajuda e documentação | Organização das informações sobre treinamentos, comparações e dados ausentes. | Telas 02, 05 e 37. | A apresentação contextual das informações auxilia o entendimento das funcionalidades disponíveis. |

---

## 7. Consolidação da equipe

A inspeção identificou três problemas principais na interface, relacionados à apresentação dos indicadores, à consistência das informações de treinamento e à qualidade textual de uma mensagem de estado vazio.

| ID | Heurística(s) | Problema | Telas afetadas | Severidade | Prioridade | Encaminhamento |
|---|---|---|---|---|---|---|
| V01 | H2 e H4 | Inconsistência na unidade de velocidade da execução EXEC-104. | P01, P03 e tela 04. | 4 | Alta | Padronizar a unidade e verificar os valores apresentados em todas as telas. |
| V02 | H4 e H5 | Ambiguidade na indicação das condições de treinamento. | P03 e telas 04 e 05. | 3 | Alta | Diferenciar ausência de diferenças identificadas de condições não confirmadas. |
| V03 | H8 | Erro de digitação na mensagem do estado vazio. | P10. | 1 | Baixa | Corrigir o texto da mensagem. |

### Análise da consolidação

O problema V01 apresenta a maior severidade, pois envolve uma informação quantitativa utilizada para interpretar o desempenho de uma execução. A utilização de unidades diferentes para o mesmo indicador pode provocar uma leitura incorreta dos resultados e comprometer comparações.

O problema V02 também exige atenção, pois a interface utiliza mensagens que podem transmitir interpretações diferentes sobre as condições de treinamento. A ausência de confirmação das condições não deve ser apresentada como se fosse uma confirmação de igualdade entre configurações.

O problema V03 possui menor impacto funcional, mas deve ser corrigido para melhorar a qualidade textual e a apresentação da interface.

A equipe deve priorizar a correção de V01 e V02 antes de considerar a interface pronta para uma avaliação final. V03 pode ser corrigido juntamente com os demais ajustes textuais.

## 8. Síntese e plano de melhoria

A avaliação heurística permitiu identificar problemas de usabilidade relacionados principalmente à consistência e à interpretação das informações apresentadas pelo sistema. Como a interface possui caráter administrativo e analítico, a precisão dos indicadores e a clareza das condições utilizadas nas comparações são fundamentais.

O principal problema identificado foi a divergência na unidade de velocidade da execução EXEC-104, que pode comprometer a interpretação dos dados. Também foi identificada ambiguidade na apresentação das condições de treinamento, além de um erro de digitação em uma mensagem de estado vazio.

O plano de melhoria proposto é:

| Ordem | Ação de melhoria | Problema relacionado | Resultado esperado |
|---|---|---|---|
| 1 | Padronizar a unidade de velocidade em todas as telas e revisar os valores apresentados. | V01 | Garantir que o indicador seja apresentado de maneira consistente e compreensível. |
| 2 | Revisar os textos referentes às condições de treinamento e diferenciar informações confirmadas de informações não verificadas. | V02 | Evitar interpretações equivocadas durante a comparação de execuções. |
| 3 | Corrigir o erro de digitação na mensagem do estado vazio. | V03 | Melhorar a qualidade textual e a apresentação da interface. |
| 4 | Realizar nova inspeção nas telas alteradas após a implementação das correções. | V01, V02 e V03 | Verificar se os problemas foram resolvidos e se não surgiram novas inconsistências. |
| 5 | Avaliar os estados de carregamento e permissões, que não fizeram parte da inspeção registrada. | Cobertura complementar | Ampliar a cobertura da avaliação para estados ainda não examinados. |

A avaliação demonstra que a interface possui elementos que auxiliam a consulta de informações, a confirmação de registros e o reconhecimento de estados de erro e ausência de resultados. Entretanto, os problemas encontrados mostram que a consistência dos indicadores e a clareza das mensagens precisam ser aprimoradas para garantir uma interpretação confiável dos dados.

## Checklist

- [x] As dez heurísticas de Nielsen foram consideradas.
- [x] O escopo da inspeção foi identificado.
- [x] Foram considerados estados vazios, de erro, de ausência de resultados e de confirmação.
- [x] Os problemas identificados receberam identificadores.
- [x] Os achados apresentam heurística, tela, descrição, evidência, severidade e recomendação.
- [x] Foi utilizada uma escala de severidade de 0 a 4.
- [x] Foram registrados exemplos de boas práticas para heurísticas sem violações identificadas.
- [x] Os achados foram organizados em uma consolidação da equipe.
- [x] Foi elaborado um plano de melhoria.
- [ ] Os prints de evidência foram inseridos no repositório.
- [ ] As avaliações individuais independentes de cada integrante foram registradas e validadas.
- [ ] Os estados de carregamento e permissões foram avaliados.
- [ ] As correções foram implementadas e verificadas em uma nova inspeção.

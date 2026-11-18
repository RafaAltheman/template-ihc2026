
# Entrega 13 — Avaliação de IHC por inspeção heurística

**Data:** 17/11/2026  
**Status:** Inspeção documentada — validação individual e reinspeção pós-correções pendentes  
**Responsabilidade:** Avaliação da interface pelos integrantes da equipe.

**Equipe 27:**
- Letizia Lowatzki Baptistella — 22.125.063-2
- Manuella Filipe Peres — 22.224.029-3
- Rafaela Altheman de Campos — 22.125.062-4

## Objetivo da atividade

Encontrar problemas de usabilidade por inspeção sistemática da interface com as **10 heurísticas de Nielsen**. Cada avaliador trabalha individualmente primeiro; depois a equipe consolida problemas duplicados e prioridades.

> **Parte de violações:** registre somente problemas reais. Não invente uma violação para “preencher” cada heurística. Para provar que todas foram exercitadas, use a **matriz de cobertura H1–H10**. Para heurísticas sem violação, a disciplina solicita um exemplo didático de boa prática.

A avaliação contempla o protótipo da plataforma de análise de resultados de treinamentos de robôs humanoides, desenvolvido na Entrega 11.

O objetivo é identificar problemas de interação que possam comprometer a localização de execuções, a interpretação de indicadores, a comparação entre treinamentos, o registro de avaliações e hipóteses e a apresentação de evidências durante reuniões.

A inspeção considera os fluxos T01, T02 e T03, os cenários da Entrega 9, os diagramas MoLIC da Entrega 10 e as metas de usabilidade da Entrega 8.

## 1. Heurísticas adotadas

Foram utilizadas as dez heurísticas de Nielsen:

| Código | Heurística | Descrição |
|---|---|---|
| H1 | Visibilidade do estado do sistema | O sistema deve manter o usuário informado sobre o que está acontecendo, por meio de mensagens e indicadores apropriados. |
| H2 | Correspondência entre o sistema e o mundo real | A interface deve utilizar termos, conceitos e informações familiares ao usuário. |
| H3 | Controle e liberdade do usuário | O usuário deve conseguir desfazer ações indesejadas e retornar de situações inesperadas. |
| H4 | Consistência e padronização | Elementos semelhantes devem seguir os mesmos padrões de apresentação e comportamento. |
| H5 | Prevenção de erros | A interface deve prevenir problemas antes que eles aconteçam. |
| H6 | Reconhecimento em vez de memorização | As informações e opções devem estar visíveis, reduzindo a necessidade de memorização. |
| H7 | Flexibilidade e eficiência de uso | A interface deve oferecer recursos que facilitem a utilização por usuários com diferentes níveis de experiência. |
| H8 | Estética e design minimalista | A interface deve apresentar somente informações relevantes, evitando excesso de elementos. |
| H9 | Reconhecimento, diagnóstico e recuperação de erros | As mensagens de erro devem ser compreensíveis e indicar como o usuário pode resolver o problema. |
| H10 | Ajuda e documentação | A interface deve oferecer informações que auxiliem o usuário a compreender e utilizar o sistema. |

### Cobertura especial para interfaces administrativas e analíticas

Além das heurísticas gerais, foram considerados os seguintes aspectos:

- Clareza dos indicadores apresentados.
- Padronização das unidades de medida.
- Facilidade para comparar diferentes execuções.
- Identificação das condições de treinamento.
- Clareza das mensagens de erro e dos estados vazios.
- Compreensão dos resultados apresentados.
- Facilidade para localizar informações relevantes.

## 2. Escopo da inspeção

A inspeção considerou o protótipo desenvolvido no Figma para a Entrega 11.

**Protótipo utilizado:**

https://www.figma.com/proto/qHpoJxQF4Sthdy99w7Scul/IHC?node-id=32-2023&p=f&scaling=min-zoom&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=32%3A2023

**Versão avaliada:** Protótipo da Entrega 11 — Figma IHC.

**Data de referência:** 17/11/2026.

Foram considerados os seguintes elementos e estados da interface:

| Elemento | Aspectos avaliados |
|---|---|
| P01 — Painel geral | Apresentação dos indicadores e síntese dos treinamentos. |
| P02 — Histórico | Busca, filtros e localização de execuções anteriores. |
| P03 — Comparação de execuções | Comparação entre métricas e informações de configuração. |
| P04 — Hipótese e ressalvas | Registro de hipóteses e limitações das comparações. |
| P05 — Avaliar treinamento | Interpretação dos resultados e escolha de classificação. |
| P06 — Confirmar registro | Feedback após o salvamento de avaliações. |
| P07 — Reunião | Apresentação e acompanhamento dos resultados. |
| P08 — Evidência detalhada | Consulta de informações complementares. |
| P09 — Busca sem resultados | Recuperação de pesquisas sem correspondência. |
| P10 — Painel sem dados do período | Tratamento de estados vazios. |
| Tela 04 — Comparar métricas e parâmetros | Comparação detalhada entre execuções. |
| Tela 05 — Verificar comparabilidade | Identificação de condições não confirmadas. |
| Tela 06 — Registrar hipótese e ressalvas | Registro de interpretações e limitações. |
| Tela 07 — Conferir hipótese registrada | Confirmação do salvamento da hipótese. |
| Tela 15 — Apresentar indicadores | Apresentação da velocidade média. |
| Tela 29 — Busca sem resultados | Mensagem e opções de recuperação. |
| Tela 33 — Corrigir ou tentar novamente | Recuperação de erro na avaliação. |
| Tela 37 — Investigar dado não registrado | Orientação sobre informações ausentes. |
| Tela 43 — Observar evidência da execução | Consulta de evidência e preservação do contexto. |
| Tela 45 — Recuperar erro de registro | Tratamento de falhas de salvamento. |

Também foram considerados os seguintes estados:

- **Estado vazio:** P10 e tela 42.
- **Estado de erro:** telas 33 e 45.
- **Pesquisa sem resultados:** P09 e tela 29.
- **Confirmação:** P06 e telas 07, 09 e 21.
- **Condições não confirmadas:** telas 04 e 05.

Os estados de carregamento e permissões não fizeram parte do escopo documentado desta inspeção.

## 3. Procedimento de avaliação

A avaliação foi estruturada a partir das dez heurísticas de Nielsen.

Para cada heurística, foram considerados os elementos da interface relacionados ao seu princípio, buscando identificar situações que pudessem dificultar a compreensão, a navegação ou a realização das atividades pelo usuário.

Os problemas identificados foram registrados com:

- Identificação do problema.
- Heurística relacionada.
- Tela ou elemento em que ocorre.
- Descrição da inconsistência.
- Impacto para o usuário.
- Severidade.
- Recomendação de melhoria.

### Organização das análises individuais

O documento está organizado em três perspectivas de inspeção:

- **A01 — Manuella:** interpretação de indicadores, coerência das métricas e confiabilidade das informações.
- **A02 — Letizia:** navegação entre tarefas, comparação de execuções e prevenção de decisões equivocadas.
- **A03 — Rafaela:** clareza das mensagens, feedback, estados de erro e continuidade da interação.

Essas perspectivas organizam as avaliações, mas não substituem a realização e a confirmação das inspeções individuais pelas integrantes.

Os problemas identificados recebem os mesmos IDs quando representam a mesma ocorrência, permitindo sua consolidação sem duplicações artificiais.

### Escala de severidade

Foi utilizada uma escala de 0 a 4:

| Severidade | Classificação | Descrição |
|---|---|---|
| 0 | Sem problema | Não foi identificada violação da heurística. |
| 1 | Cosmético | Problema visual ou textual de baixo impacto. |
| 2 | Pequeno | Problema que pode causar alguma dificuldade, mas não impede a utilização. |
| 3 | Grave | Problema que pode prejudicar significativamente a compreensão ou a realização de uma atividade. |
| 4 | Catastrófico | Problema que pode comprometer a interpretação dos dados ou impedir uma atividade importante. |

---

# Avaliador A01 — Manuella Filipe Peres

**Foco da análise:** consistência das métricas, interpretação dos resultados e confiabilidade das informações apresentadas na interface.

**Situação:** registro preparado para validação pela avaliadora.

## 4. Matriz de cobertura das 10 heurísticas

| Heurística | Elementos analisados | Resultado |
|---|---|---|
| H1 — Visibilidade do estado do sistema | P05, P06 e telas 07 e 09 | As confirmações identificam o registro concluído e a execução correspondente. Nenhuma violação específica foi identificada nesses elementos. |
| H2 — Correspondência entre o sistema e o mundo real | P01, P03, tela 04 e P10 | V01: utilização de unidades inconsistentes para a velocidade. V03: erro textual na mensagem do estado vazio. |
| H3 — Controle e liberdade do usuário | P03, P05 e tela 43 | Foram identificados controles de retorno e revisão da análise. Nenhuma violação específica foi confirmada. |
| H4 — Consistência e padronização | P01, P03 e telas 04 e 05 | V01: divergência nas unidades. V02: comunicação inconsistente sobre as condições da comparação. |
| H5 — Prevenção de erros | P03 e tela 05 | V02: risco de interpretar condições não verificadas como equivalentes. |
| H6 — Reconhecimento em vez de memorização | P02, P03 e tela 03 | Os identificadores das execuções e a seleção atual são apresentados na interface. |
| H7 — Flexibilidade e eficiência de uso | P02 e telas 02 e 04 | Busca por ID, filtros e comparação lado a lado oferecem alternativas para consultar os resultados. |
| H8 — Estética e design minimalista | P01, P03 e tela 04 | As métricas são agrupadas por execução e indicador. Nenhuma violação específica de minimalismo foi confirmada. |
| H9 — Reconhecimento, diagnóstico e recuperação de erros | P09 e telas 29 e 33 | A interface apresenta mensagens de erro e opções para revisar a ação. |
| H10 — Ajuda e documentação | Telas 05 e 37 | A interface apresenta orientações sobre comparabilidade e dados não registrados. |

## 5. Declaração de violações

### V01 — Inconsistência na unidade de velocidade da execução EXEC-104

**Heurísticas relacionadas:** H2 — Correspondência entre sistema e mundo real; H4 — Consistência e padronização.

**Localização:** P01, P03 e tela 04.

**Descrição:**

Na consulta aos resultados de treinamento, a velocidade da execução EXEC-104 é apresentada como `0,32 m/s` no painel geral.

Entretanto, nas telas de comparação, o mesmo indicador é apresentado como `0.32 cm/s`.

Essa diferença não representa apenas uma alteração de formatação. Metros por segundo e centímetros por segundo são unidades diferentes, e a troca entre elas modifica a interpretação física do valor.

Como a plataforma apoia decisões técnicas sobre o desempenho do robô, é necessário que a informação seja consistente em todas as etapas da análise.

**Consequência para o usuário:**

O usuário pode comparar valores que parecem semelhantes, mas representam grandezas expressas em unidades diferentes, chegando a conclusões equivocadas sobre a evolução do treinamento.

**Severidade:** 4 — Catastrófico.

**Justificativa:**

O problema compromete a confiabilidade de um indicador utilizado para avaliar a evolução do desempenho e pode afetar decisões posteriores.

**Recomendação:**

Padronizar a unidade de velocidade em todas as telas e verificar a correspondência dos valores com a fonte dos dados antes de realizar alterações.

A unidade deve permanecer explícita nos indicadores, gráficos e tabelas de comparação.

### V02 — Ambiguidade na indicação das condições de treinamento

**Heurísticas relacionadas:** H4 e H5.

**Localização:** P03, telas 04 e 05.

**Descrição:**

A interface apresenta a expressão `Diferença de configuração: Nenhuma` na comparação.

Entretanto, outras telas informam que as condições de treinamento não foram confirmadas.

Do ponto de vista da interpretação técnica, essas afirmações não possuem o mesmo significado.

A ausência de diferenças identificadas não comprova que duas execuções utilizaram condições equivalentes, especialmente quando informações necessárias não estão disponíveis.

**Consequência para o usuário:**

O usuário pode atribuir as diferenças de desempenho exclusivamente aos resultados observados, sem considerar que as execuções talvez tenham ocorrido sob condições distintas.

**Severidade:** 3 — Grave.

**Justificativa:**

O problema pode comprometer a interpretação da comparação e reduzir a confiabilidade das conclusões registradas.

**Recomendação:**

Apresentar separadamente as informações confirmadas e aquelas que permanecem desconhecidas.

Quando não houver dados suficientes, utilizar a expressão `Condições de treinamento não confirmadas`, acompanhada de orientação para verificar as informações disponíveis.

### V03 — Erro de digitação no estado vazio

**Heurística relacionada:** H2 — Clareza da linguagem utilizada na interface.

**Localização:** P10.

**Descrição:**

A mensagem apresentada no estado vazio contém o texto:

`Não há resultados dsponíveis no período escolhido`.

O erro não altera o significado geral da mensagem, mas prejudica a qualidade da comunicação.

**Severidade:** 1 — Cosmético.

**Recomendação:**

Corrigir a palavra `dsponíveis` para `disponíveis`.

## 6. Boas práticas — heurísticas sem violações identificadas

| Heurística | Boa prática observada |
|---|---|
| H1 | A confirmação da avaliação identifica o treinamento e a referência associados ao registro. |
| H3 | A interface oferece retorno à comparação e revisão da avaliação. |
| H6 | Os IDs EXEC-104 e EXEC-103 permanecem identificados nas etapas de comparação. |
| H7 | Os dados são apresentados lado a lado, permitindo consultar múltiplos indicadores. |
| H8 | A tabela de comparação concentra informações relevantes para a análise. |
| H9 | O estado de busca sem resultados apresenta alternativas de recuperação. |
| H10 | A tela de dado não registrado informa que valores ausentes não devem ser inferidos. |

---

# Avaliador A02 — Letizia Lowatzki Baptistella

**Foco da análise:** organização dos fluxos de interação, comparação entre execuções, controle do usuário e prevenção de decisões equivocadas.

**Situação:** registro preparado para validação pela avaliadora.

## 4. Matriz de cobertura das 10 heurísticas

| Heurística | Elementos analisados | Resultado |
|---|---|---|
| H1 — Visibilidade do estado do sistema | Telas 03, 07 e 09 | A interface informa a quantidade de execuções selecionadas e apresenta confirmação após determinados registros. |
| H2 — Correspondência entre o sistema e o mundo real | P01, P03 e P10 | V01: unidade de velocidade inconsistente. V03: erro de escrita no estado vazio. |
| H3 — Controle e liberdade do usuário | Telas 03, 05, 06 e 43 | Existem opções de retorno à comparação e à apresentação, permitindo revisar etapas da interação. |
| H4 — Consistência e padronização | P03 e telas 04 e 05 | V02: mensagens diferentes podem induzir interpretações incompatíveis sobre as condições dos treinamentos. V01 também afeta a consistência das métricas. |
| H5 — Prevenção de erros | Telas 04, 05 e 06 | V02: necessidade de distinguir claramente condições verificadas e não verificadas antes do registro de hipóteses. |
| H6 — Reconhecimento em vez de memorização | Telas 02, 03 e 06 | As execuções selecionadas aparecem identificadas e os campos de hipótese e ressalvas possuem rótulos próprios. |
| H7 — Flexibilidade e eficiência de uso | Telas 02, 03 e 04 | O fluxo permite localizar execuções, selecioná-las e realizar a comparação sem depender apenas da visão geral. |
| H8 — Estética e design minimalista | Telas 04, 05 e 06 | As informações são apresentadas em etapas relacionadas à atividade, sem violação específica de minimalismo confirmada. |
| H9 — Reconhecimento, diagnóstico e recuperação de erros | Telas 29, 33 e 39 | Existem estados destinados à correção de pesquisas e à revisão de registros. |
| H10 — Ajuda e documentação | Telas 05, 06 e 37 | A interface orienta o usuário a verificar condições e não interpretar hipóteses como causalidade demonstrada. |

## 5. Declaração de violações

### V02 — Ambiguidade na indicação das condições de treinamento

**Heurísticas relacionadas:** H4 — Consistência e padronização; H5 — Prevenção de erros.

**Localização:** P03, telas 04 e 05.

**Descrição:**

Durante o fluxo de comparação entre EXEC-104 e EXEC-103, o usuário encontra diferentes informações sobre a configuração dos treinamentos.

A tela P03 informa:

`Diferença de configuração: Nenhuma`.

Entretanto, nas etapas seguintes, o sistema informa que as condições de treinamento não foram confirmadas.

O problema é relevante porque a comparação depende do reconhecimento das condições em que cada treinamento ocorreu.

O usuário pode interpretar a primeira mensagem como uma confirmação definitiva e avançar para o registro de uma hipótese sem perceber que ainda existem limitações.

**Consequência para o usuário:**

A sequência de interação pode favorecer a elaboração de uma hipótese com base em uma premissa incorreta de equivalência entre as execuções.

**Severidade:** 3 — Grave.

**Justificativa:**

A inconsistência aparece em uma etapa decisiva do fluxo, anterior ao registro de hipóteses e ressalvas.

**Recomendação:**

Substituir a afirmação de ausência de diferenças por uma comunicação compatível com as informações efetivamente disponíveis.

A tela de comparação deve informar que as condições ainda precisam ser verificadas e manter a mesma terminologia nas etapas seguintes.

O usuário deve conseguir prosseguir com uma análise exploratória, mas sem perder de vista as limitações.

### V01 — Inconsistência na unidade de velocidade

**Heurísticas relacionadas:** H2 e H4.

**Localização:** P01, P03 e tela 04.

**Descrição:**

O indicador de velocidade utiliza `m/s` no painel geral e `cm/s` nas telas de comparação.

No fluxo de interação, o usuário pode consultar primeiro o painel e depois abrir a comparação, encontrando duas representações diferentes para o mesmo indicador.

Como a navegação entre telas faz parte da tarefa T01, essa inconsistência dificulta a continuidade da análise.

**Consequência para o usuário:**

O participante pode precisar reinterpretar os números ou realizar uma conversão não prevista, aumentando o esforço cognitivo e o risco de erro.

**Severidade:** 4 — Catastrófico.

**Recomendação:**

Manter uma unidade padronizada nos diferentes pontos do fluxo, garantindo a consistência entre a visão geral e a comparação.

### V03 — Erro de digitação no estado vazio

**Heurística relacionada:** H2.

**Localização:** P10.

**Descrição:**

A mensagem de ausência de resultados apresenta a palavra `dsponíveis`.

Embora existam opções para modificar o período ou retornar ao histórico, a redação deve ser revisada para manter a qualidade do diálogo com o usuário.

**Severidade:** 1 — Cosmético.

**Recomendação:**

Corrigir a escrita e manter o padrão de linguagem utilizado nos demais estados da interface.

## 6. Boas práticas — heurísticas sem violações identificadas

| Heurística | Boa prática observada |
|---|---|
| H1 | O histórico apresenta o número de execuções selecionadas, como `Selecionadas: 2/2`. |
| H3 | A consulta de evidência possui a ação `Voltar à apresentação (mesmo ponto)`. |
| H6 | A tela de registro identifica as execuções analisadas, evitando depender da memória do usuário. |
| H7 | Busca por identificador e filtros oferecem diferentes caminhos para localizar resultados. |
| H8 | As etapas de seleção, comparação e registro apresentam informações relacionadas à finalidade de cada tela. |
| H9 | A pesquisa sem resultados oferece as opções `Corrigir ID`, `Usar filtros` e `Voltar ao histórico`. |
| H10 | As mensagens de comparabilidade orientam a necessidade de verificar as condições antes de concluir a análise. |

---

# Avaliador A03 — Rafaela Altheman de Campos

**Foco da análise:** clareza da comunicação, feedback das ações, recuperação de erros e continuidade da navegação durante apresentações.

**Situação:** registro preparado para validação pela avaliadora.

## 4. Matriz de cobertura das 10 heurísticas

| Heurística | Elementos analisados | Resultado |
|---|---|---|
| H1 — Visibilidade do estado do sistema | P06, telas 07, 09 e 21 | A interface apresenta mensagens explícitas de confirmação após registros, permitindo reconhecer o estado da operação. |
| H2 — Correspondência entre o sistema e o mundo real | P01, P03 e P10 | V01: unidade de velocidade inconsistente. V03: erro textual que compromete o acabamento da comunicação. |
| H3 — Controle e liberdade do usuário | Telas 15, 43 e 45 | A interface oferece retorno à apresentação e opções para corrigir ou cancelar registros. |
| H4 — Consistência e padronização | P03 e telas 04 e 05 | V02: mensagens sobre as condições dos treinamentos apresentam interpretações potencialmente conflitantes. V01 também gera inconsistência. |
| H5 — Prevenção de erros | Telas 05, 06 e 45 | V02: comunicação ambígua pode induzir conclusão inadequada; a tela 45 apresenta recurso positivo para recuperação. |
| H6 — Reconhecimento em vez de memorização | Telas 15, 43 e 21 | O contexto da execução, período e indicador está identificado durante a consulta de evidências e registros. |
| H7 — Flexibilidade e eficiência de uso | Telas 15–18 e 43 | A apresentação possui controle para consultar evidências e avançar entre indicadores. |
| H8 — Estética e design minimalista | P01, P07 e P10 | Os indicadores e as mensagens são organizados em áreas específicas, sem violação concreta de minimalismo confirmada. |
| H9 — Reconhecimento, diagnóstico e recuperação de erros | P09 e telas 29, 33 e 45 | As mensagens identificam situações de erro e apresentam ações para corrigi-las. |
| H10 — Ajuda e documentação | Telas 05, 37 e 43 | A interface apresenta orientações contextuais sobre comparabilidade, informações ausentes e evidências. |

## 5. Declaração de violações

### V03 — Erro de digitação na mensagem do estado vazio

**Heurística relacionada:** H2 — Correspondência entre sistema e mundo real.

**Localização:** P10 — Painel sem dados do período.

**Descrição:**

Ao selecionar um intervalo sem resultados, o usuário recebe uma mensagem informando a ausência de registros.

Entretanto, o texto apresentado contém um erro de escrita:

`Não há resultados dsponíveis no período escolhido`.

Em interfaces analíticas, as mensagens de estado são importantes porque explicam o que aconteceu e orientam a próxima ação.

Embora o erro não impeça a recuperação, uma comunicação textual revisada contribui para a percepção de qualidade e confiabilidade da interface.

**Consequência para o usuário:**

O usuário ainda consegue compreender a mensagem, mas encontra uma inconsistência textual em uma situação que exige orientação clara.

**Severidade:** 1 — Cosmético.

**Justificativa:**

A falha possui baixo impacto funcional, mas afeta a qualidade da comunicação.

**Recomendação:**

Corrigir o texto para:

`Não há resultados disponíveis no período escolhido`.

Também é recomendada uma revisão ortográfica das mensagens de erro, confirmação e estados vazios.

### V02 — Ambiguidade na indicação das condições de treinamento

**Heurísticas relacionadas:** H4 e H5.

**Localização:** P03, telas 04 e 05.

**Descrição:**

A interface utiliza mensagens diferentes para comunicar a situação das condições de treinamento.

A expressão `Diferença de configuração: Nenhuma` pode transmitir segurança sobre a equivalência das execuções, enquanto as demais telas informam que as condições não foram confirmadas.

Esse problema afeta a comunicação porque o usuário recebe informações que não são suficientemente compatíveis entre si.

**Consequência para o usuário:**

A mensagem pode ser interpretada como uma confirmação definitiva, levando à formulação de conclusões sem considerar a ausência de informações.

**Severidade:** 3 — Grave.

**Recomendação:**

Utilizar mensagens objetivas e consistentes que diferenciem condições verificadas e condições desconhecidas.

A orientação deve permanecer visível até a etapa de registro da hipótese.

### V01 — Inconsistência na unidade de velocidade

**Heurísticas relacionadas:** H2 e H4.

**Localização:** P01, P03 e tela 04.

**Descrição:**

A interface apresenta `0,32 m/s` no painel geral e `0.32 cm/s` nas telas de comparação.

A divergência compromete a comunicação porque o usuário recebe representações diferentes para a mesma informação.

Em uma apresentação de resultados, essa inconsistência pode gerar dúvidas sobre o significado dos indicadores utilizados.

**Consequência para o usuário:**

O usuário pode perder a confiança na informação ou interpretar incorretamente a evolução do desempenho.

**Severidade:** 4 — Catastrófico.

**Recomendação:**

Padronizar as unidades e os formatos numéricos em todas as visualizações do indicador.

## 6. Boas práticas — heurísticas sem violações identificadas

| Heurística | Boa prática observada |
|---|---|
| H1 | A mensagem `Hipótese salva e vinculada a EXEC-104 e EXEC-103` identifica o resultado da ação. |
| H3 | A tela de evidência oferece `Voltar à apresentação (mesmo ponto)`, permitindo retomar a atividade. |
| H6 | A evidência identifica o treinamento, a referência, o período e o indicador consultado. |
| H7 | Durante a reunião, o usuário pode consultar evidências e avançar entre indicadores. |
| H8 | A visualização da evidência apresenta um agrupamento específico das informações de contexto. |
| H9 | A tela 45 informa que nenhuma anotação foi confirmada e oferece as ações `Corrigir anotação`, `Tentar novamente` e `Cancelar`. |
| H10 | A tela 37 explica que informações não registradas não podem ser inferidas e sugere fontes para investigação. |

---

# 7. Consolidação da equipe

A organização das análises permite observar os mesmos problemas sob três perspectivas complementares:

- **Manuella:** confiabilidade dos indicadores e coerência dos dados apresentados.
- **Letizia:** consequências das inconsistências para a conclusão das tarefas e o registro de hipóteses.
- **Rafaela:** clareza das mensagens e continuidade da comunicação entre as telas.

As ocorrências V01, V02 e V03 foram verificadas no protótipo. As redações atribuídas às integrantes devem ser confirmadas por elas antes de serem apresentadas como registros de inspeções independentes.

Não foram acrescentadas violações artificiais para diferenciar as avaliações.

## 7.1. Quadro consolidado de problemas

| ID | Problema | Heurísticas | Localização | Severidade |
|---|---|---|---|---|
| V01 | Inconsistência na unidade de velocidade da execução EXEC-104 | H2 e H4 | P01, P03 e tela 04 | 4 |
| V02 | Ambiguidade na indicação das condições de treinamento | H4 e H5 | P03, telas 04 e 05 | 3 |
| V03 | Erro de digitação na mensagem do estado vazio | H2 | P10 | 1 |

## 7.2. Priorização das melhorias

A priorização considera o impacto dos problemas sobre a interpretação das informações e a utilização da interface.

| Prioridade | Problema | Justificativa |
|---|---|---|
| 1 | V01 | A divergência de unidade pode comprometer a interpretação de uma métrica importante e a comparação entre execuções. |
| 2 | V02 | A ambiguidade pode levar o usuário a interpretar condições não verificadas como equivalentes. |
| 3 | V03 | O erro textual prejudica a comunicação, mas não impede a compreensão geral da mensagem. |

## 7.3. Relação entre problemas e heurísticas

| Heurística | Problemas relacionados |
|---|---|
| H1 | Nenhuma violação específica identificada. |
| H2 | V01 e V03. |
| H3 | Nenhuma violação específica identificada. |
| H4 | V01 e V02. |
| H5 | V02. |
| H6 | Nenhuma violação específica identificada. |
| H7 | Nenhuma violação específica identificada. |
| H8 | Nenhuma violação específica identificada. |
| H9 | Nenhuma violação específica identificada. |
| H10 | Nenhuma violação específica identificada. |

## 7.4. Evidências visuais

As figuras abaixo são comparativos visuais dos textos verificados nos frames do Figma.

A pasta `evidencias` deve ser mantida no mesmo diretório deste documento para que as figuras sejam exibidas corretamente no GitHub.

### EV01 — Inconsistência na unidade de velocidade

![EV01 — Unidade de velocidade](evidencias/EV01_unidade_velocidade.png)

**Problema relacionado:** V01.

**Evidência:**

- P01 apresenta `0,32 m/s`.
- P03 apresenta `0.32 cm/s`.
- Tela 04 apresenta `0.32 cm/s`.

**Consequência:** interpretação incorreta da grandeza física e da evolução do treinamento.

**Frames originais:**

- [P01 — Painel geral](https://www.figma.com/design/qHpoJxQF4Sthdy99w7Scul/IHC?node-id=3-2)
- [P03 — Comparação](https://www.figma.com/design/qHpoJxQF4Sthdy99w7Scul/IHC?node-id=2-2)
- [Tela 04 — Comparar métricas](https://www.figma.com/design/qHpoJxQF4Sthdy99w7Scul/IHC?node-id=32-1374)

### EV02 — Ambiguidade das condições de treinamento

![EV02 — Condições de treinamento](evidencias/EV02_condicoes_comparabilidade.png)

**Problema relacionado:** V02.

**Evidência:**

- P03: `Diferença de configuração: Nenhuma`.
- Tela 04: `Condições de treinamento: não confirmadas`.
- Tela 05: `Condições não confirmadas`.

**Consequência:** possibilidade de interpretar condições desconhecidas como comprovadamente equivalentes.

**Frames originais:**

- [P03 — Comparação](https://www.figma.com/design/qHpoJxQF4Sthdy99w7Scul/IHC?node-id=2-2)
- [Tela 04 — Comparação de métricas](https://www.figma.com/design/qHpoJxQF4Sthdy99w7Scul/IHC?node-id=32-1374)
- [Tela 05 — Verificar comparabilidade](https://www.figma.com/design/qHpoJxQF4Sthdy99w7Scul/IHC?node-id=32-1416)

### EV03 — Erro de digitação no estado vazio

![EV03 — Mensagem de estado vazio](evidencias/EV03_erro_estado_vazio.png)

**Problema relacionado:** V03.

**Texto identificado:**

`Não há resultados dsponíveis no período escolhido`.

**Correção recomendada:**

`Não há resultados disponíveis no período escolhido`.

**Frame original:**

[P10 — Painel sem dados do período](https://www.figma.com/design/qHpoJxQF4Sthdy99w7Scul/IHC?node-id=30-2)

### EV04 — Exemplos de boas práticas

![EV04 — Exemplos de boas práticas](evidencias/EV04_boas_praticas.png)

Foram identificados exemplos positivos na interface:

- **H1:** confirmação explícita de hipótese registrada.
- **H3:** possibilidade de retornar à apresentação no mesmo ponto.
- **H6:** apresentação de informações sobre execução e período.
- **H9:** mensagens que informam falhas e oferecem recuperação.
- **H10:** orientação contextual sobre dados não registrados.

**Frames originais:**

- [Tela 07 — Hipótese registrada](https://www.figma.com/design/qHpoJxQF4Sthdy99w7Scul/IHC?node-id=32-1624)
- [Tela 43 — Evidência da execução](https://www.figma.com/design/qHpoJxQF4Sthdy99w7Scul/IHC?node-id=32-2265)
- [Tela 45 — Recuperação de erro](https://www.figma.com/design/qHpoJxQF4Sthdy99w7Scul/IHC?node-id=32-2458)
- [Tela 37 — Dado não registrado](https://www.figma.com/design/qHpoJxQF4Sthdy99w7Scul/IHC?node-id=32-1268)

## 7.5. Síntese das perspectivas individuais

| Avaliadora | Foco principal | Aspecto considerado mais relevante | Contribuição para a análise consolidada |
|---|---|---|---|
| A01 — Manuella | Consistência e interpretação das métricas | V01 — Divergência de unidade na velocidade. | Destacar a confiabilidade dos indicadores e a necessidade de validar grandezas físicas. |
| A02 — Letizia | Navegação e prevenção de decisões equivocadas | V02 — Ambiguidade na comparabilidade das execuções. | Destacar o risco de avançar no fluxo com premissas não verificadas. |
| A03 — Rafaela | Comunicação e recuperação da interação | V03 — Erro textual; análise complementar de V01 e V02. | Destacar clareza dos rótulos, feedback e continuidade da apresentação. |

**Nota de validação:** esta síntese organiza perspectivas diferentes para revisão da equipe; não comprova, por si só, três inspeções independentes. Cada integrante deverá confirmar os registros atribuídos antes da entrega definitiva.

---

## 8. Síntese e plano de melhoria

A avaliação identificou três problemas relacionados à qualidade da interação com o protótipo.

O primeiro está relacionado à apresentação inconsistente da unidade de velocidade, que compromete a interpretação correta dos indicadores.

O segundo envolve a comunicação sobre as condições dos treinamentos, que pode levar o usuário a considerar execuções equivalentes sem confirmação suficiente.

O terceiro corresponde a um erro de digitação em uma mensagem de estado vazio.

Esses problemas possuem impactos diferentes e devem ser corrigidos segundo sua severidade e relação com as tarefas dos usuários.

### 8.1. Plano de melhoria

| ID | Ação recomendada | Resultado esperado |
|---|---|---|
| V01 | Padronizar a unidade de velocidade e conferir os valores apresentados em todas as telas. | Garantir consistência na apresentação e permitir comparação adequada entre execuções. |
| V02 | Diferenciar mensagens sobre condições confirmadas, diferenças identificadas e condições não verificadas. | Evitar interpretações equivocadas sobre a equivalência entre treinamentos. |
| V03 | Corrigir a palavra `dsponíveis` para `disponíveis`. | Melhorar a clareza e a qualidade textual da interface. |

### 8.2. Critérios para validação das melhorias

A validação das melhorias deve considerar os seguintes critérios:

- A velocidade da execução EXEC-104 deve utilizar a mesma unidade em todas as telas.
- Os valores de velocidade devem ser consistentes entre o painel geral e a comparação.
- A interface deve diferenciar condições confirmadas de condições não confirmadas.
- A mensagem de ausência de resultados deve apresentar a palavra `disponíveis` corretamente.
- As alterações não devem prejudicar a organização visual ou a compreensão das demais informações.

### 8.3. Registro de rechecagem

A rechecagem da versão disponível do Figma confirmou a permanência dos três problemas identificados.

Nenhuma alteração no protótipo foi confirmada durante essa verificação.

| ID | Item verificado | Evidência | Resultado |
|---|---|---|---|
| V01 | Unidade de velocidade em P01, P03 e tela 04. | EV01 | Problema ainda identificado. |
| V02 | Mensagens sobre condições de treinamento. | EV02 | Ambiguidade ainda identificada. |
| V03 | Mensagem do estado vazio em P10. | EV03 | Erro de digitação ainda identificado. |

Essa rechecagem documenta o estado da versão examinada. Ela não deve ser confundida com a reinspeção de uma versão corrigida.

### 8.4. Reinspeção após implementação das correções

Após implementar as alterações no Figma, será necessário verificar se os problemas foram resolvidos sem introduzir novas dificuldades.

| ID | Item a verificar | Critério de aprovação | Situação |
|---|---|---|---|
| V01 | Unidade de velocidade em P01, P03 e tela 04. | Valores e unidades consistentes em todas as telas. | Pendente de correção e reinspeção. |
| V02 | Mensagens de configuração e comparabilidade. | Diferenciação clara entre condições confirmadas e não confirmadas. | Pendente de correção e reinspeção. |
| V03 | Mensagem do estado vazio. | Palavra `disponíveis` escrita corretamente. | Pendente de correção e reinspeção. |

### 8.5. Procedimento de reinspeção

Para cada problema corrigido, a equipe deverá:

1. Registrar a versão e a data da alteração.
2. Identificar as telas modificadas.
3. Conferir se o problema original deixou de ocorrer.
4. Verificar possíveis inconsistências introduzidas pela alteração.
5. Registrar a evidência visual da versão corrigida.
6. Classificar o problema como resolvido, parcialmente resolvido ou persistente.

O resultado deve ser registrado com base na versão efetivamente corrigida, sem presumir sua aprovação.

---

## 10. Checklist da entrega

- [x] Definir as dez heurísticas utilizadas na avaliação.
- [x] Delimitar o escopo da inspeção.
- [x] Identificar os elementos e estados relevantes da interface.
- [x] Definir a escala de severidade.
- [x] Registrar os problemas identificados.
- [x] Relacionar os problemas às heurísticas correspondentes.
- [x] Organizar as análises individuais com perspectivas diferenciadas.
- [x] Consolidar os problemas encontrados no protótipo.
- [x] Definir recomendações de melhoria.
- [x] Organizar os critérios de validação das melhorias.
- [x] Inserir evidências visuais comparativas dos problemas identificados.
- [ ] Confirmar os registros individuais de inspeção com cada integrante.
- [ ] Implementar as correções no Figma.
- [ ] Registrar a reinspeção da versão corrigida.

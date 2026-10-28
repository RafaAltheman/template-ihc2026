# Entrega 5 — Análise de tarefas: HTA, GOMS e CTT

**Data:** 21/10/2026  
**Status:** 🟩 concluída 
**Responsabilidade:** cada integrante modela pelo menos 1 HTA, 1 GOMS e 1 CTT. As três técnicas podem abordar a mesma funcionalidade ou funcionalidades distintas, conforme a orientação da disciplina.

## Objetivo da atividade

Modelar tarefas importantes sob perspectivas complementares: decomposição hierárquica (HTA), estrutura de metas/métodos/operações (GOMS) e relações temporais entre tarefas (CTT). O diagrama deve ser acompanhado de interpretação textual.

## Para projetos cujo TCC não previa interface

Modele **tarefas humanas relacionadas ao uso da contribuição técnica**, e não a implementação interna do algoritmo. Exemplos de boas tarefas para análise:

- investigar uma consulta de baixo desempenho;
- configurar uma análise e selecionar parâmetros;
- submeter um dataset e verificar sua validade;
- acompanhar uma execução demorada;
- comparar dois resultados/modelos;
- interpretar uma recomendação e decidir se a aceita;
- localizar uma execução anterior usando busca/filtros;
- gerar e compartilhar um relatório;
- administrar papéis/permissões quando isso for parte do trabalho real;
- revisar um alerta e registrar uma decisão.

Um CRUD pode gerar tarefas relevantes, mas “cadastrar usuário” só merece modelagem se tiver significado no domínio (papéis, validações, riscos, permissões, dependências).

## Seleção das tarefas

| ID | Tarefa | Persona/cenário | Frequência/criticidade | Responsável |
|---|---|---|---|---|
| T01 | Avaliar se o resultado de um treinamento representa uma melhoria real no desempenho do robô | P01 Rafael Martins / C01 | Frequente e alta: decisão equivocada pode provocar ajustes ineficazes e gasto computacional | Letizia Lowatzki Baptistella 22.125.063-2 |
| T02 | Localizar e comparar execuções anteriores para explicar diferenças de desempenho | P02 Marina Oliveira / C02 | Recorrente e alta: exige rastreabilidade e comparabilidade entre experimentos | Manuella Filipe Peres — 22.224.029-3 |
| T03 | Consultar uma síntese do desempenho e comunicar à equipe os pontos que precisam de investigação | P03 Carlos Almeida / C03 | Periódica e alta: orienta reuniões e priorização de investigação | Rafaela Altheman de Campos — 22.125.062-4 |

> Priorize tarefas necessárias para que o usuário alcance objetivos centrais. Não desperdice a modelagem em ações triviais isoladas, como “clicar em login”, se o objetivo relevante é maior. Da mesma forma, não modele o funcionamento interno do algoritmo como se fosse uma tarefa humana.

---

## HTA — T01: Avaliar se um treinamento melhorou o desempenho


**Autor(a):** Letizia Lowatzki Baptistella 22.125.063-2

### Descrição da tarefa

O objetivo é decidir se os resultados de um treinamento indicam uma melhoria útil para o desempenho do robô em partidas de futebol. A tarefa começa quando Rafael (P01), no cenário C01, tem acesso aos resultados de uma execução e termina quando registra uma conclusão fundamentada: considerar o resultado uma melhoria, rejeitá-lo como melhoria ou indicar que são necessárias mais evidências. A avaliação considera velocidade média, distância percorrida, taxa de quedas, estabilidade, gol, força de chute e localização, além da observação do comportamento do robô, quando houver esse tipo de registro.

### Diagrama

![HTA T01](../assets/05_tarefas/hta_t01.svg)

**Leitura do diagrama:** o objetivo 0 é decomposto em preparar a comparação (1), examinar evidências (2), classificar (3) e registrar (4). A subdivisão do item 3 representa uma escolha, não três ações consecutivas. A linha inferior dos nós 1.1, 1.2, 2.1, 2.2, 3.1–3.3 e 4 representa o nível operacional.

### Decomposição e planos

| ID | Objetivo ou operação | Plano/ordem | Problema de interação e decisão de design | Input | Feedback |
|---|---|---|---|---|---|
| 0 | Avaliar se um treinamento melhorou o desempenho | `1 > 2 > 3 > 4` | Informações da execução e da referência devem acompanhar toda a decisão para evitar conclusões sem contexto. | Resultados da execução avaliada (ID, status, data, ambiente, parâmetros e métricas) e registro visual do comportamento. | Confirmação de que a decisão (melhoria, não melhoria ou evidências insuficientes) e a justificativa foram salvas, associadas ao ID da execução e ao baseline. |
| 1 | Identificar execução e referência | `1.1 > 1.2` | Mostrar identificadores, datas, versões, ambiente e parâmetros antes da comparação. |
| 1.1 | Abrir treinamento avaliado | operação | Diferenciar execução concluída, em andamento, com erro e sem dados disponíveis. |
| 1.2 | Selecionar baseline comparável | operação; se não existir, registrar a limitação e seguir para a saída de evidências insuficientes | Informar claramente compatibilidade ou divergência de condições; não escolher referência automaticamente sem identificação. |
| 2 | Examinar evidências | `2.1 + 2.2` | Reunir indicadores complementares sem ocultar pioras em outras métricas. |
| 2.1 | Comparar métricas de desempenho | operação | Apresentar velocidade média, distância percorrida, taxa de quedas, gols marcados e força de chute com unidades. |
| 2.2 | Observar comportamento em campo, localização e estabilidade | operação | Associar o registro visual à execução correta e indicar sua indisponibilidade quando pertinente. |
| 3 | Classificar resultado | `3.1 / 3.2 / 3.3`, escolhendo uma única alternativa conforme as evidências | Evitar classificação automática baseada somente em velocidade ou em uma média isolada. |
| 3.1 | Classificar como melhoria | operação alternativa | Solicitar justificativa apoiada em indicadores e comportamento observado. |
| 3.2 | Classificar como não melhoria | operação alternativa | Permitir registrar regressão ou compromisso entre ganho de velocidade e aumento de quedas. |
| 3.3 | Marcar evidências insuficientes | operação alternativa | Permitir explicar falta de baseline, incompatibilidade, ausência de medida ou incerteza. |
| 4 | Registrar decisão e justificativa | operação | Associar conclusão ao ID e à referência e confirmar que o registro foi salvo. |

**Planos detalhados:** **Plano 0:** concluir 1, depois 2, depois escolher uma saída em 3 e registrar em 4. **Plano 1:** identificar primeiro o treinamento analisado e depois verificar a referência; se não existir referência válida, conservar o estado de insuficiência de evidência. **Plano 2:** analisar métricas quantitativas e visuais do treinamento **Plano 3:** selecionar exatamente um desfecho; se uma incompatibilidade for descoberta antes do registro, retornar à seleção de referência ou à análise das evidências. **Plano 4:** salvar com justificativa e conferir confirmação.

**Verificação do HTA:**

- **O objetivo 0 representa uma meta do usuário?** Sim. O resultado é uma decisão sobre o valor do treinamento, não a execução interna de um algoritmo.
- **As subtarefas são necessárias e suficientes?** Sim para a decisão contextualizada, desde que a ausência de informação seja tratada como limitação explícita e a verificação comportamental seja condicional à disponibilidade.
- **Os planos indicam ordem, alternativa, repetição ou condição?** Sim: `>` estabelece a ordem principal, `/` separa os três desfechos, `+` representa evidências complementares e o retorno ocorre quando um dado invalida a comparação.
- **A decomposição parou em nível útil para projeto de interação?** Sim: as operações correspondem a identificar dados, consultar indicadores e registrar uma decisão; detalhes do algoritmo não são decompostos.

**Interpretação:** o maior risco identificado é confundir ganho pontual de um indicador com melhora global. Por exemplo, aumento de velocidade acompanhado de mais quedas exige uma decisão fundamentada. O protótipo deve apresentar simultaneamente as principais métricas, identificar lacunas e permitir a saída “evidências insuficientes” em condições equivalentes às demais opções.

---

## GOMS — T01: Avaliar se um treinamento melhorou o desempenho

**Autor(a):** Letizia Lowatzki Baptistella 22.125.063-2

### Goal

`G0: Decidir se o resultado de um treinamento representa uma melhoria útil no desempenho do robô e registrar uma conclusão fundamentada (melhoria, não melhoria ou evidências insuficientes).`

**Subobjetivos:** `G1` identificar execução e referência; `G2` examinar evidências; `G3` classificar resultado; `G4` registrar decisão e justificativa.

### Métodos, operadores e regras de seleção

### G1: Identificar execução e referência
#### Method M1:
- O1 (interação): abrir a lista de treinamentos e selecionar a execução a ser avaliada.
- O2 (percepção): conferir status (concluída, em andamento, com erro, sem dados), ID, data, versão, e parâmetros.
- O3 (interação): abrir a lista de referências e selecionar o treino a ser comparado (baseline).
- O4 (percepção/cognição): conferir se a versão e parâmetros do baseline são compatíveis com os da execução.
- O5 (percepção): confirmar que a execução e o baseline corretos estão identificados no contexto da análise.

### G2: Examinar evidências
#### Method M1
- O1 (percepção): ler as métricas (velocidade média, distância, quedas, gols, força de chute), com unidades, lado a lado com o baseline quando houver.
- O2 (cognição): verificar se alguma métrica piorou, mesmo que outra tenha melhorado.
- O3 (interação/percepção): abrir o registro de comportamento, localização e estabilidade para comparar com baseline.
- O4 (percepção/cognição): confirmar que métricas e registro visual correspondem à execução e ao baseline identificados em G1.

### G3: Classificar resultado
#### Method M1
- O1 (cognição): ponderar as evidências conforme os critérios de decisão.
- O2 (interação): selecionar a classificação: melhoria, não melhoria ou evidências insuficientes.
- O3 (percepção): confirmar que a classificação selecionada está destacada e é coerente com as evidências examinadas.

Critérios de decisão (O1 de G3): classificar como "melhoria" quando as métricas principais melhoram, sem piora relevante em quedas e estabilidade, e o comportamento é coerente; como "não melhoria" quando há regressão (por exemplo, mais velocidade com mais quedas); ou como "evidências insuficientes* quando falta baseline, medida ou registro necessário

### G4: Registrar decisão e justificativa
#### Method M1
- O1 (interação): digitar a justificativa, citando indicadores e comportamento observado.
- O2 (interação): salvar o registro.
- O3 (percepção): confirmar que o registro foi salvo e associado ao ID da execução e ao baseline.

### **Interpretação do GOMS:**
Rafael deve escolher uma execução de referencia e uma execução de comparação. As três classificações de G3 não são métodos, e sim desfechos de uma decisão apoiada em critérios, por isso aparecem como critérios de decisão e não como métodos alternativos. A análise mostra a necessidade de manter o contexto da execução e do baseline visível, apresentar as métricas lado a lado sem ocultar pioras, oferecer "evidências insuficientes" com o mesmo peso das demais saídas e confirmar o salvamento do registro.

---

## CTT — T01: Avaliar se um treinamento melhorou o desempenho

**Autor(a):** Letizia Lowatzki Baptistella 22.125.063-2

### Descrição

O CTT descreve o encadeamento entre reconhecer a necessidade de avaliar um treinamento, identificar execução e referência, examinar evidências, classificar o resultado e registrar a decisão. Na T01, Rafael (P01, cenário C01) decide se o resultado de uma execução representa uma melhoria útil.
As relações temporais mais importantes são três. As evidências (métricas e comportamento observado) podem ser examinadas em qualquer ordem. A classificação é uma escolha exclusiva entre melhoria, não melhoria e evidências insuficientes. A seleção do baseline pode se repetir quando a referência escolhida se mostra incompatível.


### Diagrama

![CTT T01](../assets/05_tarefas/ctt_t01.svg)

A tarefa abstrata A0 (avaliar se um treinamento melhorou o desempenho) se decompõe em quatro subtarefas abstratas, ligadas por habilitação (>>): identificar execução e referência (A1), examinar evidências (A2), classificar resultado (A3) e registrar decisão e justificativa (A4). Em A1, Rafael reconhece a necessidade de avaliar o treinamento (U11, fora do sistema) e abre o treinamento avaliado (I12), passando a informação (`[]>>`) para a seleção do baseline comparável (I13). Em A2, a comparação das métricas (I21) e a observação do comportamento (I22) ocorrem em qualquer ordem (|||) e habilitam a verificação de pioras e inconsistências entre as evidências (U23, tarefa do usuário). Em A3, Rafael escolhe uma única classificação ([]): melhoria (I31), não melhoria (I32) ou evidências insuficientes (I33). Em A4, a decisão e a justificativa informadas (I41) são passadas ao sistema (`[]>>`), que salva o registro e confirma o salvamento (S42).

**Expressão temporal do modelo:**

```text
A0 = A1 >> A2 >> A3 >> A4
A1 = U11 >> I12 []>> I13*
A2 = (I21 ||| I22) >> U23
A3 = I31 [] I32 [] I33
A4 = I41 []>> S42
```

### Legenda e relações temporais usadas

| Operador/relação | Significado no diagrama | Exemplo no modelo |
|---|---|---|
| `>>` | **Habilitação:** indica que uma atividade depende da conclusão de uma etapa anterior para ser iniciada. | `A1 >> A2 >> A3 >> A4`: a execução e a referência são identificadas antes de examinar as evidências, classificar e registrar. `U11 >> I12`: Rafael reconhece a necessidade de avaliar antes de abrir o treinamento. |
| `[]>>` | **Habilitação com passagem de informação:** além de habilitar a atividade seguinte, a etapa anterior fornece informações necessárias para sua execução. | `I12 []>> I13`: a execução aberta determina os baselines candidatos. `I41 []>> S42`: a decisão e a justificativa informadas são o que o sistema salva. |
| `[]` | **Escolha:** duas ou mais tarefas estão habilitadas, mas, iniciada uma, as outras são desabilitadas. | `I31 [] I32 [] I33`: Rafael escolhe uma única classificação. |
| `\|\|\|` | **Concorrência:** as atividades podem ocorrer em qualquer ordem ou ao mesmo tempo. | `I21 \|\|\| I22`: métricas e comportamento observado são examinados na ordem que Rafael preferir. |

**Interpretação e implicações de design:** a saída "evidências insuficientes" precisa ser uma opção da escolha, e não uma falha a esconder. A comparação das métricas e a observação do comportamento devem estar acessíveis ao mesmo tempo, para que Rafael cruze as duas evidências antes de classificar. O contexto da execução e do baseline deve acompanhar toda a análise, e a troca de baseline não pode obrigar Rafael a refazer a seleção da execução.

---



## GOMS — T02: Localizar e comparar execuções anteriores


**Autor(a):** Manuella Filipe Peres — 22.224.029-3

### Goal

`G0: Localizar duas execuções anteriores, comparar seus resultados e registrar uma hipótese rastreável para as diferenças encontradas.`

**Subobjetivos:** `G1` localizar as duas execuções; `G2` comparar métricas e parâmetros; `G3` formular a hipótese; `G4` Registrar hipótese, evidências e ressalvas.

### Métodos, operadores e regras de seleção

### G1: Localizar as duas execuções
#### Method M1: localizar por identificadores conhecidos
- O1 (cognição): recuperar o ID da primeira execução.
- O2 (interação): apontar e clicar no campo de busca.
- O3 (interação): digitar o ID.
- O4 (interação): acionar a busca.
- O5 (percepção): conferir se o registro apresentado (ID, data, versão) é o esperado.
- O6 (interação): adicionar a execução à comparação.
- O7 (cognição/interação): repetir O1–O6 para a segunda execução.
- O8 (percepção): confirmar que as duas execuções corretas foram adicionadas à comparação (IDs e versões).
#### Method M2: localizar por filtros do histórico
- O1 (interação): acessar o histórico de execuções.
- O2 (cognição): definir as pistas disponíveis (período, versão, configuração).
- O3 (interação): selecionar os filtros e acionar a consulta.
- O4 (percepção): ler a lista e conferir os metadados dos resultados.
- O5 (interação): selecionar a primeira e a segunda execução e adicioná-las à comparação.
- O6 (percepção): confirmar que as duas execuções selecionadas estão na comparação, com os IDs esperados.

#### Regras de seleção de G1
• SR1: usar M1 quando Marina conhecer os IDs das duas execuções. Usar M2 quando um ou ambos forem desconhecidos, mas houver atributos suficientes para filtrar.
• SR2: se a busca por ID falhar (O5 do M1 não confere), revisar o ID. Se continuar sem resultado, mudar para M2. Se os filtros do M2 trouxerem resultados demais, refiná-los antes de selecionar (voltar a O3).

### G2: Comparar métricas e parâmetros
#### Method M1
- O1 (interação): abrir a comparação entre as duas execuções.
- O2 (percepção): ler lado a lado os valores das métricas, com unidades.
- O3 (percepção/cognição): identificar quais parâmetros, versões e métricas divergem.
- O4 (cognição): separar o que foi medido (diferença observada) do que seria apenas uma explicação possível.
- O5 (percepção/cognição): confirmar que as divergências identificadas correspondem às duas execuções selecionadas.

### G3: Formular a hipótese
#### Method M1
- O1 (cognição): relacionar as divergências de parâmetros ou versão às diferenças de desempenho e formular uma hipótese.
- O2 (cognição): decidir que ressalvas se aplicam. Uma diferença de versão, sozinha, não prova a causa da diferença de desempenho.
- O3 (cognição): verificar que a hipótese é consistente com as divergências levantadas antes de registrar.

### G4: Registrar hipótese, evidências e ressalvas
#### Method M1
- O1 (interação): digitar a hipótese, as evidências, os IDs das duas execuções e as ressalvas.
- O2 (interação): salvar o registro.
- O3 (percepção): confirmar que o registro foi salvo e ficou associado aos IDs.


### **Interpretação do GOMS:** 
O critério que separa M1 de M2 é informação de que Marina dispõe no início da tarefa, e não uma preferência arbitrária por tela. Ambos alcançam a mesma meta e terminam com um registro contextualizado. A análise revela a necessidade de preservar seleções e filtros entre pesquisa e comparação, além de diferenciar o que foi medido da explicação que Marina propõe. Não se supõe que uma diferença de versão, sozinha, prove a causa da diferença de desempenho.

---

## HTA — T03: Consultar síntese e comunicar pontos de investigação

**Autor(a):** Rafaela Altheman de Campos — 22.125.062-4

### Descrição da tarefa

O objetivo é consultar uma síntese do desempenho do robô, interpretar a evolução dos indicadores e comunicar à equipe os principais pontos que precisam de investigação. A tarefa começa quando Carlos (P03), no cenário C03, precisa preparar ou conduzir uma reunião sobre os resultados dos treinamentos e termina quando a equipe discute os resultados e define os encaminhamentos necessários.

A análise considera a evolução de métricas como velocidade média, distância percorrida, taxa de quedas, estabilidade, gols marcados e força de chute, além das alterações de parâmetros ao longo dos treinamentos. O painel apresenta essas informações de forma consolidada, permitindo que Carlos identifique mudanças relevantes, consulte evidências detalhadas quando necessário e comunique suas observações à equipe. A interpretação, priorização e definição dos encaminhamentos permanecem sob responsabilidade humana.

### Diagrama

![HTA T03](../assets/05_tarefas/hta03.svg)

**Leitura do diagrama:** o objetivo 0 é decomposto em preparar o painel (1), interpretar o desempenho (2), comunicar a interpretação (3) e discutir os resultados e definir encaminhamentos (4). A subdivisão do item 3 representa uma apresentação que pode ser temporariamente interrompida para consultar evidências detalhadas, sem necessidade de reiniciar a análise. A linha inferior dos nós 1.1, 1.2, 2.1, 2.2, 3.1, 3.2, 4.1 e 4.2 representa o nível operacional.

### Decomposição e planos

| ID | Objetivo ou operação | Plano/ordem | Problema de interação e decisão de design | Input | Feedback |
|---|---|---|---|---|---|
| 0 | Consultar síntese e comunicar pontos de investigação | `1 > 2 > 3 > 4` | Manter o período e o contexto da análise visíveis ao longo da consulta e da apresentação. | Histórico de treinamentos, métricas, parâmetros e período selecionado. | Síntese exibida com período e indicadores identificados. |
| 1 | Preparar o painel | `1.1 > 1.2` | Permitir selecionar o escopo da análise e identificar claramente quais dados estão sendo apresentados. | Objetivo da reunião e histórico disponível. | Painel preparado para o período selecionado. |
| 1.1 | Identificar necessidade e escopo da análise | operação | Evitar a consulta de informações sem relação com o objetivo da reunião. | Necessidade de acompanhamento dos treinamentos. | Escopo de análise definido pelo usuário. |
| 1.2 | Selecionar período e visualizar síntese | operação | Oferecer seleção de período e manter os filtros visíveis, indicando ausência de dados quando pertinente. | Período escolhido e resultados dos treinamentos. | Indicadores e parâmetros apresentados no painel. |
| 2 | Interpretar o desempenho | `2.1 > 2.2` | Facilitar a identificação de tendências, mudanças relevantes e possíveis regressões. | Métricas e parâmetros consolidados. | Gráficos e valores disponíveis para interpretação. |
| 2.1 | Analisar evolução das métricas e parâmetros | operação | Apresentar os indicadores com unidades e referência temporal, sem ocultar pioras. | Velocidade, distância, quedas, estabilidade, gols, força de chute e parâmetros. | Evolução dos indicadores exibida ao longo do período. |
| 2.2 | Definir pontos que exigem investigação | operação | Permitir relacionar variações de desempenho às condições dos treinamentos sem assumir causalidade automaticamente. | Tendências, divergências e resultados observados. | Indicadores e evidências permanecem disponíveis para consulta. |
| 3 | Comunicar a interpretação à equipe | `3.1`, com `3.2` opcional e repetível quando houver necessidade de esclarecimento | Preservar o contexto do painel durante interrupções da apresentação. | Síntese interpretada e pontos identificados. | Retorno ao painel sem perda do período e dos indicadores selecionados. |
| 3.1 | Apresentar síntese e prioridades | operação | Exibir informações de forma compreensível para apoiar a comunicação dos resultados. | Conclusões e pontos considerados relevantes. | Síntese permanece disponível durante a exposição. |
| 3.2 | Abrir evidência detalhada quando necessário | operação condicional e repetível | Permitir consultar registros detalhados e retornar à apresentação sem perder o estado anterior. | Dúvida da equipe ou necessidade de esclarecer um resultado. | Evidência exibida com identificação da execução e retorno ao contexto anterior. |
| 4 | Discutir e definir encaminhamentos | `4.1 > 4.2` | Disponibilizar as evidências para apoiar a discussão, sem substituir decisões humanas. | Pontos apresentados e questionamentos da equipe. | Informações permanecem acessíveis para consulta durante a discussão. |
| 4.1 | Discutir resultados com a equipe | operação | Facilitar a consulta aos dados que fundamentam as observações apresentadas. | Resultados, dúvidas e interpretações dos participantes. | Painel e evidências disponíveis para esclarecimentos. |
| 4.2 | Definir responsáveis e próximos encaminhamentos | operação | Evitar que a interface apresente decisões automáticas sobre prioridades ou responsabilidades. | Conclusões da discussão e necessidades identificadas. | Encaminhamentos definidos pela equipe, fora do sistema. |

**Planos detalhados:**

**Plano 0:** concluir 1, depois 2, comunicar os resultados em 3 e finalizar com a discussão e definição de encaminhamentos em 4.

**Plano 1:** identificar a necessidade de análise e o objetivo da reunião; em seguida, selecionar o período e consultar a síntese preparada pelo sistema. Caso não existam dados para o período escolhido, revisar o intervalo antes de continuar.

**Plano 2:** examinar a evolução das métricas e dos parâmetros e, com base nas informações observadas, definir os principais pontos que precisam de investigação. Se houver dados incompletos ou inconsistentes, considerar essas limitações na interpretação.

**Plano 3:** apresentar os resultados e prioridades à equipe. Caso surja uma dúvida ou necessidade de esclarecimento, abrir a evidência detalhada correspondente e retornar à apresentação. A consulta pode se repetir quantas vezes forem necessárias, sem reiniciar a exposição.

**Plano 4:** discutir os resultados apresentados e definir, com os participantes, os responsáveis e encaminhamentos para as próximas investigações. Essas decisões são realizadas pelos usuários e não automaticamente pelo sistema.

### Verificação do HTA

- **O objetivo 0 representa uma meta do usuário?** Sim. O objetivo é compreender e comunicar os resultados dos treinamentos para orientar a investigação, e não executar procedimentos internos do algoritmo.
- **As subtarefas são necessárias e suficientes?** Sim. A preparação do painel, interpretação dos indicadores, comunicação dos resultados e discussão dos encaminhamentos representam as principais atividades necessárias para atingir o objetivo.
- **Os planos indicam ordem, alternativa, repetição ou condição?** Sim. O símbolo `>` representa a ordem principal, enquanto a consulta às evidências é condicional e repetível durante a apresentação. O retorno à seleção do período ocorre quando os dados disponíveis não atendem à necessidade da análise.
- **A decomposição parou em nível útil para projeto de interação?** Sim. As operações envolvem seleção de períodos, consulta de indicadores, apresentação e abertura de evidências, sem detalhar o processamento interno dos treinamentos.

**Interpretação:** o principal risco identificado é perder o contexto da análise durante a comunicação dos resultados. Por exemplo, ao apresentar uma queda de desempenho, Carlos pode precisar consultar uma execução específica para esclarecer uma dúvida da equipe. Se o sistema não preservar o período, os indicadores e o ponto da apresentação, a continuidade da discussão será prejudicada. O protótipo deve manter o contexto da análise visível, permitir acesso às evidências detalhadas e oferecer retorno ao painel sem perda das seleções realizadas. A identificação de prioridades e a definição de encaminhamentos continuam sendo responsabilidades de Carlos e da equipe.


## GOMS — T03: Consultar síntese e comunicar pontos de investigação

**Autor(a):** Rafaela Altheman de Campos — 22.125.062-4

### Goal

`G0: Consultar uma síntese da evolução do desempenho do robô, identificar pontos relevantes de investigação, comunicar os resultados à equipe e apoiar a definição de encaminhamentos.`

**Subobjetivos:** `G1` preparar o painel e selecionar o período; `G2` interpretar os resultados; `G3` comunicar os pontos de investigação; `G4` discutir resultados e definir encaminhamentos.

### Métodos, operadores e regras de seleção

### G1: Preparar o painel e selecionar o período

#### Method M1: consultar síntese por período

- O1 (cognição): identificar o objetivo da análise e o intervalo de treinamentos relevante para a reunião.
- O2 (interação): acessar o painel de acompanhamento do desempenho.
- O3 (interação): selecionar o período desejado.
- O4 (percepção): verificar se o período aplicado corresponde ao intervalo pretendido.
- O5 (percepção): conferir se os indicadores e parâmetros foram apresentados corretamente.
- O6 (percepção/cognição): verificar a disponibilidade e a abrangência dos dados exibidos.

#### Regras de seleção de G1

- SR1: utilizar M1 quando houver dados disponíveis para o período pretendido.
- SR2: se o período não apresentar dados suficientes, revisar o intervalo selecionado antes de prosseguir.
- SR3: se persistirem lacunas nos dados, considerar essa limitação nas próximas etapas da análise.

### G2: Interpretar os resultados

#### Method M1: examinar a evolução dos indicadores

- O1 (percepção): observar os gráficos de evolução do desempenho apresentados no painel.
- O2 (percepção): conferir os valores de velocidade média, distância percorrida, taxa de quedas, estabilidade, gols marcados e força de chute.
- O3 (percepção/cognição): identificar variações significativas, tendências e possíveis regressões.
- O4 (percepção/cognição): relacionar mudanças de parâmetros ou configurações com as diferenças de desempenho observadas.
- O5 (cognição): distinguir os resultados efetivamente medidos das possíveis explicações para suas variações.
- O6 (cognição): definir quais indicadores ou comportamentos precisam de investigação adicional.

#### Regras de seleção de G2

- SR1: priorizar a análise de indicadores com variações relevantes ou resultados inesperados.
- SR2: quando houver melhoria em um indicador acompanhada de regressão em outro, considerar ambos antes de definir uma prioridade.
- SR3: quando os dados não permitirem estabelecer uma interpretação segura, indicar a necessidade de investigação adicional, sem assumir uma causa como comprovada.

### G3: Comunicar os pontos de investigação

#### Method M1: apresentar a síntese sem consulta adicional

- O1 (cognição): organizar os principais resultados e pontos de investigação identificados em G2.
- O2 (percepção): conferir que o painel apresenta o período e os indicadores correspondentes à análise.
- O3 (tarefa do usuário): explicar à equipe a evolução do desempenho e os pontos considerados relevantes.
- O4 (percepção/cognição): verificar se os resultados apresentados são suficientes para sustentar a discussão.

#### Method M2: apresentar a síntese com consulta a evidências detalhadas

- O1 (tarefa do usuário): apresentar a evolução do desempenho e identificar uma dúvida ou solicitação de esclarecimento.
- O2 (interação): selecionar o indicador ou a execução relacionada à dúvida.
- O3 (interação): abrir a evidência detalhada correspondente.
- O4 (percepção): conferir o ID, o período e os resultados da execução consultada.
- O5 (cognição): interpretar a evidência e relacioná-la à síntese apresentada.
- O6 (tarefa do usuário): esclarecer a dúvida utilizando as informações consultadas.
- O7 (interação): retornar ao painel principal.
- O8 (percepção): confirmar que o período, os indicadores e o contexto anterior foram preservados.
- O9 (tarefa do usuário): retomar a apresentação do ponto em que foi interrompida.

#### Regras de seleção de G3

- SR1: utilizar M1 quando a síntese apresentar informações suficientes para a comunicação dos resultados.
- SR2: utilizar M2 quando surgir uma dúvida, divergência ou solicitação de evidência detalhada durante a reunião.
- SR3: após consultar uma evidência, retornar ao painel e retomar a apresentação sem reiniciar a análise.
- SR4: repetir a consulta a evidências quando diferentes resultados exigirem esclarecimentos adicionais.

### G4: Discutir resultados e definir encaminhamentos

#### Method M1: discutir e estabelecer próximos encaminhamentos

- O1 (tarefa do usuário): discutir com a equipe os resultados apresentados e as possíveis explicações.
- O2 (cognição): considerar a relevância e a criticidade dos pontos identificados.
- O3 (tarefa do usuário): definir, em conjunto com a equipe, quais questões precisam de investigação prioritária.
- O4 (tarefa do usuário): estabelecer responsáveis e próximos encaminhamentos.
- O5 (cognição): verificar se os encaminhamentos estão coerentes com os resultados discutidos e as necessidades de investigação.

### Interpretação do GOMS

Carlos deve inicialmente selecionar o período de análise e consultar a síntese preparada pelo sistema. A partir dos indicadores apresentados, interpreta a evolução do desempenho e identifica os pontos que precisam ser investigados. Durante a reunião, a comunicação pode seguir dois métodos: apresentar diretamente as informações consolidadas ou consultar evidências detalhadas quando houver necessidade de esclarecimento.

As regras de seleção de G3 mostram que a abertura de evidências não deve ser obrigatória, mas precisa estar disponível a qualquer momento durante a apresentação. A análise evidencia a necessidade de preservar o período e os indicadores selecionados, permitindo que Carlos retorne ao painel sem perder o contexto anterior.

O modelo também diferencia as ações realizadas na interface das atividades cognitivas e de comunicação. O sistema disponibiliza informações e evidências, enquanto a interpretação, a definição de prioridades e os encaminhamentos permanecem sob responsabilidade de Carlos e da equipe. Dessa forma, o protótipo deve priorizar a continuidade da análise, a clareza dos indicadores e a facilidade de acesso às informações detalhadas.


## CTT — T03: Consultar síntese e comunicar pontos de investigação


**Autor(a):** Rafaela Altheman de Campos — 22.125.062-4

### Descrição

O CTT descreve o encadeamento entre preparar o panorama, interpretar indicadores e alertas, comunicar prioridades e registrar encaminhamentos. Na T03, Carlos (P03, cenário C03) usa a síntese do desempenho para conduzir uma reunião com a equipe.
A relação temporal mais importante é que Carlos pode suspender a apresentação para atender a uma dúvida, abrir a evidência e depois retomar a exposição do ponto em que parou (isso não equivale a encerrar a apresentação e começar outra).

Limites e exceções: <br> 
O sistema prepara a síntese a partir do escopo informado, mas identificar prioridades e comunicá-las continua sendo trabalho humano. <br>
A evidência detalhada só é aberta quando há uma pergunta ou necessidade de esclarecimento, e pode ser aberta mais de uma vez.

### Diagrama

![CTT T03](../assets/05_tarefas/ctt_t03.svg)

A tarefa abstrata A0 (consultar painel e comunicar pontos de investigação) se decompõe em quatro subtarefas abstratas, ligadas por habilitação (>>): preparar o painel (A1), interpretar a evolução do desempenho (A2), comunicar a interpretação à equipe (A3) e discutir e delegar (A4). Em A1, Carlos sente a necessidade de consultar o painel para se preparar para a reunião com os estudante (U11). Após isso, ele executa a tarefa de escolher o período de análise (I11), com passagem de informação ([]>>), para tarefa do sistema que prepara as métricas e os parâmetros ao longo do tempo (S12). Em A2, Carlos interpreta a evolução do desempenho (U21) e, em seguida, define os pontos a investigar (U22), ambas tarefas do usuário. Em A3, a apresentação da interpretação (U31) pode ser suspensa pela abertura de uma evidência (I32), que é interativa e repetível (*), e retomada do ponto em que parou (|>). Em A4, as tarefas do usuário de discutir os resultados (U41) e delegar tarefas (U42) ocorrem em qualquer ordem (|||) e fora do sistema, que se limita a preparar o painel e a exibir as evidências.

**Expressão temporal do modelo:**

```text
A0 = A1 >> A2 >> A3 >> A4
A1 = U11 >> I12 []>> S13
A2 = U21 >> U22
A3 = U31 |> I32*
A4 = U41 ||| U42
```

### Legenda e relações temporais usadas

| Operador/relação | Significado no diagrama | Exemplo no modelo |
|---|---|---|
| `>>` | **Habilitação:** indica que uma atividade depende da conclusão de uma etapa anterior para ser iniciada. | `A1 >> A2 >> A3 >> A4`: o painel é preparado antes de ser interpretado, comunicado e discutido. `U21 >> U22`: os pontos a investigar são definidos após a interpretação da evolução. `U11 >> I12`:  |
| `[]>>` | **Habilitação com passagem de informação:** indica que, além de habilitar a atividade seguinte, a etapa anterior fornece informações necessárias para sua execução. | `I11 []>> S12`: o período escolhido determina as métricas e os parâmetros exibidos no painel. |
| `\|\|\|` | **Concorrência:** indica que duas ou mais atividades podem ocorrer simultaneamente ou em qualquer ordem, sem uma sequência obrigatória entre elas. | `U41 \|\|\| U42`: Carlos e os estudantes discutem os resultados e delegam tarefas de acordo com as necessidades da reunião. |
| `\|>` | **Suspensão e retomada:** indica que uma atividade pode ser temporariamente interrompida para a execução de outra, sendo retomada posteriormente do ponto em que parou. | `U31 \|> I32`: durante a apresentação, Carlos interrompe momentaneamente a exposição para abrir uma evidência solicitada e, em seguida, retoma a apresentação do ponto anterior. |
| `*` | **Iteração:** indica que uma atividade pode ser repetida uma ou mais vezes durante o processo. | `I32*`: Carlos pode abrir diferentes evidências ou consultar a mesma evidência várias vezes durante a reunião. |

---

## Síntese da equipe

Problemas de interação: as três tarefas exigem decidir com contexto. Em T01, o risco é concluir por um único indicador (mais velocidade, mais quedas) ou sem baseline comparável. Em T02, é perder seleções e filtros entre a busca e a comparação, e confundir o que foi medido com a hipótese. Em T03, é perder período, indicador e ponto da apresentação ao abrir uma evidência durante a reunião.

Oportunidades: uma tela de comparação serve a T01 e T02, e o painel temporal de T03 reaproveita as mesmas métricas. Mostrar métricas e parâmetros na mesma linha do tempo ajuda a relacionar mudanças de configuração a mudanças de desempenho.

Requisitos principais:
- Mostrar o contexto da execução e do baseline (ID, versão, parâmetros) durante toda a análise.
- Apresentar as métricas lado a lado, com unidades, sem ocultar pioras.
- Oferecer busca por ID e filtros como caminhos equivalentes, preservando as seleções.
- Registrar decisão ou hipótese com justificativa, IDs e ressalvas, e confirmar o salvamento.
- Exibir o período de análise e permitir abrir uma evidência e voltar ao painel sem perder o estado.

Fora do escopo: delegar tarefas e priorizar automaticamente (responsabilidade de Carlos e os estudantes).

Protótipo e teste de usabilidade: as três tarefas entram, em duas frentes, uma tela de histórico e comparação (T01 e T02) e um painel temporal (T03). Os testes simulam uma avaliação (T01), a busca e comparação de duas execuções (T02) e uma reunião com interrupção para abrir evidência (T03).

## Checklist

- [X] Cada integrante produziu ao menos 1 HTA, 1 GOMS e 1 CTT.
- [X] Cada artefato identifica autor e tarefa.
- [X] Diagramas são legíveis e possuem fonte editável quando possível (SVG e DOT).
- [X] HTA contém planos, não apenas árvore de tópicos.
- [X] GOMS distingue Goals, Operators, Methods e Selection Rules.
- [X] CTT usa operadores temporais e tipos de tarefa coerentes com a notação adotada em aula.
- [X] Há texto explicando cada diagrama.
- [X] Tarefas estão ligadas a cenários/personas na rastreabilidade.
- [X] Em TCC técnico, as tarefas descrevem o que a pessoa faz com a contribuição/resultados, não passos internos do código.
- [X] CRUDs, relatórios, filtros e atividades administrativas foram escolhidos por relevância ao objetivo do usuário.

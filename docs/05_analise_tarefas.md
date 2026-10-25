# Entrega 5 — Análise de tarefas: HTA, GOMS e CTT

**Data:** 21/10/2026  
**Status:** 🟨 em andamento  
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
| T01 | Avaliar se o resultado de um treinamento representa uma melhoria real no desempenho do robô | P01 Rafael Martins / C01 | Frequente e alta: decisão equivocada pode provocar ajustes ineficazes e gasto computacional | Rafaela Altheman de Campos — 22.125.062-4 |
| T02 | Localizar e comparar execuções anteriores para explicar diferenças de desempenho | P02 Marina Oliveira / C02 | Recorrente e alta: exige rastreabilidade e comparabilidade entre experimentos | Manuella Filipe Peres — 22.224.029-3 |
| T03 | Consultar uma síntese do desempenho e comunicar à equipe os pontos que precisam de investigação | P03 Carlos Almeida / C03 | Periódica e alta: orienta reuniões e priorização de investigação | Letizia Lowatzki Baptistella — 22.125.063-2 |

> Priorize tarefas necessárias para que o usuário alcance objetivos centrais. Não desperdice a modelagem em ações triviais isoladas, como “clicar em login”, se o objetivo relevante é maior. Da mesma forma, não modele o funcionamento interno do algoritmo como se fosse uma tarefa humana.

---

## HTA — T01: Avaliar se um treinamento melhorou o desempenho


**Autor(a):** Rafaela Altheman de Campos — 22.125.062-4

### Descrição da tarefa

O objetivo é decidir se os resultados de um treinamento indicam uma melhoria útil para o desempenho do robô em partidas de futebol. A tarefa começa quando Rafael (P01), no cenário C01, tem acesso aos resultados de uma execução e termina quando registra uma conclusão fundamentada: considerar o resultado uma melhoria, rejeitá-lo como melhoria ou indicar que são necessárias mais evidências. A avaliação considera velocidade média, distância percorrida, taxa de quedas, estabilidade, gol, força de chute e localização, além da observação do comportamento do robô, quando houver esse tipo de registro.

### Diagrama

![HTA T01](../assets/05_tarefas/hta_t01.svg)

**Leitura do diagrama:** o objetivo 0 é decomposto em preparar a comparação (1), examinar evidências (2), classificar (3) e registrar (4). A subdivisão do item 3 representa uma escolha, não três ações consecutivas. A linha inferior dos nós 1.1, 1.2, 2.1, 2.2, 3.1–3.3 e 4 representa o nível operacional.

### Decomposição e planos

| ID | Objetivo ou operação | Plano/ordem | Problema de interação e decisão de design |
|---|---|---|---|
| 0 | Avaliar se um treinamento melhorou o desempenho | `1 > 2 > 3 > 4` | Informações da execução e da referência devem acompanhar toda a decisão para evitar conclusões sem contexto. |
| 1 | Identificar execução e referência | `1.1 > 1.2` | Mostrar identificadores, datas, versões, ambiente e parâmetros antes da comparação. |
| 1.1 | Abrir treinamento avaliado | operação | Diferenciar execução concluída, em andamento, com erro e sem dados disponíveis. |
| 1.2 | Selecionar baseline comparável | operação; se não existir, registrar a limitação e seguir para a saída de evidências insuficientes | Informar claramente compatibilidade ou divergência de condições; não escolher referência automaticamente sem identificação. |
| 2 | Examinar evidências | `2.1 + 2.2` | Reunir indicadores complementares sem ocultar pioras em outras métricas. |
| 2.1 | Comparar métricas de desempenho | operação | Apresentar velocidade média, distância percorrida, taxa de quedas, gols marcadose e força de chute com unidades. |
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

## GOMS — T02: Localizar e comparar execuções anteriores


**Autor(a):** Manuella Filipe Peres — 22.224.029-3

### Goal

`G0: Localizar duas execuções anteriores, comparar seus resultados e registrar uma hipótese rastreável para as diferenças encontradas.`

**Subobjetivos:** `G1` localizar as duas execuções; `G2` comparar métricas e parâmetros; `G3` formular a hipótese; `G4` egistrar hipótese, evidências e ressalvas.

### Métodos, operadores e regras de seleção

### G1: Localizar as duas execuções
#### Method M1: localizar por identificadores conhecidos
• O1 (cognição): recuperar o ID da primeira execução.
• O2 (interação): apontar e clicar no campo de busca.
• O3 (interação): digitar o ID.
• O4 (interação): acionar a busca.
• O5 (percepção): conferir se o registro apresentado (ID, data, versão) é o esperado.
• O6 (interação): adicionar a execução à comparação.
• O7 (cognição/interação): repetir O1–O6 para a segunda execução.
#### Method M2: localizar por filtros do histórico
• O1 (interação): acessar o histórico de execuções.
• O2 (cognição): definir as pistas disponíveis (período, versão, configuração).
• O3 (interação): selecionar os filtros e acionar a consulta.
• O4 (percepção): ler a lista e conferir os metadados dos resultados.
• O5 (interação): selecionar a primeira e a segunda execução e adicioná-las à comparação.

#### Regras de seleção de G1
• SR1: usar M1 quando Marina conhecer os IDs das duas execuções. Usar M2 quando um ou ambos forem desconhecidos, mas houver atributos suficientes para filtrar.
• SR2: se a busca por ID falhar (O5 do M1 não confere), revisar o ID. Se continuar sem resultado, mudar para M2. Se os filtros do M2 trouxerem resultados demais, refiná-los antes de selecionar (voltar a O3).

### G2: Comparar métricas e parâmetros
#### Method M1
• O1 (interação): abrir a comparação entre as duas execuções.
• O2 (percepção): ler lado a lado os valores das métricas, com unidades.
• O3 (percepção/cognição): identificar quais parâmetros, versões e métricas divergem.
• O4 (cognição): separar o que foi medido (diferença observada) do que seria apenas uma explicação possível.

### G3: Formular a hipótese
#### Method M1
• O1 (cognição): relacionar as divergências de parâmetros ou versão às diferenças de desempenho e formular uma hipótese.
• O2 (cognição): decidir que ressalvas se aplicam. Uma diferença de versão, sozinha, não prova a causa da diferença de desempenho.

### G4: Registrar hipótese, evidências e ressalvas
#### Method M1
• O1 (interação): digitar a hipótese, as evidências, os IDs das duas execuções e as ressalvas.
• O2 (interação): salvar o registro.
• O3 (percepção): confirmar que o registro foi salvo e ficou associado aos IDs.


### **Interpretação do GOMS:** 
O critério que separa M1 de M2 é informação de que Marina dispõe no início da tarefa, e não uma preferência arbitrária por tela. Ambos alcançam a mesma meta e terminam com um registro contextualizado. A análise revela a necessidade de preservar seleções e filtros entre pesquisa e comparação, além de diferenciar o que foi medido da explicação que Marina propõe. Não se supõe que uma diferença de versão, sozinha, prove a causa da diferença de desempenho.

---

## CTT — T03: Consultar síntese e comunicar pontos de investigação


**Autor(a):** Letizia Lowatzki Baptistella — 22.125.063-2

### Descrição

O CTT descreve o encadeamento entre preparar o panorama, interpretar indicadores e alertas, apresentar prioridades e registrar encaminhamentos. A relação temporal mais importante para esse cenário é que Carlos pode **suspender a apresentação** para atender a uma dúvida, abrir a evidência e depois **retomar** a exposição do ponto em que parou. Isso não equivale a encerrar a apresentação e começar outra do zero.

**Limites e exceções:** o processamento do sistema prepara a síntese a partir do escopo informado, mas a identificação de prioridades e a comunicação continuam sendo humanas. A consulta de evidência detalhada ocorre quando houver uma pergunta ou necessidade de esclarecimento. Se o sistema não apresentar dados suficientes, Carlos comunica a limitação e não cria encaminhamento baseado em certeza indevida.

### Diagrama

![CTT T03](../assets/05_tarefas/ctt_t03.svg)

**Hierarquia e tipos de tarefa:** `A0` (comunicar panorama), `A1` (preparar), `A2` (interpretar), `A3` (comunicar) e `A4` (registrar) são **abstratas**. `I11` (escolher período), `I32` (abrir evidência) e `I41` (registrar ações) são **interativas**. `S12` (preparar síntese) e `S42` (persistir encaminhamentos) são **do sistema**. `U21` (interpretar indicadores), `U22` (interpretar alertas), `U23` (definir prioridades) e `U31` (apresentar descobertas) são **do usuário**.

**Expressão temporal do modelo:**

```text
A0 = A1 >> A2 >> A3 >> A4
A1 = I11 []>> S12
A2 = (U21 ||| U22) >> U23
A3 = U31 |> I32  (I32 ocorre quando há necessidade de consultar evidências)
A4 = I41 []>> S42
```

### Legenda e relações temporais usadas

| Operador/relação | Significado no diagrama | Exemplo no modelo |
|---|---|---|
| `>>` | Habilitação: exige conclusão da etapa anterior. | `A1 >> A2 >> A3 >> A4`: preparar a síntese antes de interpretá-la e comunicar prioridades. |
| `[]>>` | Habilitação com passagem de informação. | `I11 []>> S12`: o período selecionado determina os resultados; `I41 []>> S42`: ações informadas são salvas. |
| `\|\|\|` | Concorrência: atividades que podem ocorrer em qualquer ordem ou concomitantemente. | `U21 \|\|\| U22`: examinar tendências e alertas, antes da priorização. |
| `\|>` | Suspensão e retomada: uma atividade pode ser interrompida pela outra e prosseguir de onde parou. | `U31 \|> I32`: interromper momentaneamente a apresentação, abrir evidência solicitada e voltar ao ponto anterior. |

**Interpretação e implicações de design:** a preparação dos dados depende diretamente do escopo indicado; por isso, o período selecionado deve estar visível na síntese. Indicadores gerais e alertas precisam ser lidos de maneira complementar para que a priorização tenha fundamento. Durante a reunião, a interface precisa preservar filtros, indicador escolhido e posição da apresentação quando uma evidência é aberta. A confirmação dos encaminhamentos ao final garante que a comunicação gere próximos passos recuperáveis, e não apenas uma conversa sem registro.

**Situação para o teste de usabilidade:** simular uma reunião em que Carlos deve explicar uma regressão, receber uma pergunta sobre sua origem, abrir a execução correspondente e retornar ao panorama sem redefinir período e seleção. Avaliar também se registra pelo menos um próximo passo vinculado ao achado.

---

## Síntese da equipe

Quais problemas de interação, oportunidade e requisitos apareceram a partir das modelagens? Quais tarefas irão para o protótipo e para o teste de usabilidade?

## Checklist

- [ ] Cada integrante produziu ao menos 1 HTA, 1 GOMS e 1 CTT.
- [ ] Cada artefato identifica autor e tarefa.
- [ ] Diagramas são legíveis e possuem fonte editável quando possível (SVG e DOT).
- [ ] HTA contém planos, não apenas árvore de tópicos.
- [ ] GOMS distingue Goals, Operators, Methods e Selection Rules.
- [ ] CTT usa operadores temporais e tipos de tarefa coerentes com a notação adotada em aula.
- [ ] Há texto explicando cada diagrama.
- [ ] Tarefas estão ligadas a cenários/personas na rastreabilidade.
- [ ] Em TCC técnico, as tarefas descrevem o que a pessoa faz com a contribuição/resultados, não passos internos do código.
- [ ] CRUDs, relatórios, filtros e atividades administrativas foram escolhidos por relevância ao objetivo do usuário.

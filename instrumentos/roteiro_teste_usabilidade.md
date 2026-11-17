
# Roteiro de teste de usabilidade

**Projeto:** Plataforma de análise de resultados de treinamentos de robôs humanoides  
**Equipe 27:** Letizia Lowatzki Baptistella, Manuella Filipe Peres e Rafaela Altheman de Campos  
**Protótipo:** [IHC — Figma](https://www.figma.com/proto/qHpoJxQF4Sthdy99w7Scul/IHC?node-id=32-2023&p=f&scaling=min-zoom&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=32%3A2023)  
**Participante previsto:** U01 — um participante externo à equipe  
**Duração da sessão inicial:** aproximadamente 25–35 minutos

## 1. Antes da sessão

- verificar protótipo/versão;
- testar gravação e áudio;
- abrir formulários/planilhas;
- limpar dados de sessão/conta de teste;
- separar instruções das tarefas;
- confirmar consentimento e duração;
- quando o protótipo usar resultados/processamentos simulados, preparar dados realistas e manter a simulação consistente entre participantes.

**Preparação específica:**

- Abrir o protótipo no frame inicial "01 · Consultar visão geral" (32:2023).
- Conferir o caminho de "02 · Localizar treinamento" para "03 · Selecionar execuções".
- Verificar a disponibilidade das execuções EXEC-104 e EXEC-103.
- Conferir as telas "04 · Comparar métricas e parâmetros", "05 · Verificar comparabilidade" e "06 · Registrar hipótese e ressalvas".
- Conferir o caminho "08 · Avaliar desempenho" e a confirmação "09 · Conferir avaliação registrada".
- Conferir a sequência "15 · Apresentar indicadores · Velocidade média", "43 · Observar evidência da execução" e o retorno à apresentação.
- Preparar o gabarito com as diferenças entre as execuções e as ressalvas de comparabilidade.
- Utilizar cronômetro para UT01 e UT02 e medição separada de consulta e retorno em UT03.
- Realizar um ensaio interno para verificar os caminhos navegáveis.
- Aplicar UT02 primeiro, preservando a avaliação de primeiro contato da MU09.

## 2. Abertura padronizada

- agradecer participação;
- explicar objetivo geral sem revelar hipóteses específicas;
- reforçar que o produto, não a pessoa, está sendo avaliado;
- explicar possibilidade de interrupção;
- obter consentimento;
- explicar *think aloud* apenas se essa técnica for usada.

**Texto de abertura:**

"Obrigado por participar deste teste. Nossa equipe desenvolveu um protótipo que permite consultar, comparar e analisar resultados de treinamentos de um robô humanoide.

Durante a avaliação, você realizará algumas atividades utilizando a interface. Queremos observar se as informações são claras e se é possível completar as tarefas sem dificuldades excessivas.

Estamos avaliando o protótipo, não os seus conhecimentos. Não existem penalidades por erros ou dificuldades.

Você pode interromper sua participação a qualquer momento. Durante as tarefas, evitaremos indicar onde clicar, pois queremos entender como a própria interface orienta sua utilização."

### Quando a interface é um protótipo de aplicação do tema do TCC

Explique de forma simples que a sessão avalia **como a pessoa interage com o protótipo**, e não a precisão/desempenho científico do algoritmo, modelo ou estudo do TCC.

Se algum resultado técnico estiver simulado, não engane o participante sobre o nível de implementação. Use uma explicação compatível com o objetivo do teste, sem antecipar o caminho da tarefa.

**Explicação ao participante:**

"Os treinamentos, métricas e resultados apresentados nesta interface podem conter informações ilustrativas ou simuladas. O protótipo não executa novos treinamentos nem controla o robô.

Nosso objetivo é avaliar a interação com as informações apresentadas e não verificar o desempenho científico do algoritmo do TCC."

## 3. Perfil pré-teste

Colete somente informações relevantes à interpretação dos resultados: experiência com domínio, frequência de uso de soluções similares, familiaridade com ferramentas profissionais, necessidades de acessibilidade pertinentes etc.

Para perfis especializados (DBA, analista, pesquisador, administrador, técnico), registre os critérios usados para considerar o participante representativo. Se for participante proxy, registre essa condição e a limitação.

**Perguntas de caracterização:**

1. Você possui experiência com computação, programação, robótica ou análise de dados?
2. Já utilizou ferramentas com gráficos, métricas ou resultados de experimentos?
3. Com que frequência utiliza sistemas semelhantes?
4. Você conhece os termos execução, parâmetros, métricas e baseline?
5. Existe alguma necessidade de acessibilidade relevante para a realização da atividade?

A experiência do participante será registrada para determinar sua proximidade com as personas da Entrega 3. Caso não represente diretamente um usuário do domínio, será identificado como participante proxy.

## 4. Tarefas

| ID | Instrução ao participante | O moderador pode esclarecer | O moderador não deve dizer |
|---|---|---|---|
| UT01 | "Sua equipe concluiu um treinamento e precisa decidir se ele apresentou melhoria em relação a uma execução anterior. Analise os resultados disponíveis e registre uma conclusão justificada." | Que a análise deve considerar os resultados apresentados e eventuais limitações da comparação. | Quais indicadores escolher, qual classificação registrar ou onde localizar o botão de salvamento. |
| UT02 | "Sua equipe deseja comparar os treinamentos EXEC-104 e EXEC-103. Localize os dois registros, analise as diferenças e registre uma hipótese que considere também as limitações das informações disponíveis." | O significado geral de "execução" como um treinamento já realizado, sem indicar os controles. | Onde fica o histórico, como selecionar as execuções, qual campo preencher ou qual hipótese escrever. |
| UT03 | "Durante uma reunião, você precisa apresentar o resultado de velocidade média de um treinamento. Consulte uma evidência mais detalhada e retome a apresentação no mesmo ponto." | Que o objetivo é consultar uma evidência e continuar a reunião. | Qual botão abre a evidência, qual caminho seguir ou como retornar à apresentação. |
| UT04 | "Retome a atividade de consultar o histórico de treinamentos realizada em sua primeira participação." | Apenas repetir o objetivo da tarefa, sem demonstrar o procedimento. | Reapresentar tutorial, indicar filtros ou ensinar novamente o caminho de consulta. |

Tarefas podem envolver, conforme o escopo: localizar informação em dashboard; filtrar histórico; configurar análise; comparar resultados; gerar relatório; revisar alerta; editar permissão; recuperar-se de falha.

A tarefa deve expressar **objetivo do usuário**, e não “clique no filtro”, “abra o CRUD” ou “vá ao dashboard”.

**Ordem efetiva da sessão inicial:** UT02 → UT01 → UT03.

**Orientação inicial:** até 5 minutos, sem demonstrar o caminho necessário para consultar o histórico, conforme MU09.

**UT04:** prevista para sete dias depois, conforme MU10 da Entrega 8. Se não ocorrer uma segunda sessão, será documentada como não avaliada.

## 5. Durante a tarefa

Registrar início/fim, sucesso, erros, hesitações, comentários, pedidos de ajuda e intervenções do moderador. Não transformar silêncio do participante em “problema” sem evidência adicional.

Observe também, quando pertinente:

- compreensão de métricas/termos técnicos;
- percepção de status de processamento;
- escolha e remoção de filtros;
- interpretação de estados vazios/erro;
- prevenção de ações destrutivas;
- entendimento de papéis/permissões;
- confiança ao interpretar resultados/recomendações.

**Observações específicas do protótipo:**

- Verificar se o participante localiza corretamente EXEC-104 e EXEC-103.
- Observar se compreende o aumento de velocidade e distância e a redução do indicador de estabilidade.
- Verificar se percebe que as condições de treinamento ainda não estão totalmente confirmadas.
- Observar se distingue diferenças observadas de hipóteses explicativas.
- Verificar se consegue registrar uma hipótese e uma ressalva.
- Observar se interpreta as classificações "Melhoria", "Não melhoria" e "Evidências insuficientes".
- Registrar o reconhecimento da mensagem de confirmação após uma avaliação.
- Na reunião, verificar se retorna à apresentação preservando o contexto de velocidade média.
- Registrar o tempo específico da consulta de evidência e retorno para MU05.
- Registrar erros críticos relacionados à interpretação e ao registro para MU07.

**Dados apresentados no Figma:**

| Indicador | EXEC-104 | EXEC-103 |
|---|---:|---:|
| Velocidade | 0,32 (unidade a padronizar) | 0,28 (unidade a padronizar) |
| Distância | 18,3 m | 16,8 m |
| Quedas | 12 | 8 |
| Estabilidade | 78% | 88% |
| Gols / força de chute | 2 / 40 N | 2 / 34 N |

Esses dados aparecem na tela de comparação do Figma. A unidade de velocidade deverá ser corrigida ou esclarecida antes da aplicação, pois há divergência entre painel e comparação.

O participante deverá perceber que houve diferenças favoráveis em algumas métricas e desfavoráveis em outras, sem presumir causalidade ou equivalência de condições.

Como a interface possui campos com preenchimento simulado, uma limitação de interação não será considerada automaticamente um erro do participante.

## 6. Pós-tarefa

Aplicar a escala definida no plano (por exemplo 1–7) e registrar comentário curto: “O que tornou essa tarefa fácil ou difícil?”

**Escala adotada — MU06 da Entrega 8:**

"Em uma escala de 1 a 5, como você avalia a facilidade de realizar esta tarefa?"

- 1 — Muito difícil.
- 2 — Difícil.
- 3 — Nem fácil, nem difícil.
- 4 — Fácil.
- 5 — Muito fácil.

**Pergunta complementar:**

"O que tornou essa tarefa fácil ou difícil?"

A resposta será registrada após cada tarefa, sem oferecer sugestões ao participante.

## 7. Encerramento

- perguntas gerais;
- agradecer;
- confirmar como os dados serão usados;
- salvar registros com ID anônimo;
- registrar limitações de perfil, ambiente ou simulação que afetem a interpretação.

**Perguntas finais:**

1. Qual atividade você achou mais fácil?
2. Qual atividade apresentou maior dificuldade?
3. Os indicadores e os resultados foram compreensíveis?
4. Houve algum momento em que você não soube como continuar?
5. O que você mudaria para melhorar a interface?

**Texto de encerramento:**

"Obrigado pela sua participação. As informações serão utilizadas exclusivamente para fins acadêmicos, de maneira anônima, para ajudar nossa equipe a identificar dificuldades e oportunidades de melhoria na interface."

Ao finalizar, os registros serão identificados pelo código U01 e as limitações do protótipo serão documentadas.

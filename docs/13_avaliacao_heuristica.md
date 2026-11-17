# Entrega 13 — Avaliação de IHC por inspeção heurística

**Data:** 16/11/2026  
**Status:** em andamento
**Responsabilidade:** Avaliação da interface pelos integrantes da equipe.

## Objetivo da atividade

Esta entrega tem como objetivo avaliar a interface do projeto por meio de inspeção heurística, utilizando as dez heurísticas de usabilidade propostas por Jakob Nielsen.

A avaliação busca identificar problemas relacionados à usabilidade, consistência, compreensão das informações, prevenção de erros e recuperação de situações inesperadas.

Por se tratar de uma interface administrativa e analítica, também são considerados aspectos como a clareza dos indicadores, a padronização das unidades de medida, a comparação entre execuções e a apresentação das condições de treinamento.

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

https://www.figma.com/proto/qHpoJxQF4Sthdy99w7Scul/IHC?node-id=32-2023&t=MJOhlZgAfoJJp8Dt-1&scaling=min-zoom&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=32%3A2023

**Versão avaliada:** Protótipo da Entrega 11 — Figma IHC.

**Data de referência:** 16/11/2026.

Foram considerados os seguintes elementos e estados da interface:

| Elemento | Aspectos avaliados |
|---|---|
| P01 — Painel principal | Apresentação dos indicadores e informações gerais das execuções. |
| P03 — Comparação | Comparação entre execuções e apresentação das diferenças identificadas. |
| Tela 04 | Apresentação das métricas e das condições de treinamento. |
| Tela 05 | Informações relacionadas às condições de treinamento não confirmadas. |
| P06 | Confirmação de registros e ações realizadas. |
| P09 | Estado de pesquisa sem resultados. |
| P10 | Estado vazio do painel. |
| Tela 15 | Apresentação dos indicadores. |
| Tela 29 | Resultado de pesquisa sem correspondências. |
| Tela 33 | Apresentação de erro e possibilidade de nova tentativa. |
| Tela 37 | Investigação de dados ausentes. |
| Tela 43 | Consulta de evidências. |
| Tela 45 | Recuperação de erro relacionado a um registro. |

Também foram considerados os seguintes estados:

- **Estado vazio:** P10 e tela 42.
- **Estado de erro:** telas 33 e 45.
- **Pesquisa sem resultados:** P09 e tela 29.
- **Confirmação:** P06 e telas 07, 09 e 21.
- **Condições não confirmadas:** telas 04 e 05.

Os estados de carregamento e de permissões não fizeram parte do escopo documentado desta inspeção.

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

## 4. Matriz de cobertura das 10 heurísticas

| Heurística | Elementos analisados | Resultado |
|---|---|---|
| H1 — Visibilidade do estado do sistema | P06, telas 07, 09 e 21 | Não foi identificada violação específica nos elementos examinados. |
| H2 — Correspondência entre o sistema e o mundo real | P01, P03 e tela 04 | Identificada inconsistência na unidade de velocidade da execução EXEC-104. |
| H3 — Controle e liberdade do usuário | Telas 15, 43 e 45 | Não foi identificada violação específica nos elementos examinados. |
| H4 — Consistência e padronização | P01, P03, telas 04 e 05 | Identificadas inconsistências na unidade de velocidade e na apresentação das condições de treinamento. |
| H5 — Prevenção de erros | P03, telas 05 e 06 | Identificada possibilidade de interpretação incorreta das condições de treinamento. |
| H6 — Reconhecimento em vez de memorização | Telas 02, 03 e 43 | Não foi identificada violação específica nos elementos examinados. |
| H7 — Flexibilidade e eficiência de uso | Telas 02, 04 e 15 a 18 | Não foi identificada violação específica nos elementos examinados. |
| H8 — Estética e design minimalista | P01, P03 e P10 | Identificado erro de digitação na mensagem do estado vazio. |
| H9 — Reconhecimento, diagnóstico e recuperação de erros | P09, telas 29, 33 e 45 | Não foi identificada violação específica nos elementos examinados. |
| H10 — Ajuda e documentação | Telas 02, 05 e 37 | Não foi identificada violação específica nos elementos examinados. |

## 5. Declaração de violações

### V01 — Inconsistência na unidade de velocidade da execução EXEC-104

**Heurísticas relacionadas:** H2 — Correspondência entre o sistema e o mundo real; H4 — Consistência e padronização.

**Localização:** P01, P03 e tela 04.

**Descrição:**

Foi identificada uma inconsistência na apresentação da velocidade da execução EXEC-104.

No painel principal P01, a velocidade aparece como `0,32 m/s`. Já na tela de comparação P03 e na tela 04, o valor aparece como `0.32 cm/s`.

A utilização de unidades diferentes para representar a mesma métrica pode levar o usuário a interpretar incorretamente o desempenho da execução.

**Severidade:** 4 — Catastrófico.

**Recomendação:**

Padronizar a unidade de velocidade em todas as telas, garantindo que o mesmo indicador seja apresentado com a mesma unidade e convenção numérica. Também é necessário verificar se os valores apresentados correspondem à mesma grandeza antes de realizar a comparação.

### V02 — Ambiguidade na indicação das condições de treinamento

**Heurísticas relacionadas:** H4 — Consistência e padronização; H5 — Prevenção de erros.

**Localização:** P03, tela 04 e tela 05.

**Descrição:**

Foi identificada uma diferença na forma como as condições de treinamento são apresentadas.

Na tela P03, aparece a informação `Diferença de configuração: Nenhuma`. Entretanto, na tela 04, é apresentada a mensagem `Condições de treinamento: não confirmadas`, enquanto na tela 05 aparece `Condições não confirmadas`.

A informação de que não existe diferença de configuração pode ser interpretada como uma confirmação de equivalência entre as execuções. Entretanto, a ausência de confirmação das condições não permite concluir que elas sejam iguais.

**Severidade:** 3 — Grave.

**Recomendação:**

Diferenciar claramente a ausência de diferenças identificadas da ausência de informações suficientes para confirmar as condições de treinamento. Quando as condições não puderem ser verificadas, essa limitação deve ser apresentada de maneira explícita.

### V03 — Erro de digitação na mensagem do estado vazio

**Heurística relacionada:** H8 — Estética e design minimalista.

**Localização:** P10.

**Descrição:**

No estado vazio do painel, foi identificada a mensagem:

`Não há resultados dsponíveis no período escolhido`.

A palavra `dsponíveis` apresenta um erro de digitação, o que prejudica o acabamento textual da interface.

**Severidade:** 1 — Cosmético.

**Recomendação:**

Corrigir a mensagem para:

`Não há resultados disponíveis no período escolhido`.

## 6. Boas práticas — heurísticas sem violações identificadas

Durante a análise dos elementos disponíveis, foram observados exemplos positivos relacionados às seguintes heurísticas:

| Heurística | Boa prática observada |
|---|---|
| H1 — Visibilidade do estado do sistema | A interface apresenta estados de confirmação em ações relacionadas a registros. |
| H3 — Controle e liberdade do usuário | A apresentação de mensagens de erro permite identificar situações que exigem atenção. |
| H6 — Reconhecimento em vez de memorização | A interface apresenta opções de consulta e seleção de execuções. |
| H7 — Flexibilidade e eficiência de uso | A organização das telas facilita a consulta de indicadores e informações das execuções. |
| H9 — Recuperação de erros | Existem telas destinadas à apresentação de erros e à recuperação de situações problemáticas. |
| H10 — Ajuda e documentação | A apresentação de informações e evidências auxilia a compreensão dos resultados. |

---

# Avaliador A02 — Letizia Lowatzki Baptistella

## 4. Matriz de cobertura das 10 heurísticas

| Heurística | Elementos analisados | Resultado |
|---|---|---|
| H1 — Visibilidade do estado do sistema | P06, telas 07, 09 e 21 | Não foi identificada violação específica nos elementos examinados. |
| H2 — Correspondência entre o sistema e o mundo real | P01, P03 e tela 04 | Identificada inconsistência na unidade de velocidade da execução EXEC-104. |
| H3 — Controle e liberdade do usuário | Telas 15, 43 e 45 | Não foi identificada violação específica nos elementos examinados. |
| H4 — Consistência e padronização | P01, P03, telas 04 e 05 | Identificadas inconsistências na apresentação das métricas e condições de treinamento. |
| H5 — Prevenção de erros | P03, telas 05 e 06 | Identificada possibilidade de interpretação equivocada das condições de treinamento. |
| H6 — Reconhecimento em vez de memorização | Telas 02, 03 e 43 | Não foi identificada violação específica nos elementos examinados. |
| H7 — Flexibilidade e eficiência de uso | Telas 02, 04 e 15 a 18 | Não foi identificada violação específica nos elementos examinados. |
| H8 — Estética e design minimalista | P01, P03 e P10 | Identificado erro textual no estado vazio. |
| H9 — Reconhecimento, diagnóstico e recuperação de erros | P09, telas 29, 33 e 45 | Não foi identificada violação específica nos elementos examinados. |
| H10 — Ajuda e documentação | Telas 02, 05 e 37 | Não foi identificada violação específica nos elementos examinados. |

## 5. Declaração de violações

### V01 — Inconsistência na unidade de velocidade da execução EXEC-104

**Heurísticas relacionadas:** H2 e H4.

**Localização:** P01, P03 e tela 04.

**Descrição:**

A execução EXEC-104 apresenta unidades de velocidade diferentes entre as telas. No painel principal, o indicador aparece como `0,32 m/s`, enquanto na comparação aparece como `0.32 cm/s`.

Essa diferença compromete a consistência das informações e pode prejudicar a interpretação dos resultados.

**Severidade:** 4 — Catastrófico.

**Recomendação:**

Adotar uma unidade padronizada para a velocidade e garantir que a mesma representação seja utilizada no painel principal, na comparação e nas demais telas que apresentem esse indicador.

### V02 — Ambiguidade na indicação das condições de treinamento

**Heurísticas relacionadas:** H4 e H5.

**Localização:** P03, tela 04 e tela 05.

**Descrição:**

A interface apresenta informações que podem gerar interpretações diferentes sobre a equivalência entre as condições de treinamento.

A mensagem `Diferença de configuração: Nenhuma` não deixa claro se as condições foram efetivamente verificadas ou se não foi possível identificar diferenças devido à ausência de informações.

**Severidade:** 3 — Grave.

**Recomendação:**

Utilizar mensagens distintas para indicar condições confirmadas, diferenças identificadas e condições não verificadas. Dessa forma, o usuário não interpreta a ausência de dados como confirmação de equivalência.

### V03 — Erro de digitação na mensagem do estado vazio

**Heurística relacionada:** H8.

**Localização:** P10.

**Descrição:**

A mensagem do estado vazio apresenta a palavra `dsponíveis` em vez de `disponíveis`.

**Severidade:** 1 — Cosmético.

**Recomendação:**

Corrigir a mensagem textual para garantir clareza e padronização da comunicação com o usuário.

## 6. Boas práticas — heurísticas sem violações identificadas

| Heurística | Boa prática observada |
|---|---|
| H1 — Visibilidade do estado do sistema | A interface apresenta informações de confirmação para determinadas ações. |
| H3 — Controle e liberdade do usuário | As telas de erro permitem reconhecer situações que exigem atenção. |
| H6 — Reconhecimento em vez de memorização | As opções de consulta e seleção estão organizadas visualmente. |
| H7 — Flexibilidade e eficiência de uso | A organização dos indicadores favorece a consulta das informações. |
| H9 — Recuperação de erros | A interface contempla estados de erro e mensagens relacionadas à recuperação. |
| H10 — Ajuda e documentação | A apresentação de evidências contribui para a compreensão dos resultados. |

---

# Avaliador A03 — Rafaela Altheman de Campos

## 4. Matriz de cobertura das 10 heurísticas

| Heurística | Elementos analisados | Resultado |
|---|---|---|
| H1 — Visibilidade do estado do sistema | P06, telas 07, 09 e 21 | Não foi identificada violação específica nos elementos examinados. |
| H2 — Correspondência entre o sistema e o mundo real | P01, P03 e tela 04 | Identificada inconsistência na unidade de velocidade da execução EXEC-104. |
| H3 — Controle e liberdade do usuário | Telas 15, 43 e 45 | Não foi identificada violação específica nos elementos examinados. |
| H4 — Consistência e padronização | P01, P03, telas 04 e 05 | Identificadas inconsistências na apresentação de unidades e condições de treinamento. |
| H5 — Prevenção de erros | P03, telas 05 e 06 | Identificada possibilidade de interpretação incorreta das condições de treinamento. |
| H6 — Reconhecimento em vez de memorização | Telas 02, 03 e 43 | Não foi identificada violação específica nos elementos examinados. |
| H7 — Flexibilidade e eficiência de uso | Telas 02, 04 e 15 a 18 | Não foi identificada violação específica nos elementos examinados. |
| H8 — Estética e design minimalista | P01, P03 e P10 | Identificado erro de digitação na mensagem do estado vazio. |
| H9 — Reconhecimento, diagnóstico e recuperação de erros | P09, telas 29, 33 e 45 | Não foi identificada violação específica nos elementos examinados. |
| H10 — Ajuda e documentação | Telas 02, 05 e 37 | Não foi identificada violação específica nos elementos examinados. |

## 5. Declaração de violações

### V01 — Inconsistência na unidade de velocidade da execução EXEC-104

**Heurísticas relacionadas:** H2 e H4.

**Localização:** P01, P03 e tela 04.

**Descrição:**

Foi observada uma divergência na unidade de velocidade da execução EXEC-104. O painel principal apresenta `0,32 m/s`, enquanto a tela de comparação apresenta `0.32 cm/s`.

A diferença na unidade pode comprometer a interpretação da métrica e a comparação entre execuções.

**Severidade:** 4 — Catastrófico.

**Recomendação:**

Padronizar a unidade de velocidade em todas as telas e verificar a correspondência entre os valores apresentados.

### V02 — Ambiguidade na indicação das condições de treinamento

**Heurísticas relacionadas:** H4 e H5.

**Localização:** P03, tela 04 e tela 05.

**Descrição:**

A apresentação das condições de treinamento não é suficientemente clara para diferenciar uma configuração sem diferenças de uma configuração cujas condições não foram confirmadas.

Essa situação pode levar o usuário a considerar duas execuções equivalentes sem que existam informações suficientes para confirmar essa conclusão.

**Severidade:** 3 — Grave.

**Recomendação:**

Reformular as mensagens para deixar explícito quando as condições foram verificadas, quando existem diferenças e quando não há informações suficientes para realizar a comparação.

### V03 — Erro de digitação na mensagem do estado vazio

**Heurística relacionada:** H8.

**Localização:** P10.

**Descrição:**

A mensagem `Não há resultados dsponíveis no período escolhido` apresenta um erro de digitação.

**Severidade:** 1 — Cosmético.

**Recomendação:**

Substituir `dsponíveis` por `disponíveis`.

## 6. Boas práticas — heurísticas sem violações identificadas

| Heurística | Boa prática observada |
|---|---|
| H1 — Visibilidade do estado do sistema | A interface apresenta estados de confirmação em determinadas ações. |
| H3 — Controle e liberdade do usuário | A existência de telas de erro contribui para a identificação de situações inesperadas. |
| H6 — Reconhecimento em vez de memorização | As opções de seleção e consulta são apresentadas na interface. |
| H7 — Flexibilidade e eficiência de uso | A organização das informações facilita a consulta dos indicadores. |
| H9 — Recuperação de erros | A interface apresenta mensagens relacionadas a erros e situações que exigem recuperação. |
| H10 — Ajuda e documentação | A apresentação de evidências auxilia a interpretação das informações. |

---

# 7. Consolidação da equipe

Após a análise dos elementos da interface, foram consolidados três problemas principais.

Os problemas estão relacionados à consistência das informações, à clareza das condições de treinamento e à qualidade textual das mensagens apresentadas ao usuário.

## 7.1. Quadro consolidado de problemas

| ID | Problema | Heurísticas | Localização | Severidade |
|---|---|---|---|---|
| V01 | Inconsistência na unidade de velocidade da execução EXEC-104 | H2 e H4 | P01, P03 e tela 04 | 4 |
| V02 | Ambiguidade na indicação das condições de treinamento | H4 e H5 | P03, telas 04 e 05 | 3 |
| V03 | Erro de digitação na mensagem do estado vazio | H8 | P10 | 1 |

## 7.2. Priorização das melhorias

A priorização considera o impacto dos problemas sobre a interpretação das informações e a utilização da interface.

| Prioridade | Problema | Justificativa |
|---|---|---|
| 1 | V01 | A divergência de unidade pode comprometer a interpretação de uma métrica importante e a comparação entre execuções. |
| 2 | V02 | A ambiguidade pode levar o usuário a interpretar condições não verificadas como equivalentes. |
| 3 | V03 | O erro textual prejudica o acabamento da interface, mas não impede a compreensão geral da mensagem. |

## 7.3. Relação entre problemas e heurísticas

| Heurística | Problemas relacionados |
|---|---|
| H1 | Nenhuma violação específica identificada. |
| H2 | V01. |
| H3 | Nenhuma violação específica identificada. |
| H4 | V01 e V02. |
| H5 | V02. |
| H6 | Nenhuma violação específica identificada. |
| H7 | Nenhuma violação específica identificada. |
| H8 | V03. |
| H9 | Nenhuma violação específica identificada. |
| H10 | Nenhuma violação específica identificada. |

## 8. Síntese e plano de melhoria

A avaliação identificou três problemas que podem prejudicar a experiência do usuário.

O primeiro está relacionado à inconsistência na unidade de velocidade da execução EXEC-104. A apresentação de unidades diferentes pode comprometer a interpretação dos resultados e gerar comparações incorretas.

O segundo problema está relacionado à ambiguidade das informações sobre as condições de treinamento. A interface precisa diferenciar a ausência de diferenças identificadas da impossibilidade de confirmar as condições.

O terceiro problema está relacionado a um erro de digitação na mensagem apresentada no estado vazio do painel. Embora seja um problema de menor severidade, sua correção contribui para a qualidade da comunicação.

### 8.1. Plano de melhoria

| ID | Ação recomendada | Resultado esperado |
|---|---|---|
| V01 | Padronizar a unidade de velocidade e revisar os valores apresentados em todas as telas. | Garantir consistência na apresentação e permitir comparação adequada entre execuções. |
| V02 | Diferenciar as mensagens de ausência de diferenças e de condições não confirmadas. | Evitar interpretações equivocadas sobre a equivalência entre execuções. |
| V03 | Corrigir a palavra `dsponíveis` para `disponíveis`. | Melhorar a clareza e a qualidade textual da interface. |

### 8.2. Critérios para validação das melhorias

A validação das melhorias deve considerar os seguintes critérios:

- A velocidade da execução EXEC-104 deve utilizar a mesma unidade em todas as telas.
- Os valores de velocidade devem ser consistentes entre o painel principal e a comparação.
- A interface deve diferenciar condições confirmadas de condições não confirmadas.
- A mensagem de ausência de resultados deve apresentar a palavra `disponíveis` corretamente.
- As alterações não devem prejudicar a organização visual ou a compreensão das demais informações.

### 8.3. Registro de reinspeção

A reinspeção deve verificar se as alterações propostas resolvem os problemas identificados e se não introduzem novas inconsistências.

| ID | Item a verificar | Critério de aprovação |
|---|---|---|
| V01 | Unidade de velocidade da execução EXEC-104. | A unidade deve ser padronizada em P01, P03 e tela 04, com valores correspondentes. |
| V02 | Mensagens sobre as condições de treinamento. | As mensagens devem distinguir ausência de diferenças de condições não confirmadas. |
| V03 | Mensagem do estado vazio. | A palavra deve estar corrigida para `disponíveis`. |

A reinspeção deve ser registrada com a identificação da tela, a evidência visual correspondente e o resultado da verificação de cada problema.

## 9. Conclusão

A avaliação heurística permitiu identificar problemas relacionados à consistência das métricas, à clareza das informações sobre as condições de treinamento e à comunicação textual da interface.

Os três problemas encontrados foram classificados conforme sua severidade, permitindo estabelecer uma ordem de prioridade para as melhorias.

A análise também permitiu observar aspectos positivos da interface, como a apresentação de estados de confirmação, a organização das opções de consulta e a existência de telas destinadas à identificação de erros.

A aplicação das heurísticas de Nielsen contribui para orientar a evolução da interface, tornando as informações mais claras, consistentes e compreensíveis para os usuários.

## 10. Checklist da entrega

- [x] Definir as dez heurísticas utilizadas na avaliação.
- [x] Delimitar o escopo da inspeção.
- [x] Identificar os elementos e estados relevantes da interface.
- [x] Definir a escala de severidade.
- [x] Registrar os problemas identificados.
- [x] Relacionar os problemas às heurísticas correspondentes.
- [x] Consolidar os problemas encontrados pela equipe.
- [x] Definir recomendações de melhoria.
- [x] Organizar os critérios de validação das melhorias.
- [ ] Inserir as evidências visuais dos problemas identificados.
- [ ] Confirmar e registrar as avaliações individuais realizadas por cada integrante.
- [ ] Registrar a reinspeção após a implementação das correções.

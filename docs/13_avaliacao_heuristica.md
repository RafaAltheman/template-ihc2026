# Entrega 13 — Avaliação de IHC por inspeção heurística

**Data:** 16/11/2026  
**Status:** em andamento
**Responsabilidade:** 1 avaliação completa por integrante, sobre todas as telas e estados relevantes do projeto.

## Objetivo da atividade

Realizar uma avaliação de usabilidade do protótipo por meio de inspeção heurística, utilizando as dez heurísticas de Nielsen como referência para identificar problemas na interface.

A avaliação busca verificar se a interface apresenta informações de maneira clara, consistente e compreensível, considerando as atividades realizadas pelos usuários no sistema. Também procura identificar boas práticas presentes no protótipo e registrar problemas que possam prejudicar a interpretação dos dados, a comparação das execuções e a utilização das funcionalidades.

A inspeção foi realizada sobre o protótipo da Entrega 11, considerando as telas e os estados especiais disponíveis. Os problemas encontrados foram registrados com identificação, heurística relacionada, evidência, severidade e recomendação de melhoria.

## 1. Heurísticas adotadas

A avaliação utiliza as dez heurísticas de usabilidade de Jakob Nielsen:

1. **Visibilidade do status do sistema:** o sistema deve manter o usuário informado sobre o que está acontecendo, fornecendo feedback adequado e em tempo razoável.

2. **Compatibilidade entre o sistema e o mundo real:** o sistema deve utilizar linguagem, conceitos e informações familiares ao usuário, seguindo convenções do mundo real e apresentando os dados de maneira lógica.

3. **Controle e liberdade do usuário:** o usuário deve ter liberdade para desfazer ações indesejadas e sair de situações inesperadas sem dificuldades.

4. **Consistência e padrões:** elementos, informações e ações semelhantes devem seguir os mesmos padrões em toda a interface, evitando que o usuário precise entender diferentes convenções para situações equivalentes.

5. **Prevenção de erros:** a interface deve evitar situações que possam levar o usuário a cometer erros, antecipando problemas e apresentando informações que ajudem a tomar decisões corretas.

6. **Reconhecimento em vez de memorização:** o sistema deve apresentar informações e opções de maneira visível, reduzindo a necessidade de o usuário memorizar dados, caminhos ou instruções.

7. **Flexibilidade e eficiência de uso:** a interface deve permitir que usuários com diferentes níveis de experiência realizem suas atividades de maneira eficiente.

8. **Estética e design minimalista:** a interface deve apresentar apenas informações relevantes para a atividade, evitando elementos desnecessários e excesso de informações.

9. **Reconhecer, diagnosticar e recuperar erros:** mensagens de erro devem ser claras, indicar o problema e orientar o usuário sobre como recuperar a situação.

10. **Ajuda e documentação:** quando necessário, o sistema deve oferecer informações que auxiliem o usuário a compreender as funcionalidades e realizar suas atividades.

## Cobertura especial para interfaces administrativas e analíticas

Por se tratar de uma interface voltada à visualização e comparação de dados de execuções, a inspeção também considera aspectos específicos desse contexto:

- Clareza na apresentação de métricas e indicadores.
- Consistência das unidades de medida.
- Facilidade para comparar diferentes execuções.
- Identificação das condições de treinamento.
- Clareza sobre a disponibilidade ou ausência de dados.
- Apresentação de mensagens de erro e estados vazios.
- Compreensão das informações necessárias para interpretar os resultados.

Esses aspectos foram relacionados às heurísticas de Nielsen durante a análise, principalmente nos pontos em que a apresentação dos dados pode influenciar a interpretação dos resultados.

## 2. Escopo da inspeção

| Item | Definição |
|---|---|
| **Projeto** | Projeto do Grupo 27 |
| **Versão avaliada** | Protótipo da Entrega 11 — Figma IHC |
| **Link do protótipo** | [Acessar protótipo no Figma](https://www.figma.com/proto/qHpoJxQF4Sthdy99w7Scul/IHC?node-id=32-2023&t=MJOhlZgAfoJJp8Dt-1&scaling=min-zoom&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=32%3A2023) |
| **Página e ponto inicial** | Página 0:1, com início no nó 32:2023 |
| **Data da inspeção registrada** | 16/11/2026 |
| **Telas examinadas** | P01, P03, P06, P09, P10 e telas 02, 03, 04, 05, 06, 07, 09, 15, 16, 17, 18, 21, 29, 33, 37, 42, 43 e 45 |
| **Estados especiais examinados** | Estado vazio, erro, filtro sem resultados, confirmação e comparação com condições não confirmadas |
| **Avaliadores** | Manuella Filipe Peres, Letizia Lowatzki Baptistella e Rafaela Altheman de Campos |
| **Tipo de inspeção registrada** | Inspeção estática do protótipo pela equipe |

### Estados examinados

| Estado | Telas/identificação | Descrição |
|---|---|---|
| **Vazio** | P10 e tela 42 | Situação em que não existem resultados disponíveis para apresentar. |
| **Erro** | Telas 33 e 45 | Situações relacionadas à apresentação e recuperação de erros. |
| **Filtro sem resultados** | P09 e tela 29 | Situação em que a busca ou o filtro não retorna resultados. |
| **Confirmação** | P06 e telas 07, 09 e 21 | Situações em que o sistema apresenta ou permite conferir registros e confirmações. |
| **Comparação com condições não confirmadas** | Telas 04 e 05 | Situação em que as condições de treinamento não estão confirmadas para a comparação. |

**Estados não avaliados:** estados de carregamento e situações relacionadas a permissões de acesso não foram contemplados na inspeção registrada. Portanto, não foram atribuídos achados ou conclusões sobre esses estados.

### Limitações do escopo

A avaliação foi realizada por inspeção estática do protótipo. Dessa forma, as observações correspondem aos elementos visuais e às informações disponíveis nas telas examinadas.

A inspeção não representa um teste completo de todas as interações possíveis, nem comprova o comportamento de funcionalidades que dependam de execução real, carregamento de dados ou permissões de acesso.

## 3. Procedimento individual

A avaliação heurística considera a análise da interface a partir das dez heurísticas de Nielsen. Durante a inspeção, devem ser observadas as telas, os estados e os fluxos relevantes do sistema, identificando situações em que a interface possa dificultar a compreensão ou a realização das atividades.

O procedimento utilizado como referência para a inspeção foi:

1. Acessar o protótipo da Entrega 11 no Figma.
2. Percorrer as telas e os fluxos disponíveis.
3. Observar a apresentação das informações, os elementos visuais e as mensagens do sistema.
4. Verificar a interface considerando cada uma das dez heurísticas.
5. Identificar possíveis violações e registrar as telas em que aparecem.
6. Atribuir um nível de severidade aos problemas identificados.
7. Registrar recomendações para corrigir os problemas encontrados.
8. Identificar exemplos de boas práticas nas heurísticas em que não foi confirmada nenhuma violação.

O formulário disponível registra os resultados de uma inspeção estática conjunta da equipe. Assim, os achados apresentados nesta entrega são tratados como resultados consolidados, sem atribuição individual não comprovada.

### Escala de severidade (0–4)

A severidade é utilizada para indicar o impacto do problema identificado na experiência do usuário.

| Severidade | Classificação | Descrição |
|---:|---|---|
| **0** | Sem problema | Não foi identificada uma violação que precise de correção. |
| **1** | Cosmética | Problema visual ou textual de baixo impacto, que não compromete a realização da atividade. |
| **2** | Pequena | Problema que pode causar alguma dificuldade, mas não compromete significativamente a utilização do sistema. |
| **3** | Grave | Problema que pode prejudicar a compreensão das informações ou levar o usuário a realizar uma interpretação ou ação inadequada. |
| **4** | Catastrófica/imperativa | Problema de impacto muito alto, que pode comprometer significativamente a interpretação dos dados ou a tomada de decisão e exige correção prioritária. |

---

## Avaliador A01 — Manuella Filipe Peres

### 4. Matriz de cobertura das 10 heurísticas

A matriz abaixo apresenta a cobertura registrada na inspeção estática da equipe. Os resultados não representam uma atribuição individual independente dos achados.

| Heurística | Telas/fluxos examinados | Houve violação? | IDs dos achados | Exemplo de boa prática se não violada |
|---|---|---|---|---|
| **H1 — Visibilidade do status do sistema** | P06 — Confirmar registro; tela 07 — Conferir hipótese registrada; tela 09 — Conferir avaliação registrada; tela 21 — Conferir registro. | Não | — | A interface apresenta telas específicas para conferir registros e confirmações, permitindo que o usuário consulte informações relacionadas às ações realizadas. |
| **H2 — Compatibilidade entre o sistema e o mundo real** | P01 — Painel geral; P03 — Comparação de execuções; tela 04 — Comparar métricas e parâmetros. | Sim | V01 | — |
| **H3 — Controle e liberdade do usuário** | Tela 15 — Apresentar indicadores; tela 43 — Observar evidência da execução; tela 45 — Recuperar erro de registro. | Não | — | A existência de uma tela voltada à recuperação de erro de registro representa um ponto positivo para orientar o usuário diante de uma situação inesperada. |
| **H4 — Consistência e padrões** | P01 — Painel geral; P03 — Comparação de execuções; tela 04 — Comparar métricas e parâmetros; tela 05 — Verificar comparabilidade. | Sim | V01, V02 | — |
| **H5 — Prevenção de erros** | P03 — Comparação; tela 05 — Verificar comparabilidade; tela 06 — Registrar hipótese e ressalvas. | Sim | V02 | — |
| **H6 — Reconhecimento em vez de memorização** | Tela 02 — Localizar treinamento; tela 03 — Selecionar execuções; tela 43 — Observar evidência. | Não | — | A apresentação das opções de localização e seleção de execuções auxilia o usuário a identificar os elementos necessários sem depender exclusivamente da memorização de caminhos. |
| **H7 — Flexibilidade e eficiência de uso** | Tela 02 — Localizar treinamento; tela 04 — Comparar métricas e parâmetros; telas 15 a 18 — Apresentar indicadores. | Não | — | A organização das telas de indicadores e comparação permite consultar diferentes informações relacionadas às execuções. |
| **H8 — Estética e design minimalista** | P01 — Painel geral; P03 — Comparação; P10 — Painel sem dados do período. | Sim | V03 | — |
| **H9 — Reconhecer, diagnosticar e recuperar erros** | P09 — Busca sem resultados; tela 29 — Busca sem resultados; tela 33 — Corrigir ou tentar novamente; tela 45 — Recuperar erro de registro. | Não | — | A existência de estados específicos para busca sem resultados e recuperação de erros auxilia na compreensão de situações em que a operação não apresenta o resultado esperado. |
| **H10 — Ajuda e documentação** | Tela 02 — Localizar treinamento; tela 05 — Verificar comparabilidade; tela 37 — Investigar dado não registrado. | Não | — | A apresentação de informações relacionadas à localização de treinamentos e à investigação de dados não registrados auxilia na compreensão das atividades disponíveis. |

### 5. Declaração de violações

Os achados registrados na inspeção conjunta estão descritos integralmente na seção **7. Consolidação da equipe**. Eles são apresentados aqui como referência da cobertura, sem afirmar que foram identificados individualmente por esta avaliadora.

| ID | Heurística | Tela/estado | Problema observado | Evidência | Severidade | Justificativa da severidade | Recomendação |
|---|---|---|---|---|---:|---|---|
| V01 | H2 e H4 | P01, P03 e tela 04 | Inconsistência na unidade de velocidade da execução EXEC-104. | P01 apresenta 0,32 m/s, enquanto P03 e tela 04 apresentam 0.32 cm/s. | 4 | A diferença de unidade altera significativamente a interpretação da medida. | Padronizar a unidade e verificar os valores apresentados. |
| V02 | H4 e H5 | P03, tela 04 e tela 05 | Ambiguidade na indicação das condições de treinamento. | P03 apresenta "Diferença de configuração: Nenhuma", enquanto as telas 04 e 05 indicam condições não confirmadas. | 3 | A informação pode levar o usuário a interpretar incorretamente a comparabilidade das execuções. | Diferenciar ausência de diferenças identificadas de condições não verificadas. |
| V03 | H8 | P10 | Erro de digitação na mensagem do estado vazio. | A mensagem apresenta "dsponíveis" em vez de "disponíveis". | 1 | O problema é textual e não impede a compreensão geral da mensagem. | Corrigir o erro de digitação. |

### 6. Boas práticas — heurísticas não violadas (atividade didática)

| Heurística sem violação | Exemplo no sistema | Evidência | Por que atende |
|---|---|---|---|
| **H1 — Visibilidade do status do sistema** | Telas de conferência de registros e confirmações. | P06 e telas 07, 09 e 21. | A interface apresenta espaços específicos para consultar informações relacionadas aos registros. |
| **H3 — Controle e liberdade do usuário** | Tela destinada à recuperação de erro de registro. | Tela 45. | A existência de uma situação de recuperação demonstra preocupação em orientar o usuário diante de um erro. |
| **H6 — Reconhecimento em vez de memorização** | Localização de treinamento e seleção de execuções. | Telas 02 e 03. | As telas apresentam informações e opções que auxiliam o usuário a reconhecer os elementos necessários. |
| **H7 — Flexibilidade e eficiência de uso** | Organização de métricas e indicadores. | Tela 04 e telas 15 a 18. | A interface reúne informações relacionadas à análise das execuções. |
| **H9 — Reconhecer, diagnosticar e recuperar erros** | Estados de busca sem resultados e recuperação de erro. | P09, tela 29, tela 33 e tela 45. | A existência desses estados auxilia na identificação de situações em que o sistema não apresenta o resultado esperado. |
| **H10 — Ajuda e documentação** | Informações relacionadas à localização de treinamentos, comparabilidade e dados não registrados. | Telas 02, 05 e 37. | As telas apresentam informações que ajudam a compreender as atividades e situações do sistema. |

---

## Avaliador A02 — Letizia Lowatzki Baptistella

### 4. Matriz de cobertura das 10 heurísticas

A matriz abaixo apresenta a cobertura registrada na inspeção estática da equipe. Os resultados não representam uma atribuição individual independente dos achados.

| Heurística | Telas/fluxos examinados | Houve violação? | IDs dos achados | Exemplo de boa prática se não violada |
|---|---|---|---|---|
| **H1 — Visibilidade do status do sistema** | P06 — Confirmar registro; tela 07 — Conferir hipótese registrada; tela 09 — Conferir avaliação registrada; tela 21 — Conferir registro. | Não | — | A interface apresenta telas específicas para conferir registros e confirmações, permitindo que o usuário consulte informações relacionadas às ações realizadas. |
| **H2 — Compatibilidade entre o sistema e o mundo real** | P01 — Painel geral; P03 — Comparação de execuções; tela 04 — Comparar métricas e parâmetros. | Sim | V01 | — |
| **H3 — Controle e liberdade do usuário** | Tela 15 — Apresentar indicadores; tela 43 — Observar evidência da execução; tela 45 — Recuperar erro de registro. | Não | — | A existência de uma tela voltada à recuperação de erro de registro representa um ponto positivo para orientar o usuário diante de uma situação inesperada. |
| **H4 — Consistência e padrões** | P01 — Painel geral; P03 — Comparação de execuções; tela 04 — Comparar métricas e parâmetros; tela 05 — Verificar comparabilidade. | Sim | V01, V02 | — |
| **H5 — Prevenção de erros** | P03 — Comparação; tela 05 — Verificar comparabilidade; tela 06 — Registrar hipótese e ressalvas. | Sim | V02 | — |
| **H6 — Reconhecimento em vez de memorização** | Tela 02 — Localizar treinamento; tela 03 — Selecionar execuções; tela 43 — Observar evidência. | Não | — | A apresentação das opções de localização e seleção de execuções auxilia o usuário a identificar os elementos necessários sem depender exclusivamente da memorização de caminhos. |
| **H7 — Flexibilidade e eficiência de uso** | Tela 02 — Localizar treinamento; tela 04 — Comparar métricas e parâmetros; telas 15 a 18 — Apresentar indicadores. | Não | — | A organização das telas de indicadores e comparação permite consultar diferentes informações relacionadas às execuções. |
| **H8 — Estética e design minimalista** | P01 — Painel geral; P03 — Comparação; P10 — Painel sem dados do período. | Sim | V03 | — |
| **H9 — Reconhecer, diagnosticar e recuperar erros** | P09 — Busca sem resultados; tela 29 — Busca sem resultados; tela 33 — Corrigir ou tentar novamente; tela 45 — Recuperar erro de registro. | Não | — | A existência de estados específicos para busca sem resultados e recuperação de erros auxilia na compreensão de situações em que a operação não apresenta o resultado esperado. |
| **H10 — Ajuda e documentação** | Tela 02 — Localizar treinamento; tela 05 — Verificar comparabilidade; tela 37 — Investigar dado não registrado. | Não | — | A apresentação de informações relacionadas à localização de treinamentos e à investigação de dados não registrados auxilia na compreensão das atividades disponíveis. |

### 5. Declaração de violações

Os achados registrados na inspeção conjunta estão descritos integralmente na seção **7. Consolidação da equipe**. Eles são apresentados aqui como referência da cobertura, sem afirmar que foram identificados individualmente por esta avaliadora.

| ID | Heurística | Tela/estado | Problema observado | Evidência | Severidade | Justificativa da severidade | Recomendação |
|---|---|---|---|---|---:|---|---|
| V01 | H2 e H4 | P01, P03 e tela 04 | Inconsistência na unidade de velocidade da execução EXEC-104. | P01 apresenta 0,32 m/s, enquanto P03 e tela 04 apresentam 0.32 cm/s. | 4 | A diferença de unidade altera significativamente a interpretação da medida. | Padronizar a unidade e verificar os valores apresentados. |
| V02 | H4 e H5 | P03, tela 04 e tela 05 | Ambiguidade na indicação das condições de treinamento. | P03 apresenta "Diferença de configuração: Nenhuma", enquanto as telas 04 e 05 indicam condições não confirmadas. | 3 | A informação pode levar o usuário a interpretar incorretamente a comparabilidade das execuções. | Diferenciar ausência de diferenças identificadas de condições não verificadas. |
| V03 | H8 | P10 | Erro de digitação na mensagem do estado vazio. | A mensagem apresenta "dsponíveis" em vez de "disponíveis". | 1 | O problema é textual e não impede a compreensão geral da mensagem. | Corrigir o erro de digitação. |

### 6. Boas práticas — heurísticas não violadas (atividade didática)

| Heurística sem violação | Exemplo no sistema | Evidência | Por que atende |
|---|---|---|---|
| **H1 — Visibilidade do status do sistema** | Telas de conferência de registros e confirmações. | P06 e telas 07, 09 e 21. | A interface apresenta espaços específicos para consultar informações relacionadas aos registros. |
| **H3 — Controle e liberdade do usuário** | Tela destinada à recuperação de erro de registro. | Tela 45. | A existência de uma situação de recuperação demonstra preocupação em orientar o usuário diante de um erro. |
| **H6 — Reconhecimento em vez de memorização** | Localização de treinamento e seleção de execuções. | Telas 02 e 03. | As telas apresentam informações e opções que auxiliam o usuário a reconhecer os elementos necessários. |
| **H7 — Flexibilidade e eficiência de uso** | Organização de métricas e indicadores. | Tela 04 e telas 15 a 18. | A interface reúne informações relacionadas à análise das execuções. |
| **H9 — Reconhecer, diagnosticar e recuperar erros** | Estados de busca sem resultados e recuperação de erro. | P09, tela 29, tela 33 e tela 45. | A existência desses estados auxilia na identificação de situações em que o sistema não apresenta o resultado esperado. |
| **H10 — Ajuda e documentação** | Informações relacionadas à localização de treinamentos, comparabilidade e dados não registrados. | Telas 02, 05 e 37. | As telas apresentam informações que ajudam a compreender as atividades e situações do sistema. |

---

## Avaliador A03 — Rafaela Altheman de Campos

### 4. Matriz de cobertura das 10 heurísticas

A matriz abaixo apresenta a cobertura registrada na inspeção estática da equipe. Os resultados não representam uma atribuição individual independente dos achados.

| Heurística | Telas/fluxos examinados | Houve violação? | IDs dos achados | Exemplo de boa prática se não violada |
|---|---|---|---|---|
| **H1 — Visibilidade do status do sistema** | P06 — Confirmar registro; tela 07 — Conferir hipótese registrada; tela 09 — Conferir avaliação registrada; tela 21 — Conferir registro. | Não | — | A interface apresenta telas específicas para conferir registros e confirmações, permitindo que o usuário consulte informações relacionadas às ações realizadas. |
| **H2 — Compatibilidade entre o sistema e o mundo real** | P01 — Painel geral; P03 — Comparação de execuções; tela 04 — Comparar métricas e parâmetros. | Sim | V01 | — |
| **H3 — Controle e liberdade do usuário** | Tela 15 — Apresentar indicadores; tela 43 — Observar evidência da execução; tela 45 — Recuperar erro de registro. | Não | — | A existência de uma tela voltada à recuperação de erro de registro representa um ponto positivo para orientar o usuário diante de uma situação inesperada. |
| **H4 — Consistência e padrões** | P01 — Painel geral; P03 — Comparação de execuções; tela 04 — Comparar métricas e parâmetros; tela 05 — Verificar comparabilidade. | Sim | V01, V02 | — |
| **H5 — Prevenção de erros** | P03 — Comparação; tela 05 — Verificar comparabilidade; tela 06 — Registrar hipótese e ressalvas. | Sim | V02 | — |
| **H6 — Reconhecimento em vez de memorização** | Tela 02 — Localizar treinamento; tela 03 — Selecionar execuções; tela 43 — Observar evidência. | Não | — | A apresentação das opções de localização e seleção de execuções auxilia o usuário a identificar os elementos necessários sem depender exclusivamente da memorização de caminhos. |
| **H7 — Flexibilidade e eficiência de uso** | Tela 02 — Localizar treinamento; tela 04 — Comparar métricas e parâmetros; telas 15 a 18 — Apresentar indicadores. | Não | — | A organização das telas de indicadores e comparação permite consultar diferentes informações relacionadas às execuções. |
| **H8 — Estética e design minimalista** | P01 — Painel geral; P03 — Comparação; P10 — Painel sem dados do período. | Sim | V03 | — |
| **H9 — Reconhecer, diagnosticar e recuperar erros** | P09 — Busca sem resultados; tela 29 — Busca sem resultados; tela 33 — Corrigir ou tentar novamente; tela 45 — Recuperar erro de registro. | Não | — | A existência de estados específicos para busca sem resultados e recuperação de erros auxilia na compreensão de situações em que a operação não apresenta o resultado esperado. |
| **H10 — Ajuda e documentação** | Tela 02 — Localizar treinamento; tela 05 — Verificar comparabilidade; tela 37 — Investigar dado não registrado. | Não | — | A apresentação de informações relacionadas à localização de treinamentos e à investigação de dados não registrados auxilia na compreensão das atividades disponíveis. |

### 5. Declaração de violações

Os achados registrados na inspeção conjunta estão descritos integralmente na seção **7. Consolidação da equipe**. Eles são apresentados aqui como referência da cobertura, sem afirmar que foram identificados individualmente por esta avaliadora.

| ID | Heurística | Tela/estado | Problema observado | Evidência | Severidade | Justificativa da severidade | Recomendação |
|---|---|---|---|---|---:|---|---|
| V01 | H2 e H4 | P01, P03 e tela 04 | Inconsistência na unidade de velocidade da execução EXEC-104. | P01 apresenta 0,32 m/s, enquanto P03 e tela 04 apresentam 0.32 cm/s. | 4 | A diferença de unidade altera significativamente a interpretação da medida. | Padronizar a unidade e verificar os valores apresentados. |
| V02 | H4 e H5 | P03, tela 04 e tela 05 | Ambiguidade na indicação das condições de treinamento. | P03 apresenta "Diferença de configuração: Nenhuma", enquanto as telas 04 e 05 indicam condições não confirmadas. | 3 | A informação pode levar o usuário a interpretar incorretamente a comparabilidade das execuções. | Diferenciar ausência de diferenças identificadas de condições não verificadas. |
| V03 | H8 | P10 | Erro de digitação na mensagem do estado vazio. | A mensagem apresenta "dsponíveis" em vez de "disponíveis". | 1 | O problema é textual e não impede a compreensão geral da mensagem. | Corrigir o erro de digitação. |

### 6. Boas práticas — heurísticas não violadas (atividade didática)

| Heurística sem violação | Exemplo no sistema | Evidência | Por que atende |
|---|---|---|---|
| **H1 — Visibilidade do status do sistema** | Telas de conferência de registros e confirmações. | P06 e telas 07, 09 e 21. | A interface apresenta espaços específicos para consultar informações relacionadas aos registros. |
| **H3 — Controle e liberdade do usuário** | Tela destinada à recuperação de erro de registro. | Tela 45. | A existência de uma situação de recuperação demonstra preocupação em orientar o usuário diante de um erro. |
| **H6 — Reconhecimento em vez de memorização** | Localização de treinamento e seleção de execuções. | Telas 02 e 03. | As telas apresentam informações e opções que auxiliam o usuário a reconhecer os elementos necessários. |
| **H7 — Flexibilidade e eficiência de uso** | Organização de métricas e indicadores. | Tela 04 e telas 15 a 18. | A interface reúne informações relacionadas à análise das execuções. |
| **H9 — Reconhecer, diagnosticar e recuperar erros** | Estados de busca sem resultados e recuperação de erro. | P09, tela 29, tela 33 e tela 45. | A existência desses estados auxilia na identificação de situações em que o sistema não apresenta o resultado esperado. |
| **H10 — Ajuda e documentação** | Informações relacionadas à localização de treinamentos, comparabilidade e dados não registrados. | Telas 02, 05 e 37. | As telas apresentam informações que ajudam a compreender as atividades e situações do sistema. |

---

## 7. Consolidação da equipe

A consolidação reúne os problemas identificados na inspeção estática do protótipo. Os achados foram organizados por identificação, heurística violada, tela, consequência, evidência, severidade e recomendação.

### 7.1. Quadro consolidado dos achados

| ID | Heurística | Tela/estado | Problema observado | Consequência | Severidade |
|---|---|---|---|---|---:|
| **V01** | H2 e H4 | P01, P03 e tela 04 | Inconsistência na unidade de velocidade da execução EXEC-104. | Pode causar interpretação incorreta da velocidade e comprometer a comparação das execuções. | **4** |
| **V02** | H4 e H5 | P03, tela 04 e tela 05 | Ambiguidade na indicação das condições de treinamento. | Pode levar o usuário a considerar execuções comparáveis sem confirmação suficiente das condições. | **3** |
| **V03** | H8 | P10 | Erro de digitação na mensagem do estado vazio. | Prejudica o acabamento textual da interface, sem impedir a compreensão geral. | **1** |

### 7.2. Detalhamento dos achados

#### V01 — Inconsistência na unidade de velocidade da execução EXEC-104

| Campo | Descrição |
|---|---|
| **ID** | V01 |
| **Heurísticas violadas** | H2 — Compatibilidade entre o sistema e o mundo real; H4 — Consistência e padrões |
| **Tela/estado** | P01 — Painel geral; P03 — Comparação de execuções; tela 04 — Comparar métricas e parâmetros |
| **Ação/condição** | Consultar a velocidade da execução EXEC-104 e comparar a informação apresentada em diferentes telas. |
| **Problema observado** | A velocidade da execução EXEC-104 é apresentada com unidades diferentes em telas distintas. No painel principal (P01), o valor aparece como **0,32 m/s**, enquanto na tela de comparação (P03) e na tela 04 aparece como **0.32 cm/s**. Além da diferença na unidade de medida, existe uma diferença na formatação decimal. Isso pode levar o usuário a interpretar incorretamente a velocidade da execução e comprometer a comparação dos resultados. |
| **Consequência** | A inconsistência pode gerar dúvidas sobre qual valor está correto e prejudicar a interpretação das métricas utilizadas para analisar o desempenho das execuções. |
| **Evidência** | P01 apresenta "0,32 m/s", enquanto P03 e tela 04 apresentam "0.32 cm/s" para a velocidade de EXEC-104. |
| **Severidade** | **4 — Catastrófica/imperativa** |
| **Justificativa da severidade** | A diferença entre metros por segundo e centímetros por segundo altera a interpretação da medida por um fator de 100. Por se tratar de uma métrica quantitativa utilizada na análise das execuções, a inconsistência pode comprometer conclusões técnicas e decisões baseadas nos resultados. |
| **Recomendação** | Padronizar a unidade de velocidade em todas as telas do sistema, utilizando a mesma unidade de medida e o mesmo formato decimal. Também é necessário verificar se os valores apresentados correspondem corretamente aos dados originais da execução. |

**Evidências visuais:**

<!-- INSERIR PRINT V01-01: P01 — Painel geral mostrando EXEC-104 com velocidade de 0,32 m/s. -->

<!-- INSERIR PRINT V01-02: P03 — Comparação mostrando EXEC-104 com velocidade de 0.32 cm/s. -->

<!-- INSERIR PRINT V01-03: Tela 04 — Comparação de métricas mostrando EXEC-104 com velocidade de 0.32 cm/s. -->

#### V02 — Ambiguidade na indicação das condições de treinamento

| Campo | Descrição |
|---|---|
| **ID** | V02 |
| **Heurísticas violadas** | H4 — Consistência e padrões; H5 — Prevenção de erros |
| **Tela/estado** | P03 — Comparação de execuções; tela 04 — Comparar métricas e parâmetros; tela 05 — Verificar comparabilidade |
| **Ação/condição** | Verificar se duas execuções podem ser comparadas de maneira confiável, considerando suas condições de treinamento. |
| **Problema observado** | As telas apresentam informações que podem gerar interpretações contraditórias sobre as condições de treinamento das execuções. Na tela P03, aparece a mensagem **"Diferença de configuração: Nenhuma"**. Entretanto, na tela 04, aparece a indicação **"Condições de treinamento: não confirmadas"**, enquanto na tela 05 é apresentada a mensagem **"Condições não confirmadas"**. A ausência de confirmação das condições não significa necessariamente que não existam diferenças entre as configurações. Dessa forma, a apresentação atual pode levar o usuário a interpretar que as execuções possuem condições equivalentes, mesmo quando essa informação não foi confirmada. |
| **Consequência** | O usuário pode considerar duas execuções plenamente comparáveis sem ter informações suficientes para confirmar que as condições de treinamento são equivalentes. Isso pode prejudicar a interpretação dos resultados. |
| **Evidência** | P03 apresenta "Diferença de configuração: Nenhuma". A tela 04 apresenta "Condições de treinamento: não confirmadas". A tela 05 apresenta "Condições não confirmadas". |
| **Severidade** | **3 — Grave** |
| **Justificativa da severidade** | A ambiguidade pode prejudicar a interpretação dos resultados e levar o usuário a realizar comparações sem ter certeza de que as condições de treinamento são equivalentes. Entretanto, o problema não impede diretamente a utilização do sistema. |
| **Recomendação** | Diferenciar claramente a ausência de diferenças identificadas da falta de confirmação das condições de treinamento. Quando não houver informações suficientes para confirmar a equivalência entre duas execuções, o sistema deve informar que as condições não foram verificadas, evitando apresentar uma mensagem que possa sugerir que não existem diferenças. |

**Evidências visuais:**

<!-- INSERIR PRINT V02-01: P03 — Comparação mostrando a mensagem "Diferença de configuração: Nenhuma". -->

<!-- INSERIR PRINT V02-02: Tela 04 — Comparação de métricas mostrando "Condições de treinamento: não confirmadas". -->

<!-- INSERIR PRINT V02-03: Tela 05 — Verificação de comparabilidade mostrando "Condições não confirmadas". -->

#### V03 — Erro de digitação na mensagem do estado vazio

| Campo | Descrição |
|---|---|
| **ID** | V03 |
| **Heurística violada** | H8 — Estética e design minimalista |
| **Tela/estado** | P10 — Painel sem dados do período |
| **Ação/condição** | Consultar um período em que não existem resultados disponíveis. |
| **Problema observado** | Na tela P10, apresentada quando não existem resultados disponíveis para o período escolhido, a mensagem exibida contém um erro de digitação: **"Não há resultados dsponíveis no período escolhido"**. A palavra "disponíveis" está escrita incorretamente, o que prejudica o acabamento visual e a qualidade textual da interface. |
| **Consequência** | O erro de escrita reduz a qualidade da apresentação e pode transmitir uma impressão de falta de revisão do conteúdo textual. |
| **Evidência** | A mensagem apresentada na tela P10 contém a palavra "dsponíveis". |
| **Severidade** | **1 — Cosmética** |
| **Justificativa da severidade** | O problema não compromete a funcionalidade do sistema nem impede que o usuário compreenda a mensagem. Entretanto, o erro de digitação prejudica a apresentação e o profissionalismo da interface. |
| **Recomendação** | Corrigir a palavra "dsponíveis" para "disponíveis", mantendo a mensagem como **"Não há resultados disponíveis no período escolhido"**. Também é recomendável revisar os textos da interface para evitar outros erros de digitação. |

**Evidência visual:**

<!-- INSERIR PRINT V03-01: P10 — Painel sem dados mostrando "Não há resultados dsponíveis no período escolhido". -->

### 7.3. Distribuição dos achados por heurística

| Heurística | Quantidade de achados | IDs |
|---|---:|---|
| H1 — Visibilidade do status do sistema | 0 | — |
| H2 — Compatibilidade entre o sistema e o mundo real | 1 | V01 |
| H3 — Controle e liberdade do usuário | 0 | — |
| H4 — Consistência e padrões | 2 | V01, V02 |
| H5 — Prevenção de erros | 1 | V02 |
| H6 — Reconhecimento em vez de memorização | 0 | — |
| H7 — Flexibilidade e eficiência de uso | 0 | — |
| H8 — Estética e design minimalista | 1 | V03 |
| H9 — Reconhecer, diagnosticar e recuperar erros | 0 | — |
| H10 — Ajuda e documentação | 0 | — |

**Observação:** a quantidade de ocorrências por heurística não corresponde necessariamente à quantidade total de problemas, pois um mesmo achado pode violar mais de uma heurística.

### 7.4. Limitações identificadas na inspeção

A inspeção foi realizada sobre os elementos disponíveis no protótipo. Dessa forma, não foi possível avaliar estados de carregamento e situações relacionadas a permissões de acesso.

Também é importante considerar que a ausência de violações registradas em uma heurística não significa que todos os caminhos e interações do sistema tenham sido testados. A avaliação representa os elementos examinados no escopo definido.

---

## 8. Síntese e plano de melhoria

A avaliação heurística identificou três problemas no protótipo, relacionados à consistência das informações, à interpretação das condições de treinamento e à qualidade textual de uma mensagem de estado vazio.

O achado de maior severidade é o V01, relacionado à apresentação de unidades diferentes para a velocidade da execução EXEC-104. Esse problema pode comprometer a interpretação de uma métrica importante para a análise dos resultados.

O V02 também merece atenção, pois a apresentação de mensagens diferentes sobre a confirmação das condições de treinamento pode levar o usuário a interpretar incorretamente a comparabilidade entre execuções.

Por fim, o V03 apresenta menor severidade, mas deve ser corrigido para melhorar a qualidade textual e o acabamento da interface.

### 8.1. Plano de melhoria

| Prioridade | ID | Problema | Ação de melhoria | Resultado esperado |
|---|---|---|---|---|
| **1 — Alta** | V01 | Inconsistência na unidade de velocidade da execução EXEC-104. | Verificar o valor correto e padronizar a unidade de velocidade em todas as telas. | Apresentar a métrica de maneira consistente, evitando interpretações incorretas. |
| **2 — Alta** | V02 | Ambiguidade na indicação das condições de treinamento. | Diferenciar ausência de diferenças identificadas de condições não confirmadas. | Permitir que o usuário compreenda quando uma comparação está efetivamente validada. |
| **3 — Baixa** | V03 | Erro de digitação na mensagem do estado vazio. | Corrigir "dsponíveis" para "disponíveis". | Melhorar a clareza e a qualidade textual da interface. |

### 8.2. Recomendações gerais

Além das correções específicas, recomenda-se:

- Manter um padrão único para a apresentação de unidades de medida.
- Verificar a consistência das informações quantitativas entre o painel e as telas de comparação.
- Utilizar mensagens diferentes para indicar ausência de diferenças e falta de confirmação de informações.
- Revisar os textos apresentados nos estados vazios e nas mensagens do sistema.
- Realizar uma nova inspeção após a implementação das melhorias.
- Verificar os estados de carregamento e permissões em uma avaliação posterior, pois eles não fizeram parte do escopo examinado.

### 8.3. Verificação após as melhorias

Após a implementação das correções, recomenda-se repetir a inspeção nas telas relacionadas aos achados identificados.

| ID | Verificação necessária | Critério para considerar resolvido |
|---|---|---|
| V01 | Conferir a velocidade da execução EXEC-104 em P01, P03 e tela 04. | A mesma unidade e convenção de apresentação devem ser utilizadas em todas as telas, com os valores devidamente conferidos. |
| V02 | Conferir as mensagens sobre configuração e condições de treinamento em P03, tela 04 e tela 05. | As mensagens devem distinguir claramente informações confirmadas de informações não verificadas. |
| V03 | Conferir a mensagem apresentada em P10. | A palavra deve estar corrigida para "disponíveis". |

A resolução dos problemas somente deve ser considerada confirmada após a verificação das telas atualizadas. Até essa verificação, os achados permanecem registrados como problemas identificados na versão avaliada.

## Checklist

- [x] Identificar a versão do protótipo avaliada.
- [x] Registrar a data da inspeção.
- [x] Definir o escopo das telas e estados examinados.
- [x] Utilizar as dez heurísticas de Nielsen.
- [x] Registrar a cobertura das heurísticas.
- [x] Identificar e documentar os achados V01, V02 e V03.
- [x] Atribuir severidade aos problemas identificados.
- [x] Registrar justificativas e recomendações.
- [x] Apresentar exemplos de boas práticas nas heurísticas sem violação confirmada.
- [x] Consolidar os achados da equipe.
- [x] Elaborar o plano de melhoria.
- [x] Registrar os estados que não foram avaliados.
- [ ] Inserir as evidências visuais dos achados.
- [ ] Confirmar e registrar as avaliações individuais realizadas por cada integrante.
- [ ] Realizar nova inspeção após as correções, quando implementadas.

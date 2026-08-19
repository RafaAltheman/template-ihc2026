# Entrega 1 — Conhecendo o projeto, o usuário e o problema

**Data:** 12/08/2026

**Status:** iniciada  
**Responsabilidade:** 1 solução consolidada por equipe

## Objetivo da atividade

Reinterpretar o tema do TCC sob a perspectiva de Interação Humano-Computador e construir um **entendimento comum entre os integrantes da equipe**.

A disciplina utiliza preferencialmente o tema do TCC para os exercícios de IHC. Isso vale tanto para TCCs que já preveem uma interface quanto para trabalhos cujo resultado principal é algoritmo, modelo, API, biblioteca, análise de dados, infraestrutura, estudo experimental ou outro artefato técnico.

> **Importante:** a interface projetada na disciplina é um artefato de aprendizagem de IHC. Ela **não se torna automaticamente uma obrigação do TCC**. Sua incorporação ao trabalho de conclusão depende de decisão da equipe e do orientador.

Antes de preencher, leia [`../GUIA_ESCOPO_IHC.md`](../GUIA_ESCOPO_IHC.md).

Nesta primeira semana a equipe **não deve começar desenhando telas**. Primeiro deverá compreender:

- o que o TCC realmente produz;
- quem poderia obter valor dessa contribuição;
- quais pessoas interagem, administram, configuram, interpretam ou são afetadas;
- o que essas pessoas precisam alcançar;
- como atividades relacionadas acontecem hoje;
- problemas, limitações e contexto;
- alternativas existentes;
- qual recorte de interação fará sentido para a disciplina.

Ao final desta entrega, a equipe deve diferenciar:

- **tema do TCC** × **escopo formal do TCC** × **escopo de IHC da disciplina**;
- **objetivo do projeto** × **objetivo do usuário**;
- **problema do usuário** × **solução tecnológica**;
- **fato conhecido** × **hipótese** × **lacuna de conhecimento**;
- **capacidade técnica** × **forma de uso dessa capacidade**;
- **funcionalidade** × **atividade/resultado que o usuário precisa alcançar**;
- **usuário direto** × **stakeholders**.

---

## Como classificar as respostas

Sempre que a resposta fizer uma afirmação sobre usuários, problemas, atividades, necessidades, contexto ou mercado, use:

- **[F] Fato conhecido** — existe evidência/fonte.
- **[H] Hipótese** — afirmação plausível que ainda precisa ser investigada.
- **[?] Não sabemos ainda** — lacuna relevante.

Quando usar `[F]`, informe a origem. Hipóteses prioritárias devem receber IDs (`H01`, `H02`...) e também ser registradas em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

> **Exemplo:** `[H] H01 — DBAs considerariam útil comparar automaticamente o plano atual de execução com uma recomendação produzida pelo algoritmo.`

Uma hipótese explicitada é melhor do que uma suposição escondida.

---

# 0. Identificação do TCC e da equipe

## 0.1 Membros

| Nome completo | Matrícula | GitHub |

| Rafaela Altheman de Campos | 22.125.062-4 | RafaAltheman |

| Manuella Filipe Peres | 24.224.039-3 | manu3lla |

| Letizia Lowatzki Baptistella | 22.125.063-2 | le-bap |

## 0.2 Título atual do TCC

**Aprendizado por reforço profundo para locomoção bípede de um robô humanoide em simulação**

## 0.3 Orientador(a)

Orientador: Isaac Jesus

Coorientador: Reinaldo Bianchi

## 0.4 Qual é o resultado principal atualmente previsto no TCC?

Marque e descreva:

- [ ] sistema/aplicação interativa;
- [ ] algoritmo;
- [X] modelo de IA/ML/LLM;
- [ ] biblioteca/API/framework;
- [ ] análise de dataset;
- [ ] estudo/benchmark/avaliação experimental;
- [ ] infraestrutura/backend;
- [ ] componente embarcado/IoT;
- [ ] outro: {{...}}.

**Descrição:** Modelo de aprendizado por reforço profundo responsável por aprender uma política de controle para a locomoção bípede do robô humanoide Atom, buscando uma caminhada estável e eficiente em ambiente simulado da RoboCup 3D.

## 0.5 O TCC já previa desenvolvimento de interface com usuário?

- [ ] Sim, a interface já faz parte do TCC.
- [ ] Parcialmente; existe alguma interação, mas ainda não está bem definida.
- [X] Não. O TCC é predominantemente técnico e não previa interface.

**Explique o que está formalmente previsto no TCC:** O TCC prevê a modelagem do robô humanoide Atom e sua integração à plataforma de simulação MuJoCo, onde serão realizados o treinamento e a avaliação do modelo de aprendizado por reforço profundo. A interação ocorre com o ambiente de simulação para configurar, executar e analisar os experimentos, mas não está previsto o desenvolvimento de uma interface específica voltada ao usuário.

> Esta resposta serve para separar o compromisso do TCC do projeto da disciplina. Mesmo quando a opção for **não**, a equipe irá definir uma interface para exercitar IHC.

---

# 1. Entendendo a contribuição do projeto

## 1.1 Explique o TCC em uma frase, sem citar linguagem de programação, framework ou banco de dados.

O TCC busca desenvolver uma estratégia de locomoção bípede estável e eficiente para o robô humanoide Atom por meio de aprendizado por reforço profundo em ambiente simulado.

## 1.2 Qual situação, atividade ou problema do mundo real motivou o TCC?

[F] A motivação surgiu a partir da experiência das integrantes em competições de robótica, principalmente no Brasil, onde foi possível observar a dificuldade das equipes em desenvolver um walking estável e eficiente. Problemas na locomoção, como quedas e baixa velocidade, acabam prejudicando diretamente o desempenho do robô durante as partidas.

## 1.3 Qual é a **capacidade/contribuição central** produzida pelo TCC?

[F] Nosso TCC busca melhorar a forma como o robô humanoide Atom caminha, usando aprendizado por reforço profundo para que ele aprenda uma política de controle capaz de manter o equilíbrio, se deslocar com mais estabilidade e velocidade e lidar melhor com situações inesperadas durante a simulação. A ideia é que esse walking contribua para um desempenho melhor do robô nas partidas.


## 1.4 O que se espera que esteja diferente **para pessoas, organizações ou processos** se essa contribuição for bem-sucedida?

[F] Se a proposta funcionar bem, ela pode contribuir não só para a RoboFEI, mas também servir como referência para outras equipes de futebol de robôs humanoides que enfrentam dificuldades parecidas com locomoção. O estudo pode ajudar no desenvolvimento de walkings mais estáveis e eficientes e mostrar como o aprendizado por reforço profundo pode ser aplicado nesse tipo de problema.

## 1.5 O que é mérito técnico/científico do TCC e o que seria uma possível aplicação prática?

| Mérito/contribuição técnica | Possível aplicação/valor em uso |

Mérito/contribuição técnica:

- Desenvolvimento e avaliação de uma política de controle com aprendizado por reforço profundo para a locomoção bípede do robô Atom.
  
- Análise do desempenho do agente considerando aspectos como estabilidade, velocidade e distância.
  
- Estudo do DRL como alternativa aos métodos tradicionais de controle de caminhada.

Possível aplicação/valor em uso:

- Melhorar o walking do Atom nas competições.
  
- Ajudar a RoboFEI a ter uma locomoção mais estável e eficiente.
  
- Servir como estudo e referência para outras equipes de robótica que enfrentam problemas semelhantes de locomoção humanoide.

---

# 2. Entendendo as pessoas envolvidas

## 2.1 Quem interage diretamente com o produto, se já existe interface prevista?

NÃO SE APLICA AO ESCOPO ORIGINAL

[F] O TCC não prevê uma interface própria para usuário. A interação atual acontece diretamente com o ambiente de simulação já existente (MuJoCo).

## 2.2 Quem poderia **usar, configurar, administrar, operar, interpretar ou tomar decisões** a partir da contribuição técnica?

Considere perfis profissionais e stakeholders, não apenas consumidores finais.

| Perfil | Relação com a contribuição | O que faria | Status/evidência |

| Pesquisadores e estudantes de robótica | Poderiam utilizar o estudo como referência ou base para novos experimentos | Comparariam algoritmos, parâmetros e resultados de locomoção | F |

| Integrantes de equipes de futebol de robôs humanoides | Usuários mais próximos da aplicação prática | Configurariam treinamentos, acompanhariam resultados e avaliariam a qualidade do walking | F |

| Desenvolvedores responsáveis pelo robô |Poderiam integrar ou adaptar a política de locomoção ao restante do sistema | Ajustariam configurações do robô e avaliariam a integração com outras funções | [H] H01 |

## 2.3 Existem pessoas afetadas que não usariam a interface diretamente?

| Stakeholder | Como é afetado | Usa interface? | Status/evidência |

| Demais integrantes da equipe RoboFEI | São beneficiados caso a melhoria da locomoção aumente o desempenho do robô nas competições | não | [F] |

| Outras equipes de futebol de robôs humanoides | Podem utilizar os resultados e aprendizados do trabalho como referência para seus próprios projetos | não | [F] |

## 2.4 Que características desses perfis podem influenciar a interação?

Considere conhecimento do domínio, experiência tecnológica, frequência de uso, necessidades de acessibilidade, responsabilidade profissional, familiaridade com métricas, linguagem técnica, urgência etc.

[H] H02 — Os principais usuários provavelmente terão algum conhecimento técnico em robótica, inteligência artificial ou aprendizado por reforço, então a interface pode utilizar termos como recompensa, episódio, velocidade, taxa de quedas e parâmetros de treinamento.

[F] Também é importante que os resultados sejam apresentados de forma visual, porque o desempenho não é avaliado por uma única métrica. O TCC considera distância, velocidade, altura do centro de massa, taxa de quedas e também avaliação visual do comportamento e desempenho do robô.

[H] H03 — Como treinamentos de aprendizado por reforço podem envolver várias tentativas e ajustes, esses usuários podem precisar comparar execuções diferentes e identificar rapidamente quais configurações produziram melhores resultados.

---

# 3. Entendendo objetivos e atividades

## 3.1 O que o usuário está tentando conseguir no mundo real?

Não responda “usar o algoritmo”, “clicar no sistema” ou “ver o dashboard”.

[F] O usuário busca conseguir uma locomoção mais estável, eficiente e competitiva para o robô humanoide, reduzindo quedas e melhorando sua capacidade de se deslocar e se recuperar durante situações de jogo.

## 3.2 Quais são as atividades mais importantes?

| ID | Atividade/objetivo | Quem realiza | Frequência/criticidade inicial | Status/evidência |

| A01 | Configurar e iniciar treinamentos do agente | Integrantes/desenvolvedores da equipe de robótica | Frequente / alta | [F] |

| A02 | Acompanhar e interpretar métricas de desempenho do treinamento | Integrantes da equipe e pesquisadores | Frequente / alta | [F] |

| A03 | Comparar os resultados dos treinamentos e avaliar visualmente a qualidade do walking | Integrantes da equipe | Frequente / alta | [F] |

## 3.3 Qual atividade parece mais frequente? Por quê?

[F] A atividade que parece mais frequente é acompanhar os treinamentos e analisar seus resultados, porque o desenvolvimento envolve vários ciclos de treinamento, avaliação e ajuste de parâmetros até chegar a um comportamento bom para o robô.

## 3.4 Qual parece mais crítica? Que consequência existe se for mal executada?

[F] A atividade mais crítica é interpretar corretamente os resultados do treinamento e decidir quais ajustes devem ser feitos. Uma interpretação errada pode levar a equipe a manter parâmetros ou uma função de recompensa inadequados, fazendo o agente aprender comportamentos que parecem bons pelas métricas, mas que não representam uma caminhada eficiente. O próprio TCC destaca que apenas a recompensa não é suficiente para avaliar o comportamento do agente.

---

# 4. Entendendo o problema ou processo atual

## 4.1 Como essas atividades são realizadas hoje, antes da interface imaginada na disciplina?

Pode existir software concorrente, linha de comando, planilha, notebook, script, painel técnico, processo manual, consulta a logs, análise visual, troca de mensagens, decisão por especialista etc.

[F] Atualmente, o treinamento e a avaliação são feitos diretamente no ambiente de simulação MuJoCo. Nós configuramos os experimentos, executamos o treinamento do agente, acompanhamos as métricas como recompensa, velocidade, distância percorrida e taxa de quedas, além de observar visualmente o comportamento do robô no simulador. Os resultados dos diferentes ciclos de treinamento precisam ser registrados e analisados.

## 4.2 O que é difícil, demorado, confuso, repetitivo, arriscado ou pouco transparente?

[F] O processo exige vários ciclos de treinamento, análise e ajuste de parâmetros, o que pode ser demorado e repetitivo. Além disso, não é suficiente analisar apenas a recompensa do agente, já que ela pode aumentar mesmo quando o comportamento aprendido não representa um bom walking. Por isso, é necessário analisar várias métricas e também observar o robô visualmente.

[H] H04 — Comparar diferentes treinamentos e entender quais alterações realmente melhoraram o desempenho pode ser difícil quando as informações ficam distribuídas entre execuções, métricas e observações visuais.

## 4.3 Que informações o profissional precisa interpretar para tomar decisão?

[F] O profissional precisa interpretar informações como:

-recompensa obtida durante o treinamento
-distância percorrida
-velocidade média
-taxa de quedas
-estabilidade e equilíbrio do robô
-comportamento visual do walking
-configurações e parâmetros utilizados em cada treinamento

Essas informações ajudam a decidir se o treinamento está evoluindo e quais ajustes devem ser feitos para os próximos experimentos

## 4.4 O que acontece quando a atividade falha ou quando o resultado é interpretado incorretamente?

[F] Uma interpretação incorreta pode fazer a equipe considerar um treinamento como bom mesmo quando o agente aprendeu um comportamento inadequado. Por exemplo, o agente pode aumentar sua recompensa mantendo-se parado e equilibrado, sem realmente aprender a caminhar de forma eficiente. Também podem ser feitos ajustes inadequados nos parâmetros ou na função de recompensa, comprometendo os treinamentos seguintes.

## 4.5 Conte uma situação concreta.

Escreva uma pequena narrativa com pessoa, objetivo, atividade, contexto, dificuldade e consequência. **Não descreva ainda a futura solução.**

[F] Uma integrante da equipe roda um treinamento para tentar melhorar o walking do robô. No final, vê que a recompensa aumentou e pode parecer que o resultado foi bom. Mas, olhando outras métricas e o robô no simulador, percebe que ele até consegue ficar mais equilibrado, porém quase não anda. Nesse caso, olhar só para a recompensa poderia levar a uma conclusão errada sobre o treinamento.

## 4.6 Que evidência existe hoje?

| Evidência/fonte | O que sustenta | Limitação |

| Experimentos realizados com o robô BahiaRT | Mostram que o treinamento passa por diferentes fases e exige acompanhamento do comportamento do agente | Os testes ainda não foram realizados completamente com o Atom |

| Experiência das integrantes com a RoboFEI e competições | Sustenta a dificuldade prática relacionada ao desenvolvimento de um walking competitivo | É uma experiência do grupo e ainda não representa outras equipes |

---

# 5. Entendendo o contexto de uso

## 5.1 Onde e em quais situações a interação poderia ocorrer?

[H] H03 — A interação poderia acontecer principalmente em laboratórios de robótica ou em computadores utilizados pelas equipes durante o desenvolvimento e teste dos robôs. O uso aconteceria principalmente durante a configuração, execução e análise de treinamentos de locomoção.

## 5.2 Em quais dispositivos/equipamentos?

[H] Principalmente em computadores ou notebooks utilizados para executar o ambiente de simulação, realizar os treinamentos e analisar os resultados.

## 5.3 Existem condições físicas relevantes?

Considere iluminação, ruído, mobilidade, conexão, privacidade, uso compartilhado, interrupções, pressão de tempo etc.

[H] H04 — Não foram identificadas condições físicas muito específicas para o uso. Como a interação deve ocorrer principalmente em computadores, os pontos mais relevantes são a disponibilidade do equipamento e a estabilidade do ambiente durante a execução dos treinamentos, além de um hardware equivalente 

## 5.4 Existem fatores sociais ou organizacionais?

Considere papéis, chefias, equipes, permissões, aprovação, responsabilidade profissional, auditoria, turnos e colaboração.

[H] Sim. O desenvolvimento acontece dentro de uma equipe de robótica, então diferentes integrantes podem participar da configuração dos experimentos, análise dos resultados e tomada de decisões.

[F] Também existe acompanhamento de professores e orientadores, que participam das decisões técnicas do projeto.

## 5.5 Existe necessidade de histórico, rastreabilidade ou auditoria?

[F] Existe necessidade de histórico e rastreabilidade dos experimentos, já que o TCC prevê ciclos de ajuste dos parâmetros e da função de recompensa, registrando as métricas de cada treinamento para acompanhar o impacto das mudanças realizadas.

## 5.6 Um erro pode produzir consequência relevante? Qual?

[F] Sim. Uma configuração inadequada ou uma interpretação errada dos resultados pode fazer o agente aprender um comportamento ruim, comprometer a convergência do treinamento e gerar perda de tempo computacional. Em alguns casos, uma escolha inadequada das observações fornecidas ao agente pode comprometer o aprendizado mesmo que o algoritmo esteja correto.

---

# 6. Entendendo mercado e alternativas existentes

> Nesta entrega faça apenas um **levantamento inicial**. A análise aprofundada ocorre na Entrega 2.

## 6.1 Como pessoas resolvem problemas semelhantes hoje?

| Alternativa atual | Quem usa | Para quê | Status/evidência |
|---|---|---|---|
| {{...}} | {{...}} | {{...}} | {{...}} |

## 6.2 Existem produtos que atuam na mesma área, mesmo sem serem equivalentes ao TCC?

{{[F/H/?] ...}}

## 6.3 Quais interfaces profissionais esse público já conhece?

Exemplos possíveis: ferramentas de banco, IDEs, consoles de nuvem, dashboards, plataformas de dados, ferramentas de monitoramento, painéis de IA, sistemas administrativos.

{{[F/H/?] ...}}

## 6.4 O que essas soluções parecem fazer bem?

{{[F/H/?] ...}}

## 6.5 O que parecem fazer mal, dificultar ou não atender?

{{[F/H/?] ...}}

## 6.6 Que padrões de interface ou vocabulário parecem familiares a esse público?

{{[F/H/?] ...}}

---

# 7. Derivando o escopo de IHC da disciplina

## 7.1 Escolha o caminho do projeto

### Caminho A — TCC já possui interface

Explique qual parte da interface será usada como recorte da disciplina e por que esse fluxo é relevante.

{{...}}

### Caminho B — TCC não possui interface prevista

Faça o exercício de transferência de uso:

> **Imagine que o TCC foi concluído com sucesso e uma empresa, laboratório ou organização quer transformar a contribuição em algo utilizável. Quem precisaria interagir com ela e para quê?**

Responda:

1. quem poderia contratar/adotar a solução? {{...}}
2. quem seria o usuário direto? {{...}}
3. quem administraria/configuraria? {{...}}
4. quem interpretaria resultados? {{...}}
5. quem tomaria decisões? {{...}}
6. quais dados/entradas seriam necessários? {{...}}
7. quais resultados deveriam ser compreendidos? {{...}}
8. que erros/rupturas seriam possíveis? {{...}}

## 7.2 Qual perfil será priorizado no projeto de IHC?

{{...}}

**Por que esse perfil foi escolhido?** {{...}}

## 7.3 Qual objetivo desse usuário será priorizado?

{{...}}

## 7.4 Que interface será explorada na disciplina?

Complete:

> **Para fins da disciplina de IHC, será projetada uma interface que permita a `{{perfil}}` utilizar `{{capacidade/resultado do TCC}}` para `{{objetivo}}`, no contexto de `{{situação}}`.**

{{...}}

## 7.5 Qual é a relação dessa interface com o TCC?

- [ ] Já fazia parte do TCC.
- [ ] É um aprofundamento de algo parcialmente previsto.
- [ ] É uma extensão conceitual criada para a disciplina.
- [ ] É um protótipo demonstrativo de aplicação potencial.
- [ ] Outra: {{...}}.

> **Declaração:** a interface desenvolvida nesta disciplina é um artefato de aprendizagem de IHC baseado no tema do TCC. Sua inclusão ou implementação no TCC somente ocorrerá se isso for posteriormente decidido pela equipe e pelo orientador.

---

# 8. Levantando possibilidades de interação — sem desenhar ainda

A equipe pode registrar possibilidades para investigação. **Não significa que todas serão implementadas.**

Marque apenas as que parecem plausíveis e explique o objetivo correspondente.

| Possibilidade | Pode fazer sentido? | Objetivo/tarefa que justificaria | Evidência atual |
|---|---|---|---|
| Dashboard/visão geral | sim/não/talvez | {{...}} | {{...}} |
| Configuração/parametrização | sim/não/talvez | {{...}} | {{...}} |
| Entrada/upload/seleção de dados | sim/não/talvez | {{...}} | {{...}} |
| Acompanhamento de processamento | sim/não/talvez | {{...}} | {{...}} |
| Relatório/resultados | sim/não/talvez | {{...}} | {{...}} |
| Histórico com busca/filtros | sim/não/talvez | {{...}} | {{...}} |
| Comparação de resultados | sim/não/talvez | {{...}} | {{...}} |
| Explicabilidade/detalhamento | sim/não/talvez | {{...}} | {{...}} |
| Administração/configurações globais | sim/não/talvez | {{...}} | {{...}} |
| Usuários/perfis/permissões | sim/não/talvez | {{...}} | {{...}} |
| CRUD de entidade do domínio | sim/não/talvez | {{...}} | {{...}} |
| Auditoria/logs | sim/não/talvez | {{...}} | {{...}} |
| Alertas/ocorrências | sim/não/talvez | {{...}} | {{...}} |
| Ajuda/documentação | sim/não/talvez | {{...}} | {{...}} |

> **Atenção:** “login + dashboard + CRUD” não é uma solução universal. Cada padrão deve surgir de uma tarefa real.

---

# 9. Benefícios e ações iniciais

## 9.1 Qual benefício concreto o projeto de IHC pretende oferecer?

| Benefício esperado | Problema/necessidade | Usuário | Status/evidência |
|---|---|---|---|
| {{...}} | {{...}} | {{...}} | {{...}} |

## 9.2 Que ações o usuário deverá conseguir realizar?

| ID | O usuário precisa conseguir... | Para alcançar... | Prioridade inicial |
|---|---|---|---|
| F01 | {{ação}} | {{objetivo}} | alta/média/baixa |

## 9.3 Tecnologias/restrições já definidas no TCC

A tecnologia aparece **agora**, depois do entendimento do uso.

| Tecnologia/restrição | Por que existe | Possível impacto na interação |
|---|---|---|
| {{...}} | {{...}} | {{...}} |

---

# 10. Hipóteses e dúvidas prioritárias

| ID | Hipótese/dúvida | Por que importa | Como poderá ser investigada |
|---|---|---|---|
| H01 | {{...}} | {{...}} | Entrega 2/3/7/... |
| H02 | {{...}} | {{...}} | {{...}} |
| H03 | {{...}} | {{...}} | {{...}} |

Registre em [`../RASTREABILIDADE.md`](../RASTREABILIDADE.md).

---

# 11. Síntese da equipe

| Pergunta | Síntese atual |
|---|---|
| Qual é a contribuição central do TCC? | {{...}} |
| O TCC já previa interface? | {{...}} |
| Quem é o usuário prioritário de IHC? | {{...}} |
| O que ele precisa alcançar? | {{...}} |
| Qual problema/atividade será estudado? | {{...}} |
| Como isso acontece hoje? | {{...}} |
| Qual é o contexto de uso? | {{...}} |
| Que interface/recorte será explorado? | {{...}} |
| Como a interface se relaciona ao TCC? | {{...}} |
| Quais pontos ainda são hipóteses? | {{H01...}} |

### Delimitação

**Dentro do escopo de IHC:** {{...}}  
**Fora do escopo de IHC:** {{...}}  
**Dentro do escopo formal do TCC:** {{...}}  
**Interface da disciplina será implementada no TCC?** não definido / sim / não — {{justificativa, se houver}}

---

# 12. Como esta entrega alimenta as próximas

- **Entrega 2:** verifica mercado, concorrentes e interfaces profissionais representativas.
- **Entrega 3:** detalha perfis e contexto.
- **Entrega 4:** aprofunda situações problemáticas.
- **Entrega 5:** modela tarefas centrais.
- **Entrega 6:** experimenta alternativas em baixa fidelidade.
- **Entrega 7:** investiga hipóteses com dados.
- **Entrega 8:** define restrições e metas de usabilidade.
- **Entregas 9–11:** transformam o recorte em modelo de interação e protótipo.
- **Entregas 12–14:** avaliam a interface construída na disciplina.

A Entrega 1 é uma **fotografia inicial do conhecimento**. Ela pode e deve ser revisada quando surgirem evidências.

---

# 13. Relação com INOVA e comunicação do projeto

Prepare uma explicação de até três frases:

1. **Problema/atividade humana:** {{...}}
2. **Contribuição técnica do TCC:** {{...}}
3. **Como uma pessoa poderia utilizar essa contribuição:** {{...}}

Essa síntese ajuda a apresentar o projeto para público não especializado sem reduzir seu mérito técnico.

---

# Checklist de qualidade

- [ ] Está clara a diferença entre tema do TCC, escopo formal do TCC e escopo de IHC.
- [ ] A equipe declarou se o TCC já previa interface.
- [ ] Se não previa, foi derivado um usuário plausível e um objetivo de uso.
- [ ] A interface de IHC não foi apresentada como obrigação automática do TCC.
- [ ] A contribuição do TCC foi descrita sem começar por tecnologias de implementação.
- [ ] Usuários diretos e stakeholders foram diferenciados.
- [ ] Foram considerados profissionais que configuram, administram, interpretam ou decidem, quando pertinente.
- [ ] Objetivo do usuário não foi confundido com objetivo do projeto.
- [ ] Processo/problema atual foi descrito antes da solução.
- [ ] Existe situação concreta de uso/problema.
- [ ] Contexto físico, social/organizacional, dispositivos e consequências de erro foram considerados.
- [ ] Mercado/alternativas existentes foram levantados inicialmente.
- [ ] Possibilidades como dashboard, relatório, histórico, filtros e CRUD foram tratadas como hipóteses de solução, não como requisitos automáticos.
- [ ] Cada possibilidade de interface tem um objetivo/tarefa que poderia justificá-la.
- [ ] Afirmações relevantes estão marcadas `[F]`, `[H]` ou `[?]`.
- [ ] Hipóteses prioritárias receberam IDs e foram para a rastreabilidade.
- [ ] O recorte de IHC é viável para modelar, prototipar e avaliar no semestre.
- [ ] A equipe consegue explicar problema humano → contribuição computacional → forma de uso.

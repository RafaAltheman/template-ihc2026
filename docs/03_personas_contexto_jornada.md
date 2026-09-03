# Entrega 3 — Personas, mapa de empatia, contexto de uso e jornada

**Data:** {{dd/mm/aaaa}}  
**Status:** 🟨 Em andamento
**Responsabilidade:** 1 persona por integrante; 1 mapa de empatia, 1 contexto de uso consolidado e 1 jornada por equipe (salvo orientação diferente do docente).

## Objetivo da atividade

Representar grupos de usuários de forma útil para decisões de design. Persona não é personagem decorativo: suas características devem alterar requisitos, prioridades, linguagem, fluxos ou critérios de avaliação.

## Atenção a projetos técnicos

Em TCCs sem interface original, a persona pode representar um **profissional que se apropria da contribuição técnica**: DBA, analista, cientista de dados, administrador, pesquisador, técnico, operador, gestor ou especialista de domínio.

Não escolha um perfil apenas porque “parece combinar” com a tecnologia. Explique **qual objetivo esse perfil teria e qual parte da contribuição do TCC produziria valor para ele**. Se ainda for hipótese, mantenha como hipótese/proto-persona a validar.

Também considere papéis diferentes quando houver tarefas distintas, por exemplo:

- operador que executa análises;
- administrador que configura e gerencia permissões;
- especialista que interpreta resultados;
- gestor que consulta relatórios e decide;
- auditor que revisa histórico.

## Entradas da Entrega 1

Antes de criar personas, retome os tipos de usuários, características relevantes, objetivos e hipóteses registradas na Entrega 1. A persona **não deve transformar uma hipótese inicial em fato por meio de uma história fictícia**.

| Item da Entrega 1 | Status inicial | Evidência disponível agora | Como será tratado nesta entrega |
|---|---|---|---|
| {{usuário/objetivo/característica/H01...}} | F / H / ? | {{...}} | incorporar / manter como hipótese / descartar / investigar |

## 1. Personas

### Persona P01 — Rafael Martins

**Autor(a):** Rafaela Altheman de Campos — 22.125.062-4  
**Tipo:** primária  
**Base de evidências:** experiência da equipe
**Hipóteses da Entrega 1 relacionadas:** H01, H02, H03

![Persona P01](../assets/03_personas/persona_p01.svg)

| Campo | Descrição |
|---|---|
| Faixa etária / contexto relevante | 24 anos; participa ativamente de uma equipe de robótica humanoide e está envolvido no desenvolvimento e testes do robô. [H] |
| Ocupação/papel | Integrante técnico de equipe de robótica humanoide, responsável por desenvolver, testar e avaliar comportamentos do robô. [H] |
| Conhecimento do domínio | Conhece conceitos de robótica humanoide, locomoção bípede, treinamento e métricas de desempenho. [H] |
| Experiência tecnológica | Alta: utiliza ambientes de simulação, ferramentas de desenvolvimento, scripts e ferramentas para análise de dados. [H] |
| Objetivos | Melhorar o desempenho, reduzir quedas, aumentar a estabilidade e velocidade e identificar quais alterações realmente melhoram o robô. [F/H] |
| Necessidades | Visualizar métricas de forma rápida, comparar diferentes treinamentos e versões, consultar histórico e relacionar métricas com o comportamento observado do robô. [H] |
| Dores/frustrações | Precisa analisar informações distribuídas entre diferentes execuções, métricas e observações visuais. Pode interpretar um treinamento de forma incorreta quando uma métrica isolada apresenta bons resultados. [F/H] |
| Motivadores | Obter um robô mais estável e competitivo, economizar tempo nos ciclos de treinamento e tomar decisões técnicas com base em evidências. [H] |
| Restrições/acessibilidade | Pode trabalhar sob pressão durante períodos de testes e preparação para competições. Necessita de informações técnicas sem excesso de simplificação. [H] |
| Ambiente típico de uso | Laboratório de robótica ou ambiente de desenvolvimento, utilizando computador ou notebook durante treinamentos, testes e preparação para competições. [H] |
| Comportamentos relevantes | Executa diversos ciclos de treinamento, acompanha métricas, observa o comportamento do robô, compara resultados e ajusta parâmetros para novos experimentos. [F/H] |

**Decisões de design influenciadas por P01:**

- Priorizar uma visão rápida das principais métricas de desempenho, sem esconder informações técnicas importantes.
- Permitir comparação direta entre diferentes treinamentos, versões e execuções.
- Apresentar métricas como velocidade, distância percorrida, recompensa, taxa de quedas, número de gols e números de passes, evitando que o usuário dependa de uma única métrica.
- Disponibilizar histórico e filtros para localizar rapidamente testes anteriores.
- Utilizar vocabulário técnico familiar ao usuário, como recompensa, agente, velocidade, torque e taxa de quedas.
- Facilitar a relação entre resultados quantitativos e o comportamento visual do robô.

---

### Persona P02 — Marina Oliveira

**Autor(a):** Manuella Filipe Peres — 22.224.029-3  
**Tipo:** primária  
**Base de evidências:** experiência da equipe
**Hipóteses da Entrega 1 relacionadas:** H01, H02, H03

![Persona P02](../assets/03_personas/persona_p02.svg)

| Campo | Descrição |
|---|---|
| Faixa etária / contexto relevante | 27 anos; pesquisadora que atua diretamente no desenvolvimento de um robô de robótica humanoide [H] |
| Ocupação/papel | Pesquisadora de robótica responsável por estudar, testar e aprimorar o comportamento e a locomoção do robô. [H] |
| Conhecimento do domínio | Avançado em robótica e aprendizado de máquina, com conhecimento sobre locomoção humanoide, treinamento de agentes e avaliação de desempenho de robôs. [H] |
| Experiência tecnológica | Tem experiência alta: utiliza ferramentas de programação, simulação, treinamento, coleta de dados, visualização de métricas e análise de resultados. [H] |
| Objetivos | Melhorar o desempenho do robô, testar diferentes estratégias de locomoção, identificar configurações mais eficientes e compreender os resultados obtidos durante os treinamentos. [H] |
| Necessidades | Acessar rapidamente os resultados dos treinamentos, comparar diferentes experimentos, visualizar métricas de desempenho e consultar os parâmetros utilizados em cada execução. [H] |
| Dores/frustrações | A quantidade de experimentos e dados gerados durante os treinamentos pode dificultar a comparação entre resultados. Também pode ser trabalhoso identificar quais alterações nos parâmetros realmente contribuíram para a melhora ou piora do robô. [H] |
| Motivadores | Melhorar o desempenho do robô, reduzir o tempo necessário para análise dos experimentos, encontrar configurações mais eficientes e obter resultados confiáveis para orientar os próximos treinamentos. [H] |
| Restrições/acessibilidade | Possui conhecimento técnico elevado, mas trabalha com grande quantidade de informações e resultados simultaneamente. A interface deve facilitar a análise sem esconder informações importantes para a pesquisa. [H] |
| Ambiente típico de uso | Laboratório de robótica ou ambiente de desenvolvimento, utilizando computador para executar treinamentos, acompanhar testes e analisar os resultados do robô. [H] |
| Comportamentos relevantes | Executa treinamentos e testes, altera parâmetros do robô, acompanha métricas, compara diferentes execuções, analisa o comportamento do robô e utiliza os resultados para definir novos experimentos. [H] |

**Decisões de design influenciadas por P02:**

- Permitir comparar diferentes treinamentos e execuções do robô.
- Exibir as principais métricas de desempenho de maneira clara e objetiva.
- Permitir consultar os parâmetros utilizados em cada treinamento.
- Facilitar a identificação de melhorias ou regressões no desempenho do robô.
- Disponibilizar histórico dos experimentos para evitar a perda de informações de treinamentos anteriores.
- Apresentar informações técnicas suficientes para apoiar decisões de pesquisa sem sobrecarregar a visualização inicial.
- Permitir relacionar os resultados quantitativos das métricas com o comportamento observado no robô.

---

### Persona P03 — Carlos Almeida

**Autor(a):** Letizia Lowatzki Baptistella — 22.125.063-2  
**Tipo:** secundária  
**Base de evidências:** participação de professores e orientadores no projeto
**Hipóteses da Entrega 1 relacionadas:** H01, H02

![Persona P03](../assets/03_personas/persona_p03.svg)

| Campo | Descrição |
|---|---|
| Faixa etária / contexto relevante | 52 anos; acompanha projetos de pesquisa ou equipes de robótica e participa de decisões técnicas. [H] |
| Ocupação/papel | Professor, orientador ou responsável técnico que acompanha o desenvolvimento de robôs humanoides. [F/H] |
| Conhecimento do domínio | Alto conhecimento em robótica e pesquisa, mas pode não acompanhar todos os detalhes das implementações e dos treinamentos realizados pela equipe. [H] |
| Experiência tecnológica | Alta, especialmente em ferramentas de pesquisa, análise de resultados e acompanhamento de experimentos. [H] |
| Objetivos | Avaliar a evolução do projeto, identificar problemas relevantes e orientar a equipe na escolha de próximos experimentos e melhorias. [F/H] |
| Necessidades | Obter uma visão consolidada do desempenho, comparar resultados importantes e compreender rapidamente quais aspectos evoluíram ou pioraram. [H] |
| Dores/frustrações | Não participa necessariamente de todos os experimentos e pode precisar compreender resultados produzidos por outros integrantes. Consultar informações fragmentadas pode dificultar o acompanhamento da evolução do projeto. [H] |
| Motivadores | Acompanhar o progresso da equipe, apoiar decisões técnicas e verificar se os resultados obtidos são coerentes com os objetivos do projeto. [H] |
| Restrições/acessibilidade | Possui pouco tempo disponível para analisar cada experimento individualmente. A interface deve permitir uma leitura rápida, mas possibilitar acesso aos detalhes quando necessário. [H] |
| Ambiente típico de uso | Universidade, laboratório ou reuniões da equipe, utilizando computador ou notebook para acompanhar resultados e discutir decisões técnicas. [H] |
| Comportamentos relevantes | Consulta resultados consolidados, compara versões ou experimentos relevantes, questiona resultados inesperados e utiliza as informações para orientar a equipe. [H] |

**Decisões de design influenciadas por P03:**

- Disponibilizar uma visão geral do desempenho antes de apresentar detalhes técnicos.
- Destacar mudanças relevantes entre versões e experimentos.
- Permitir acessar detalhes de uma execução quando houver necessidade de investigação.
- Utilizar gráficos e indicadores que facilitem a interpretação rápida da evolução do robô.
- Evitar sobrecarregar a visão inicial com parâmetros de baixo nível.
- Permitir gerar ou consultar relatórios que possam apoiar discussões e decisões da equipe.

### Síntese das personas

As três personas representam diferentes formas de interação com os resultados do desenvolvimento de robôs humanoides. Rafael é o usuário técnico e primário, que realiza treinamentos, acompanha métricas e toma decisões diretamente relacionadas ao desenvolvimento do walking. Marina representa o contexto de pesquisa, no qual a comparação e a reprodutibilidade dos experimentos são importantes. Carlos representa o papel de orientação e tomada de decisão, necessitando principalmente compreender a evolução geral e identificar problemas relevantes sem necessariamente acompanhar cada execução.

A Persona P01 (Rafael Martins) é considerada prioritária para o projeto de IHC, pois corresponde mais diretamente ao perfil definido na Entrega 1: integrante de uma equipe de robótica humanoide responsável por acompanhar, analisar e contribuir para a melhoria do desempenho do robô. O objetivo principal da interface é justamente apoiar esse usuário na visualização, comparação e interpretação dos resultados. [F] 

As características de Marina e Carlos permanecem parcialmente como proto-personas, pois a Entrega 1 ainda não apresenta entrevistas ou questionários específicos com pesquisadores externos e professores/orientadores. Portanto, suas características devem ser validadas nas próximas etapas, especialmente na investigação das hipóteses H01, H02 e H03.

## 2. Mapa de empatia — equipe

**Persona escolhida:** {{P01}}  
**Justificativa:** {{por que esse perfil é relevante}}

![Mapa de empatia](../assets/03_personas/mapa_empatia.svg)

Documente também em texto: o que vê; ouve; diz/faz; pensa/sente; dores; ganhos. Diferencie **evidência** de **hipótese**.

## 3. Contexto de uso — consolidação

| Dimensão | Descrição | Implicação de design |
|---|---|---|
| Usuários | {{...}} | {{...}} |
| Tarefas | {{...}} | {{...}} |
| Equipamentos | {{...}} | {{...}} |
| Ambiente físico | {{...}} | {{...}} |
| Ambiente social/organizacional | {{...}} | {{...}} |
| Papéis/permissões/governança | {{...}} | {{...}} |
| Volume de dados/histórico | {{...}} | {{...}} |

## 4. Jornada do usuário — equipe

**Persona:** {{P01}}  
**Objetivo da jornada:** {{...}}  
**Início e fim da jornada:** {{...}}

| Etapa | Situação/ação | Objetivo | Pensamento/emoção | Dor | Oportunidade de design | Evidência |
|---|---|---|---|---|---|---|
| 1 | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} | {{...}} |

> A jornada pode incluir etapas **antes, durante e depois** do uso do produto. Não transforme a jornada em lista de telas.

## Síntese

Quais necessidades e objetivos devem obrigatoriamente aparecer nos cenários e nas tarefas seguintes?

## Checklist

- [ ] Existe pelo menos uma persona por integrante.
- [ ] As personas não são apenas diferenças demográficas superficiais.
- [ ] Está claro o que é dado real e o que é hipótese/proto-persona.
- [ ] A persona não “validou por ficção” uma hipótese da Entrega 1; afirmações continuam marcadas como hipótese quando não há evidência.
- [ ] Objetivos e dores têm consequência para o design.
- [ ] Contexto de uso está coerente com a Entrega 1.
- [ ] Em TCC sem interface original, a persona possui relação explícita com a contribuição técnica.
- [ ] Papéis administrativos, técnicos e decisórios só foram criados quando possuem objetivos/tarefas diferentes.
- [ ] Jornada possui etapas, dores e oportunidades e não é apenas wireflow.
- [ ] IDs das personas foram adicionados à rastreabilidade.

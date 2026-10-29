# Entrega 6 — Prototipação em papel

**Data:** {{28/10/2026}}  
**Status:** 🟨 em andamento
**Responsabilidade:** 1 solução integrada por equipe

## Objetivo da atividade

Externalizar rapidamente ideias de interação em baixa fidelidade para explorar alternativas antes de investir em detalhes visuais. O valor da atividade está no **ciclo construir → simular → observar → revisar**, não na beleza do desenho.

## 1. Escopo do protótipo

### Personas:

P01 — Rafael Martins: responsável por avaliar os resultados dos treinamentos e identificar se houve melhoria real no desempenho do robô.

P02 — Marina Oliveira: responsável por localizar execuções anteriores, comparar experimentos e investigar possíveis causas para diferenças de desempenho.

P03 — Carlos Almeida: responsável por acompanhar a evolução do desempenho do robô, interpretar indicadores e comunicar à equipe os pontos que precisam de investigação.

### Cenários/tarefas cobertos:

C01/T01: avaliar se o resultado de um treinamento representa uma melhoria real no desempenho do robô, comparando indicadores com uma execução de referência (baseline) e registrando uma conclusão fundamentada.

C02/T02: localizar duas execuções anteriores por identificadores ou filtros, comparar suas métricas e parâmetros e registrar uma hipótese para explicar as diferenças encontradas, acompanhada de evidências e ressalvas.

C03/T03: consultar uma síntese da evolução do desempenho ao longo dos treinamentos, identificar pontos relevantes de investigação e apresentar os resultados à equipe, permitindo consultar evidências detalhadas durante a reunião.

### Objetivos principais:

O protótipo tem como objetivo explorar uma solução integrada de visualização e análise dos resultados dos treinamentos do robô humanoide, facilitando a interpretação dos indicadores e apoiando decisões da equipe sobre possíveis melhorias e necessidades de investigação.

Para isso, a interface deverá permitir:

Visualizar os resultados de treinamentos, incluindo velocidade média, distância percorrida, taxa de quedas, estabilidade, gols marcados e força de chute.

Consultar o histórico de execuções utilizando busca por identificador e filtros de período, versão e parâmetros.

Selecionar e comparar duas execuções, apresentando métricas e configurações lado a lado para facilitar a identificação de diferenças.

Avaliar se uma execução apresentou melhoria em relação a um baseline, considerando ganhos e possíveis regressões em diferentes indicadores.

Registrar conclusões e hipóteses com justificativas, evidências e ressalvas, mantendo a associação com as execuções analisadas.

Acompanhar a evolução dos indicadores e parâmetros ao longo do tempo por meio de um painel de síntese.

Consultar evidências detalhadas e retornar ao contexto anterior sem perder o período, os filtros ou as execuções selecionadas.

Apoiar a comunicação dos resultados durante reuniões, mantendo a interpretação e a definição dos encaminhamentos sob responsabilidade da equipe.

O escopo da prototipação será concentrado nas interações necessárias para realizar essas três tarefas. A proposta não inclui a implementação interna dos algoritmos de treinamento, nem a automatização da interpretação dos resultados ou da definição de prioridades.

Por se tratar de um protótipo em papel, as telas serão representadas em baixa fidelidade, priorizando a organização das informações, os controles de navegação, os fluxos entre telas e os estados de interação. O objetivo é identificar dificuldades de uso e revisar a estrutura da solução antes da implementação de uma interface funcional.

## 1.1 Possíveis famílias de interface

Escolha apenas o que for coerente com tarefas e cenários. Para TCCs técnicos, o protótipo pode explorar:

- **dashboard** para monitoramento e tomada de decisão;
- **configuração/parametrização** para preparar algoritmo/modelo/processo;
- **entrada/seleção de dados** com validação;
- **acompanhamento de execução** com progresso, fila, cancelamento e recuperação;
- **relatório/resultados** com explicação, gráficos e exportação;
- **histórico** com busca, filtros, ordenação e detalhes;
- **comparação** entre execuções, versões, algoritmos ou períodos;
- **administração** de usuários, papéis, permissões ou entidades do domínio;
- **auditoria/logs** traduzidos para o perfil;
- **alertas/ocorrências** com ação de resposta.

> Não desenhe todas essas telas por obrigação. O objetivo da baixa fidelidade é experimentar a **estrutura da interação** necessária para as tarefas priorizadas.

## 2. Fluxos escolhidos

Os fluxos foram definidos com base nas três tarefas priorizadas na Entrega 5, contemplando a avaliação de treinamentos, a comparação de execuções anteriores e o acompanhamento da evolução do desempenho do robô. A proposta é integrar essas funcionalidades em uma única interface, permitindo que diferentes integrantes da equipe consultem os resultados de acordo com seus objetivos.

| Fluxo | Tarefa/objetivo | Por que foi priorizado |
|---|---|---|
| PF01 | **T01 — Avaliar melhoria de um treinamento:** selecionar uma execução, definir um baseline comparável, analisar métricas e evidências e registrar uma conclusão sobre o desempenho. | É uma atividade frequente e crítica para a evolução do robô. Uma avaliação incorreta pode levar a ajustes inadequados nos treinamentos e ao desperdício de recursos computacionais. |
| PF02 | **T02 — Localizar e comparar execuções anteriores:** buscar duas execuções por ID ou filtros, comparar métricas e parâmetros e registrar uma hipótese sobre as diferenças encontradas. | Garante rastreabilidade dos experimentos e permite investigar variações de desempenho. A comparação estruturada reduz o risco de perder informações ou atribuir causas sem evidências suficientes. |
| PF03 | **T03 — Consultar síntese e comunicar pontos de investigação:** selecionar um período, visualizar a evolução dos indicadores, identificar pontos relevantes e apresentar os resultados à equipe, consultando evidências detalhadas quando necessário. | Apoia reuniões de acompanhamento e decisões sobre futuras investigações. O fluxo permite organizar os resultados e manter o contexto da análise durante a comunicação com a equipe. |

### Descrição dos fluxos

**PF01 — Avaliação de melhoria do treinamento**

O usuário acessa o histórico de treinamentos e seleciona uma execução para avaliação. Em seguida, escolhe um baseline, verifica a compatibilidade entre as execuções e consulta as métricas e evidências disponíveis. Após analisar os resultados, classifica o treinamento como melhoria, não melhoria ou evidências insuficientes, registrando uma justificativa associada às execuções.

**PF02 — Localização e comparação de execuções**

O usuário localiza duas execuções anteriores utilizando identificadores conhecidos ou filtros do histórico. Depois de confirmar as seleções, acessa uma visualização comparativa das métricas, versões e parâmetros. Com base nas divergências observadas, formula uma hipótese explicativa, registra as evidências utilizadas e indica possíveis limitações da análise.

**PF03 — Acompanhamento e comunicação do desempenho**

O usuário seleciona um período de análise e consulta um painel com a evolução dos principais indicadores dos treinamentos. A partir dos resultados, identifica tendências, regressões e pontos que precisam de investigação. Durante a apresentação à equipe, pode consultar evidências detalhadas sem perder o contexto do painel. Por fim, a equipe discute os resultados e define os encaminhamentos necessários.

### Integração entre os fluxos

Os três fluxos compartilham informações sobre execuções, métricas e parâmetros dos treinamentos. O histórico e a comparação de resultados atendem principalmente aos fluxos PF01 e PF02, enquanto o painel de evolução temporal atende ao PF03.

Essa integração permite reutilizar componentes e informações, evitando a criação de telas independentes para funcionalidades semelhantes. A prototipação em papel deverá representar tanto os caminhos principais quanto situações relevantes, como ausência de dados, incompatibilidade entre execuções e retorno ao painel após a consulta de evidências.

## 3. Telas e estados

- Numere as telas/estados (`P01`, `P02`...).
- Indique controles que mudam o estado.
- Mostre pelo menos caminhos principais e estados de erro/retorno relevantes.

![Protótipo](../assets/06_prototipos/prototipo_fluxo_01.svg)

## 4. Simulação / walkthrough

Realize uma simulação com uma pessoa que não participou da elaboração dessas telas. Um colega pode ser usado **para essa iteração formativa**, mas isso não substitui os participantes finais da Entrega 14.

| Observação | Tela/ação | Evidência | Consequência para o design |
|---|---|---|---|
| {{...}} | {{...}} | {{...}} | {{...}} |

## 5. Alterações após a simulação

| Antes | Problema | Depois | Justificativa |
|---|---|---|---|
| {{...}} | {{...}} | {{...}} | {{...}} |

## Checklist

- [ ] O protótipo cobre tarefas relevantes da Entrega 5.
- [ ] Cada tela/estado pode ser justificado por uma tarefa, decisão ou informação necessária.
- [ ] O projeto não criou dashboard/CRUD/login apenas para parecer “completo”.
- [ ] Telas/estados estão numerados e navegáveis na documentação.
- [ ] Há pelo menos uma simulação/walkthrough documentado.
- [ ] Críticas não foram apenas listadas: geraram decisão de revisão.
- [ ] O protótipo continua em baixa fidelidade; detalhes visuais não mascaram problemas de fluxo.

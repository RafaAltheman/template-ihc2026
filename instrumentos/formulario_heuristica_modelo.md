
# Formulário de avaliação heurística — modelo

**Avaliador:** Equipe 27 — Letizia Lowatzki Baptistella, Manuella Filipe Peres e Rafaela Altheman de Campos (inspeção estática do protótipo)  
**Versão:** Protótipo da Entrega 11 — Figma IHC, página 0:1, com início em 32:2023  
**Data:** 16/11/2026  
**Estados especiais examinados:** Vazio (P10 e tela 42), erro (telas 33 e 45), filtro sem resultado (P09 e tela 29), confirmação (P06 e telas 07, 09 e 21), comparação com condições não confirmadas (telas 04 e 05). Carregamento e permissões não foram avaliados por não fazerem parte dos estados examinados nesta inspeção.

## Cobertura

| H | Heurística | Fluxos/telas examinados | Violação? | IDs |
|---:|---|---|---|---|
| 1 | Visibilidade do status do sistema | P06 — Confirmar registro; tela 07 — Conferir hipótese registrada; tela 09 — Conferir avaliação registrada; tela 21 — Conferir registro. | não | — |
| 2 | Compatibilidade sistema–mundo real | P01 — Painel geral; P03 — Comparação de execuções; tela 04 — Comparar métricas e parâmetros. | sim | V01 |
| 3 | Controle e liberdade do usuário | Tela 15 — Apresentar indicadores; tela 43 — Observar evidência da execução; tela 45 — Recuperar erro de registro. | não | — |
| 4 | Consistência e padrões | P01 — Painel geral; P03 — Comparação de execuções; tela 04 — Comparar métricas e parâmetros; tela 05 — Verificar comparabilidade. | sim | V01, V02 |
| 5 | Prevenção de erros | P03 — Comparação; tela 05 — Verificar comparabilidade; tela 06 — Registrar hipótese e ressalvas. | sim | V02 |
| 6 | Reconhecimento em vez de memorização | Tela 02 — Localizar treinamento; tela 03 — Selecionar execuções; tela 43 — Observar evidência. | não | — |
| 7 | Flexibilidade e eficiência de uso | Tela 02 — Localizar treinamento; tela 04 — Comparar métricas e parâmetros; telas 15–18 — Apresentar indicadores. | não | — |
| 8 | Estética e design minimalista | P01 — Painel geral; P03 — Comparação; P10 — Painel sem dados do período. | sim | V03 |
| 9 | Reconhecer, diagnosticar e recuperar erros | P09 — Busca sem resultados; tela 29 — Busca sem resultados; tela 33 — Corrigir ou tentar novamente; tela 45 — Recuperar erro de registro. | não | — |
| 10 | Ajuda e documentação | Tela 02 — Localizar treinamento; tela 05 — Verificar comparabilidade; tela 37 — Investigar dado não registrado. | não | — |

**Observação:** "Não" indica que nenhuma violação específica foi confirmada nos elementos examinados durante esta inspeção estática. Não significa que todos os caminhos interativos foram testados ou que o protótipo está livre de problemas.

## Problemas

| ID | H | Tela/estado | Ação/condição | Problema | Consequência | Evidência | Severidade 0–4 | Justificativa | Recomendação |
|---|---|---|---|---|---|---|---:|---|---|
| V01 | 2, 4 | P01 — Painel geral; P03 e tela 04 — Comparação de execuções | Consultar velocidade e comparar EXEC-104 com EXEC-103. | A velocidade é apresentada com unidades inconsistentes entre o painel e a comparação. | Pode causar interpretação incorreta da grandeza física e comprometer conclusões sobre o desempenho do robô. | P01 apresenta "0,32 m/s", enquanto P03 e tela 04 apresentam "0.32 cm/s" para a velocidade de EXEC-104. | 4 | A diferença entre m/s e cm/s altera a interpretação da medida por um fator de 100, podendo comprometer decisões técnicas. | Padronizar as unidades de velocidade, confirmar os valores corretos e utilizar a mesma convenção de apresentação em todas as telas. |
| V02 | 4, 5 | P03 — Comparação de execuções; tela 04 — Comparar métricas e parâmetros; tela 05 — Verificar comparabilidade | Verificar se duas execuções podem ser comparadas de maneira confiável. | O protótipo apresenta uma informação afirmativa sobre ausência de diferenças de configuração em uma tela, enquanto outras indicam condições de treinamento não confirmadas. | O usuário pode considerar as execuções plenamente comparáveis antes de verificar as condições necessárias. | P03: "Diferença de configuração: Nenhuma". Tela 04: "Condições de treinamento: não confirmadas". Tela 05: "Condições não confirmadas". | 3 | A comunicação pode gerar confiança excessiva na comparação, especialmente quando informações de configuração ainda não foram verificadas. | Diferenciar explicitamente "nenhuma diferença identificada" de "condições não verificadas", evitando afirmar equivalência quando faltarem informações. |
| V03 | 8 | P10 — Painel sem dados do período | Consultar um intervalo sem resultados. | A mensagem de estado vazio apresenta erro de escrita. | Reduz o acabamento e a clareza textual da mensagem, embora a recuperação continue compreensível. | P10: "Não há resultados dsponíveis no período escolhido". | 1 | Problema textual de baixo impacto, sem impedir a compreensão geral da mensagem. | Corrigir "dsponíveis" para "disponíveis" e revisar a escrita das mensagens de estado. |

## Prompt: Teste Interativo do Efeito Stroop (Psicologia Cognitiva)

**Objetivo:** Criar uma ferramenta experimental interativa que reproduza o clássico Teste de Stroop, medindo tempo de reação e taxa de erro do usuário em condições congruentes e incongruentes, para demonstrar na prática o fenômeno de interferência cognitiva estudado em neurociência e psicologia cognitiva.

**Prompt:**

```
Atue como um(a) neurocientista e pesquisador(a) de psicologia cognitiva. Crie um teste interativo do Efeito Stroop onde o usuário responde à cor das palavras exibidas. No final, calcule o tempo médio de reação e a taxa de erro para condições congruentes vs. incongruentes.
```


**Por que funciona:**
- **Atribuição de persona (neurocientista e pesquisador de psicologia cognitiva):** ancora o tom experimental/científico da resposta, garantindo que o modelo trate o teste como um instrumento de pesquisa real (com rigor metodológico), e não apenas como um jogo casual.
- **Referência a um paradigma nomeado (Efeito Stroop):** funciona como âncora conceitual — o modelo já conhece a lógica clássica do experimento (palavras de cores exibidas em tintas congruentes ou incongruentes com seu significado), dispensando a necessidade de explicar manualmente a mecânica do teste.
- **Definição clara da interação esperada (usuário responde à cor, não à palavra):** elimina a ambiguidade mais comum na implementação do Stroop, que é confundir "responder o que está escrito" com "responder a cor da tinta" — justamente o cerne do efeito a ser medido.
- **Especificação das métricas de saída (tempo médio de reação e taxa de erro):** transforma o teste de uma simples atividade interativa em um instrumento de coleta de dados quantitativos, exigindo que o modelo implemente cronometragem por resposta e contabilização de acertos/erros.
- **Distinção explícita entre condições (congruentes vs. incongruentes):** obriga o modelo a estruturar o experimento com dois grupos de estímulos comparáveis, permitindo a análise estatística que é o objetivo científico central do paradigma Stroop.
- **Abertura proposital (sem especificar tecnologia/formato de saída):** dá liberdade para o modelo escolher a melhor implementação (HTML/JS com temporizador via `Date.now()` ou `performance.now()`, por exemplo), servindo como prompt-base a ser refinado depois com requisitos técnicos específicos, como no exemplo da enquete interativa.
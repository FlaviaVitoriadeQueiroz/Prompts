## Prompt: Simulador de Genética de Populações (Equilíbrio de Hardy-Weinberg)

**Objetivo:** Criar uma ferramenta educacional interativa que permita visualizar, na prática, como frequências alélicas e genotípicas se comportam em uma população ao longo de gerações — tanto em equilíbrio quanto sob efeito de pressões seletivas — facilitando o ensino do Princípio de Hardy-Weinberg em genética de populações.

**Prompt:**

```
Atue como um(a) geneticista e professor(a) universitário(a). Crie um modelo interativo de genética de populações baseado no Princípio de Hardy-Weinberg. O usuário ajusta as frequências alélicas iniciais (p e q) e aplica variáveis de seleção natural para observar as mudanças genotípicas ao longo das gerações.
```

**Por que funciona:**
- **Atribuição de persona (geneticista e professor universitário):** ancora o tom e o nível técnico da resposta, garantindo terminologia científica correta (alelos, loci, genótipos, frequências) e ao mesmo tempo uma postura didática, adequada para fins de ensino.
- **Referência a um framework teórico nomeado (Hardy-Weinberg):** funciona como uma "âncora conceitual" — o modelo já sabe exatamente quais fórmulas aplicar (p² + 2pq + q² = 1) sem precisar que o usuário as descreva manualmente, reduzindo erros e aumentando a precisão científica do resultado.
- **Definição clara das variáveis de entrada (p e q):** delimita a interface interativa esperada, indicando que o usuário deve poder manipular os parâmetros iniciais e não apenas visualizar dados estáticos.
- **Inclusão de "variáveis de seleção natural":** eleva a simulação além do equilíbrio teórico puro, permitindo demonstrar desequilíbrio genético (seleção, deriva, migração) — o que é pedagogicamente mais rico, pois mostra tanto a regra quanto suas exceções.
- **Ênfase em "mudanças ao longo das gerações":** sinaliza que a saída não deve ser um cálculo único e estático, mas sim uma simulação iterativa/temporal (ex: gráfico de linha, animação por gerações), o que é essencial para visualizar dinâmica evolutiva.
- **Abertura proposital (sem especificar tecnologia/formato de saída):** dá liberdade para o modelo escolher a melhor representação (interativa em HTML/JS, gráfico, tabela), sendo ideal como prompt-base a ser refinado depois com requisitos técnicos específicos, como no exemplo da enquete.
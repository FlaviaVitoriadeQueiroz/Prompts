## Prompt: Visualizador Interativo de QuickSort (Algoritmos e Estruturas de Dados)

**Objetivo:** Criar uma ferramenta educacional interativa que demonstre visualmente o funcionamento interno do algoritmo QuickSort — escolha de pivô, partição e trocas — permitindo ao usuário controlar o tamanho da entrada e avançar a execução passo a passo, facilitando o ensino de algoritmos de ordenação e análise de complexidade.

**Prompt:**

```
Atue como um(a) professor(a) de algoritmos e estruturas de dados. Crie um visualizador interativo para o algoritmo de ordenação QuickSort. O usuário deve poder definir o tamanho do vetor inicial e avançar passo a passo para observar os pivôs e as trocas de posição.
```


**Por que funciona:**
- **Atribuição de persona (professor de algoritmos e estruturas de dados):** direciona o tom didático e garante rigor técnico na implementação do algoritmo (complexidade, casos de pior/melhor caso, nomenclatura correta de pivô, partição, recursão).
- **Referência a um algoritmo nomeado (QuickSort):** funciona como âncora conceitual — o modelo já conhece a lógica exata a ser implementada (escolha de pivô, particionamento, recursão em subvetores), eliminando a necessidade de descrever pseudocódigo manualmente.
- **Definição da entrada controlável pelo usuário (tamanho do vetor):** delimita a interface interativa esperada, indicando que a visualização deve ser generativa/parametrizável e não um exemplo fixo e estático.
- **Ênfase em "avançar passo a passo":** sinaliza que a saída não deve ser uma execução instantânea do algoritmo, mas sim uma simulação controlada (com botões de "próximo passo"/"anterior"), essencial para fins pedagógicos onde o aluno precisa acompanhar cada decisão do algoritmo no seu próprio ritmo.
- **Especificar os elementos visuais-chave a destacar (pivôs e trocas de posição):** guia o modelo a criar indicadores visuais claros (cores, destaques) para essas duas operações centrais do QuickSort, que são justamente os pontos de maior confusão para estudantes iniciantes.
- **Abertura proposital (sem especificar tecnologia/formato de saída):** permite que o modelo escolha a melhor representação (barras animadas em HTML/JS/Canvas, por exemplo), servindo como prompt-base a ser refinado depois com requisitos técnicos específicos, como no exemplo da enquete interativa.
## Prompt: Análise Comparativa Teoria x Prática (Paper x Study Notebook)

**Objetivo:** Cruzar um artigo acadêmico com um notebook de código Python correspondente, gerando uma matriz de alinhamento entre o que foi proposto teoricamente e o que foi de fato implementado — expondo divergências, simplificações e lacunas metodológicas, com rastreabilidade obrigatória para cada afirmação (página/parágrafo do artigo e célula/linha do notebook).

**Prompt:**

```
Atue como um Especialista Sênior e Revisor Acadêmico em Ciência de Dados e Machine Learning. Seu objetivo é guiar um estudante na transição entre a fundamentação teórica de artigos acadêmicos e a experimentação prática em código Python (via Study Notebooks).

Analise os arquivos fornecidos ([Artigo/Fonte A] e [Notebook/Fonte B]) e execute as seguintes etapas:

1. Matriz de Alinhamento Teoria-Prática
Construa uma tabela em Markdown comparando ambas as fontes com as seguintes colunas:
- [Pipeline / Algoritmo Proposto]
- [Bibliotecas & Estruturas de Dados em Python Utilizadas] (ex: NumPy, Pandas, Scikit-learn, PyTorch)
- [Hipóteses Teóricas vs. Implementação Prática]
- [Tratamento de Dados & Limitações Empíricas] (ex: data leakage, viés de amostragem, escalabilidade O(n))
- [Métricas de Avaliação & Performance Declarada] (ex: F1-Score, RMSE, AUC-ROC, tempo de treino)

2. Mapeamento de Divergências, Discrepâncias de Código e Trade-offs
Abaixo da tabela, crie uma seção destacando expressamente:
- Onde o código no Notebook diverge da teoria descrita no Paper (ex: hiperparâmetros fixados de forma diferente, simplificação de funções de perda, pré-processamento ausente).
- Onde os resultados experimentais em Python contradizem as alegações teóricas da publicação.

3. Veredito Metodológico, Boas Práticas em Python & Lacunas
Resuma em 1 parágrafo:
- A solidez da reprodutibilidade computacional do pipeline em Python.
- Quais boas práticas de engenharia/ciência de dados foram violadas ou deixadas em aberto (ex: falta de validação cruzada estratificada, ausência de testes de significância estatística, sementes aleatórias desreguladas).

Regras estritas de execução (Grounding & Rastreabilidade de Código/Texto):
- Rastreabilidade Obrigatória: Para o artigo, cite o número exato da página e parágrafo: [Artigo A, Pág. X, Parágrafo Y]. Para o Notebook, cite a célula de código/markdown e a linha de código: [Notebook B, Célula In[Z], Linhas W-K].
- Tratamento de Dados Ausentes: Se a fonte/notebook não trouxer explicitamente algum dado (ex: sem menção ao random_state ou métrica de convergência), preencha estritamente com "dado/código não informado explicitamente na fonte". NÃO deduza parâmetros ocultos.
- Zero Conhecimento Prévio: Baseie sua análise estritamente nos artefatos anexados (Paper + Notebook).
```

**Por que funciona:**
- **Persona ("Especialista Sênior e Revisor Acadêmico")** eleva o padrão de rigor da resposta, ancorando o modelo em um papel que naturalmente exige citação de fontes e ceticismo metodológico, em vez de uma resposta genérica de "resumo de leitura".
- **Estrutura em etapas numeradas (1, 2, 3)** força o raciocínio a seguir uma progressão lógica: primeiro mapear (matriz), depois comparar (divergências) e só então julgar (veredito) — evitando que o modelo pule direto para uma opinião sem evidência.
- **Colunas fixas na matriz** obrigam a análise a cobrir tanto o aspecto teórico (hipóteses, métricas declaradas) quanto o aspecto de engenharia (bibliotecas, estruturas de dados, limitações empíricas), que costumam ser tratados separadamente por estudantes.
- **Seção dedicada a divergências** existe porque comparações costumam gerar apenas semelhanças; pedir explicitamente por onde teoria e prática se afastam é o que gera o real valor de aprendizado (é onde estão os erros comuns e as simplificações do mundo real).
- **Rastreabilidade obrigatória (página/parágrafo e célula/linha)** transforma a saída em algo auditável — o estudante pode verificar cada afirmação na fonte original, o que reduz alucinação e aumenta a confiança no material gerado.
- **Regra de "dado não informado explicitamente"** é uma salvaguarda anti-alucinação: impede que o modelo preencha lacunas (como `random_state` não citado) com suposições plausíveis, mas falsas.
- **"Zero Conhecimento Prévio"** restringe o modelo a usar apenas os artefatos anexados, evitando que conhecimento genérico de treinamento se misture com o conteúdo específico das fontes fornecidas — essencial para um exercício de estudo fiel ao material.
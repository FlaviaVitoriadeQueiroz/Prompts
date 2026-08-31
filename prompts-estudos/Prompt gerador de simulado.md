## Prompt: Gerador de Questões de Prova / Desafios Técnicos (Cenários Reais de Data Science)

**Objetivo:** Transformar notas de estudo, trechos de notebooks e papers anexados em questões de prova multipartes, baseadas em cenários reais de engenharia e modelagem de dados, exigindo síntese cruzada entre conceitos e vindo acompanhadas de gabarito comentado e rubrica de correção.

**Prompt:**

```
Atue como um Professor e Avaliador Técnico Sênior em Ciência de Dados aplicada com Python.

Analise todas as notas de estudo, trechos de notebooks e papers anexados e gere 3 Questões de Prova / Desafios Técnicos baseados em cenários reais de engenharia e modelagem de dados.

Critérios obrigatórios para as questões:

1. Cenário Realista: Cada questão deve apresentar um problema prático de Ciência de Dados (ex: degradação de métricas em produção, debugging de pipeline de pré-processamento no Pandas, sobreajuste/overfitting em modelos Scikit-learn/PyTorch, vazamento de dados em séries temporais).

2. Estrutura Multipartes & Síntese Cruzada: Cada questão deve conter pelo menos 3 subitens (a, b, c) e exigir obrigatoriamente a combinação de pelo menos DOIS conceitos distintos das notas (ex: Álgebra Linear/Cálculo do Paper + Otimização de Código Vetorizado em NumPy; ou Seleção de Features + Interpretação de SHAP Values).

3. Gabarito Detalhado & Rubrica de Correção:
   - Resposta esperada comentada com os trechos exatos de código Python (quando aplicável).
   - Justificativa teórica com citações precisas das fontes enviadas ([Paper, Pág. X] ou [Notebook, Célula Y]).
   - Critérios para Crédito Parcial (Rubrica detalhando pontuações para respostas corretas, semi-corretas ou com erros comuns de implementação/lógica).
```

**Por que funciona:**
- **Persona ("Professor e Avaliador Técnico Sênior")** direciona o modelo para o modo "avaliação", que naturalmente exige rigor, objetividade e critérios de correção — diferente do modo "explicação", que tende a ser mais permissivo e menos estruturado.
- **Cenário Realista como critério obrigatório** evita questões abstratas de "decoreba" (ex: "defina overfitting") e força o modelo a ancorar cada questão em um problema que o estudante encontraria de fato no dia a dia (produção, debugging, pipelines), aumentando a transferência do aprendizado para a prática.
- **Estrutura multipartes (a, b, c)** simula o formato de prova real e quebra um problema complexo em etapas progressivas — geralmente diagnóstico, correção/implementação e justificativa — o que também facilita a correção parcial.
- **Exigência de síntese cruzada entre dois conceitos distintos** é o núcleo pedagógico do prompt: impede que a IA gere questões triviais de "conceito isolado" e obriga o estudante a conectar teoria (ex: fundamentos matemáticos do paper) com prática de código (ex: vetorização em NumPy, interpretabilidade com SHAP), que é exatamente a lacuna que motivou o uso do Study Notebook.
- **Gabarito com trechos exatos de código** transforma a questão em algo autoexplicativo e verificável — o estudante não precisa confiar cegamente na resposta, pode rodar o código e comparar o resultado.
- **Citações precisas das fontes ([Paper, Pág. X] / [Notebook, Célula Y])** mantém a mesma exigência de rastreabilidade do prompt de análise comparativa, evitando que o gabarito "invente" teoria não presente no material de estudo.
- **Rubrica de crédito parcial** transforma o prompt em uma ferramenta de autoavaliação real: em vez de um simples "certo/errado", o estudante consegue identificar exatamente que tipo de erro cometeu (conceitual, de implementação ou de interpretação), o que é mais próximo de como avaliações técnicas sérias são corrigidas.
## Prompt: Simulador Interativo de Perceptron Artificial

**Objetivo:** gerar uma aplicação web interativa e didática (HTML/CSS/JS em arquivo único) que simule visualmente o funcionamento de um Perceptron simples, servindo como material de estudo para a disciplina de Redes Neurais.

**Prompt:**
```
Atue como um especialista em Machine Learning e desenvolvimento Web frontend. Crie no Canvas uma aplicação interativa completa (em um único arquivo HTML contendo CSS e JavaScript) que simule e explique o funcionamento de um Neurônio Artificial Perceptron simples.

A aplicação deve conter:

1. Interface Visual (Diagrama Interativo do Perceptron):
   - Entradas visíveis: x1, x2 e o Bias (b = 1).
   - Sliders ou campos de entrada para ajustar os valores de entrada e os respectivos pesos sinápticos (w1, w2 e w_bias).
   - Um nó central (soma ponderada) exibindo a fórmula: z = (x1 * w1) + (x2 * w2) + w_bias.
   - Uma representação da Função de Ativação (com seletor para escolher entre: Degrau/Step Function, Sigmoide e ReLU).
   - O nó de Saída (y), destacando o resultado final de acordo com a função escolhida.

2. Visualização Gráfica do Espaço de Decisão (Canvas/Chart 2D):
   - Um gráfico cartesiano 2D simples mostrando os eixos x1 e x2.
   - A linha de decisão geométrica traçada dinamicamente baseada nos pesos atuais: (w1*x1 + w2*x2 + w_bias = 0).
   - O ponto correspondente às entradas atuais marcado no gráfico, mostrando em qual classe ele se encontra.

3. Seção Prática de Aprendizado (Exemplo Lógico):
   - Botões pré-definidos para carregar problemas clássicos de portas lógicas (AND, OR).
   - Um botão "Treinar Perceptron (Epochs)" simples que execute o algoritmo de aprendizado supervisionado (Regra do Perceptron com taxa de aprendizado ajustável) para ajustar os pesos automaticamente até convergir.

4. Design e Usabilidade:
   - Layout moderno, limpo, responsivo e intuitivo (estilo dashboard educacional com Tailwind CSS via CDN).
   - Código bem comentado explicando a matemática por trás da soma ponderada, ativação e atualização de pesos.
```

**Por que funciona:**
- **Papel especializado definido ("especialista em ML e frontend"):** direciona o tom técnico e a qualidade do código esperado, evitando explicações simplistas demais ou implementações rasas.
- **Divisão em quatro blocos numerados e bem delimitados:** separa claramente interface do diagrama, visualização gráfica, prática de treinamento e design, o que evita que a IA misture ou omita alguma dessas partes ao gerar uma aplicação complexa.
- **Fórmulas matemáticas explicitadas no próprio prompt** (soma ponderada, equação da linha de decisão): elimina ambiguidade sobre qual cálculo deve ser implementado, garantindo que o resultado seja matematicamente correto, não apenas visualmente bonito.
- **Especificação de tecnologia (arquivo único HTML/CSS/JS, Tailwind via CDN):** evita que a IA gere múltiplos arquivos ou dependências complexas de instalação, já que o objetivo é rodar direto no navegador, sem setup.
- **Casos de uso prontos (portas lógicas AND/OR) e botão de treinamento automático:** transforma a aplicação de um simples "diagrama estático" em uma ferramenta prática de experimentação, essencial para realmente entender como os pesos convergem durante o aprendizado supervisionado.
- **Pedido explícito de comentários explicando a matemática no código:** garante que o material sirva não só como ferramenta visual, mas também como material de estudo do próprio código-fonte, reforçando o aprendizado dos conceitos da disciplina de Redes Neurais.
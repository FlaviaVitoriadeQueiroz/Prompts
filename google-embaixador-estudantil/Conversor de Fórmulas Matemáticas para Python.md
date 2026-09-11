## Prompt: Conversor de Fórmulas Matemáticas para Python (FórmulaPy)

**Objetivo:** Gerar, via Gemini Canvas, uma interface web funcional que converte fórmulas matemáticas digitadas pelo usuário em código Python, com sistema de favoritos, salvamento de fórmulas nomeadas e uma biblioteca de fórmulas comuns pré-carregadas.

**Prompt:**

'''
Crie uma interface web (HTML, CSS e JavaScript) chamada "FórmulaPy" — um conversor de fórmulas matemáticas para código Python. A interface deve ter as seguintes funcionalidades:

1. Campo de entrada de fórmulas

Um campo de texto onde o usuário digita uma fórmula matemática (ex: x^2 + 2x - 5, (a+b)/c, área do círculo π*r^2)
Um botão "Converter" que gera o código Python equivalente (como função, com nome de variáveis claro)
Exibir o código gerado em um bloco com syntax highlighting e botão de "copiar código"

2. Sistema de favoritos

Botão de estrela/coração ao lado de cada fórmula convertida para marcar como favorita
Uma aba ou seção "Favoritos" listando todas as fórmulas marcadas, com acesso rápido para reutilizá-las

3. Salvar fórmulas com nome personalizado

Ao converter uma fórmula, permitir salvá-la com um nome escolhido pelo usuário (ex: "Bhaskara", "Juros compostos")
Lista de "Minhas fórmulas salvas" com busca/filtro por nome
Opção de editar o nome ou excluir fórmulas salvas

4. Biblioteca de fórmulas comuns (pré-carregadas)
Inclua uma seção "Fórmulas Populares" já vindo pronta com pelo menos estas categorias e exemplos:

Álgebra: Bhaskara, área do triângulo, área do círculo, perímetro
Física: velocidade média, força (F=ma), energia cinética
Estatística: média, desvio padrão, variância
Matemática financeira: juros simples, juros compostos
Cada fórmula popular deve já vir com seu código Python pronto e um botão "usar essa fórmula" que a leva para o campo de conversão/edição.

5. Persistência de dados

Salvar os favoritos e fórmulas personalizadas do usuário localmente, para que não se percam ao recarregar a página

6. Design

Interface limpa, moderna, com boa organização visual entre as três áreas (conversor, favoritos, fórmulas populares)
Cores agradáveis, responsivo para uso em celular
Ícones intuitivos (estrela para favoritar, lápis para editar, lixeira para excluir)

Gere o código completo funcional dessa interface.
'''


**Por que funciona:**
- **Divisão em seções numeradas** força o modelo a tratar cada funcionalidade como um requisito independente, reduzindo o risco de ele esquecer alguma parte (ex: implementar só o conversor e ignorar os favoritos).
- **Placeholders entre colchetes** (nome do app, exemplos de fórmulas, categorias) tornam o prompt reutilizável para outros domínios além de matemática — basta trocar os exemplos.
- **Especificar "syntax highlighting" e "botão de copiar código"** evita que o resultado venha como texto puro, já pensando na usabilidade real de quem for copiar o código gerado.
- **Pedir persistência de dados explicitamente** garante que o modelo não gere um protótipo que perde tudo ao recarregar a página — comum quando essa instrução não é dada.
- **Seção de design no final** direciona o modelo a pensar em UX/UI depois da lógica funcional, evitando que ele gaste o "orçamento" de resposta só na parte técnica e entregue uma interface feia ou confusa.
- **Fechar com "gere o código completo funcional"** deixa claro que se espera uma entrega pronta para uso, não um esboço ou pseudo-código.

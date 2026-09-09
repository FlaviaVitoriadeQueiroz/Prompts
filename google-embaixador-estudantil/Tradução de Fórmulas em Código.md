## Prompt: Tradução de Fórmulas em Código

**Objetivo:** transformar uma fórmula ou cálculo matemático em uma representação visual que conecte os termos matemáticos às suas implementações em código, facilitando a compreensão da relação entre matemática, estruturas de dados e programação.

**Prompt:**

```svg id="p6x9rw"
Quero transformar a seguinte fórmula/cálculo em um esquema visual interativo que traduza cada termo matemático em código:

[COLE AQUI A FÓRMULA OU CÁLCULO]

Contexto/linguagem de programação:
[EX: PYTHON COM NUMPY / JAVASCRIPT / PSEUDOCÓDIGO]

Antes de gerar o visual, explique brevemente cada termo da fórmula em palavras simples, indicando:
- o que o símbolo representa;
- qual é sua função no cálculo;
- qual estrutura de dado ele representa, como escalar, vetor, matriz ou função;
- como esse termo pode ser representado no código.

Depois, crie um diagrama que combine:

1. SEQUÊNCIA (FLUXOGRAMA):
Quebre a fórmula em etapas, mostrando a ordem em que os cálculos precisam ser realizados e o que depende de cada etapa.

2. CORRESPONDÊNCIA (DIAGRAMA):
Para cada etapa, mostre lado a lado:
- o termo matemático;
- o significado do termo;
- o código equivalente que o implementa.

3. DEPENDÊNCIA ENTRE ETAPAS:
Deixe visível que a saída de uma etapa alimenta a entrada da próxima, tanto no lado matemático quanto no lado do código.

4. EXEMPLO PRÁTICO:
Se eu fornecer valores concretos, utilize-os para demonstrar como os valores percorrem cada etapa do cálculo e como aparecem no código.

5. REVISÃO:
Verifique se todos os termos da fórmula foram representados e se existe correspondência clara entre a expressão matemática, as etapas do cálculo e o código.

Se a fórmula for muito grande ou complexa, como no caso de um processo completo de backpropagation, divida a representação em mais de um diagrama para evitar excesso de informações em uma única visualização.

Não gere o visual antes de explicar os termos da fórmula.
```

**Como usar:**

* Cole qualquer fórmula que esteja estudando, como fórmulas de redes neurais, estatística, álgebra, física ou outras áreas.
* Informe a linguagem de programação que deseja utilizar.
* Se quiser trabalhar com valores concretos, adicione exemplos como: "[USE X = 10 E Y = 5 COMO EXEMPLO]".
* Para fórmulas muito extensas, peça que o conteúdo seja dividido em mais de um diagrama.

**Por que funciona:** o prompt cria uma ponte entre três formas de representação: **matemática, lógica de cálculo e código**. A identificação das estruturas de dados ajuda a compreender o papel de cada termo, enquanto o fluxograma evidencia a sequência e as dependências. A correspondência lado a lado permite visualizar como uma expressão matemática é transformada em instruções de programação, tornando conceitos abstratos mais concretos.

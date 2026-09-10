## Prompt: Revisor Acadêmico Sênior (Análise Comparativa de Literatura)

**Objetivo:** Realizar uma análise comparativa rigorosa e rastreável entre duas fontes acadêmicas, produzindo uma matriz estruturada, um mapeamento de contradições e um veredito de solidez metodológica — com controles anti-alucinação que forçam citação exata de página/parágrafo e proíbem inferências não fundamentadas nos documentos.

**Prompt:**

```
Atue como um revisor acadêmico sênior focado em análise rigorosa de literatura. Analise os arquivos [Fonte A] e [Fonte B] fornecidos e execute as seguintes etapas:

Matriz Comparativa Estruturada
Construa uma tabela em Markdown comparando ambas as fontes com as seguintes colunas: [Metodologia] [Premissas Teóricas] [Limitações Empíricas] [Taxa de Convergência Declarada]
Mapeamento de divergências e contradições
Abaixo da tabela, crie uma seção destacando expressamente onde os dois estudos se contradizem ou chegam a conclusões opostas sobre o mesmo fenômeno.
Veredito acadêmico & lacunas
Resuma em 1 parágrafo qual das duas abordagens apresenta maior solidez metodológica e qual lacuna de pesquisa ainda permanece em aberto.

Regras estritas de execução (grounding & citação):

Rastreabilidade obrigatória: toda e qualquer informação extraída DEVE vir acompanhada do número exato da página e do parágrafo entre colchetes. Exemplo: [Fonte A, Pág. 12, Parágrafo 3].
Tratamento de dados ausentes: se a fonte não mencionar explicitamente algum dos critérios da tabela (como a Taxa de Convergência), preencha o campo estritamente com "dado não informado explicitamente na fonte". NÃO deduza ou infira dados.
Zero conhecimento prévio: Limite-se estritamente às informações contidas nos documentos anexados. Não utilize dados externos à sua base de treinamento.
```


**Por que funciona:**
- **Atribuição de persona (revisor acadêmico sênior):** eleva o padrão de rigor esperado na resposta, ativando um "modo crítico" em vez de um resumo superficial ou complacente das fontes.
- **Estrutura em etapas numeradas (matriz → divergências → veredito):** impõe uma ordem lógica de raciocínio — primeiro extrair, depois comparar, só então julgar — evitando que o modelo pule direto para conclusões sem base extrativa.
- **Colunas pré-definidas na matriz:** elimina a ambiguidade sobre quais critérios comparar, garantindo que a comparação seja simétrica e não apenas um resumo livre de cada fonte.
- **Seção dedicada a contradições:** força o modelo a fazer contraste ativo entre as fontes (não apenas listar diferenças passivamente), que é o valor analítico central de uma revisão de literatura.
- **Veredito limitado a 1 parágrafo:** evita divagação e obriga síntese — o modelo precisa priorizar o que realmente importa (solidez metodológica + lacuna de pesquisa) em vez de repetir a tabela em prosa.
- **Rastreabilidade obrigatória (página + parágrafo):** é o controle mais crítico do prompt — transforma cada afirmação em uma alegação verificável, reduzindo drasticamente o risco de alucinação e permitindo auditoria humana rápida.
- **Regra de dados ausentes com frase padronizada:** impede que o modelo "invente" valores plausíveis para preencher lacunas na tabela — um dos erros mais comuns e perigosos em análises acadêmicas geradas por IA, substituindo a tentação de inferir por uma resposta padronizada e segura.
- **Regra de "zero conhecimento prévio":** restringe o modelo à base fornecida, evitando contaminação por conhecimento genérico do treinamento que poderia ser impreciso, desatualizado ou simplesmente não pertencente às fontes analisadas — essencial para revisões que exigem fidelidade estrita ao corpus.
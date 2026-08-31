## Prompt: Plano de estudos personalizado (Desafio #01 — Auditoria de Prompt)

**Objetivo:** transformar um pedido genérico de plano de estudos em um prompt específico e acionável, eliminando as suposições que a IA precisaria fazer sozinha.

**Contexto do desafio:** o cenário original propunha um estudante com prova chegando que manda para o Gemini: "Tenho uma prova na sexta-feira. Monte um plano de estudos para mim." O problema é que o Gemini teria que "chutar" quase tudo, e provavelmente devolveria um plano padrão e raso.

**Prompt:**
```
Tenho uma prova de [matéria/assunto] na sexta-feira. Tenho [X horas por dia] disponíveis até lá. Tenho mais dificuldade em [tópico A] e mais facilidade em [tópico B]. A prova é [formato: dissertativa/múltipla escolha/com consulta]. Prefiro estudar fazendo [exercícios/resumos/flashcards]. Monte um plano de estudos, em PDF, dia a dia até a prova.
```

**Por que funciona:**
O prompt original era extremamente raso — o Gemini teria que chutar quase tudo e devolveria algo padrão e genérico. Cada critério adicionado resolve um tipo específico de suposição que a IA teria que fazer sozinha (e provavelmente erraria):

- **Tempo disponível:** sem isso definido, a IA não tem como dimensionar o plano; ela não conseguiria trabalhar com precisão.
- **Matéria e assunto específico:** é a parte principal de toda a elaboração do plano de estudo; sem isso, não há como gerar uma resposta de verdade.
- **Facilidade e dificuldade:** resolve a questão da priorização, tornando o plano muito mais assertivo e personalizado para o usuário.
- **Formato da prova:** implica diretamente na estratégia de estudo, que muda em relação ao formato e ao conteúdo da prova.
- **Maneira preferida de estudar:** afeta a probabilidade de o usuário seguir o plano de estudos e ter um bom desempenho na prova.

Em suma: tempo define escala, assunto define conteúdo, dificuldade define prioridade, formato define estratégia, e estilo define adesão. Juntos, esses critérios cobrem as perguntas que qualquer bom professor ou tutor faria antes de ajudar alguém a estudar.
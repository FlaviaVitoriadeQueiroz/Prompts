## Prompt: Enquete Interativa "Cabo de Guerra" (Google Sheets + Canvas HTML)

**Objetivo:** Gerar um painel visual único em HTML, sem backend, que transforma respostas coletadas em um Google Forms/Sheets em uma enquete estilo "cabo de guerra" em tempo real (atualização manual), exibindo placar, barra de progresso animada e últimos votantes — ideal para exibição em telas, lives ou eventos.

**Prompt:**

```svg id="v7k3px"
Crie uma aplicação web interativa em um único arquivo HTML (usando Tailwind CSS via CDN e JavaScript puro) para exibir um painel visual de uma enquete no estilo "Cabo de Guerra", sem scroll vertical e ocupando 100% da tela (100vh).

A enquete compara a opção [TEMA CLARO] contra a opção [TEMA ESCURO] e sua atualização deve ser somente manual. No topo da tela, exiba o título [ENQUETE INTERATIVA: TEMA CLARO VS TEMA ESCURO] e o total de votos. No centro, mostre o placar com porcentagens (1 casa decimal) e votos totais de cada lado. Logo abaixo, inclua uma barra horizontal em glassmorphism com um nó central contendo o ícone [❓] que desliza suavemente de 0% a 100% de acordo com a proporção das opções. Abaixo da barra, exiba duas colunas mostrando os 5 últimos votantes de cada lado (com nickname e horário). A fonte de dados virá da variável let csvUrl ="[LINK DA PLANILHA COMPARTILHADA COMO .CSV]".

Crie uma função que aceite links publicados na Web como valores separados por vírgula (.csv) do Google Sheets (contendo /pub?output=csv ou /export?format=csv), com aviso caso de erro do link. Os dados de horário vem da coluna A, o nickname da coluna B e o voto da coluna C.

No rodapé, exiba o horário da última atualização, o número de linhas lidas no CSV, um botão "Atualizar Já" em destaque com efeito de rotação que dispara a atualização manual sem cache (?t=Date.now()).
```


**Por que funciona:**
- **Arquivo único (HTML + Tailwind CDN + JS puro):** elimina dependência de build/deploy, permitindo abrir o painel direto no navegador ou hospedar em qualquer lugar (ex: OBS Browser Source em lives).
- **Placeholders entre colchetes (`[TEMA CLARO]`, `[LINK DA PLANILHA]` etc.):** tornam o prompt reutilizável para qualquer enquete binária, sem precisar reescrever a lógica a cada uso.
- **Especificação de "100vh sem scroll":** força um layout de painel/dashboard fixo, evitando que elementos "vazem" da tela — essencial para exibições públicas ou telões.
- **Definição explícita das colunas do CSV (A=horário, B=nickname, C=voto):** remove ambiguidade na hora do modelo escrever a função de parsing, já que planilhas do Google Forms sempre seguem essa ordem previsível.
- **Aceitar tanto `/pub?output=csv` quanto `/export?format=csv`:** cobre os dois formatos mais comuns de exportação do Google Sheets, tornando a função mais robusta a variações de como o usuário compartilha o link.
- **Atualização manual com `?t=Date.now()`:** resolve um problema técnico comum (cache do navegador/CDN em requisições CSV), garantindo que o botão sempre traga dados frescos.
- **Pedir aviso de erro no link:** antecipa falha de usuário (link não publicado corretamente) e transforma isso em feedback visível, evitando uma tela em branco sem explicação.
- **Detalhamento visual (glassmorphism, nó central com ícone, animação suave, 1 casa decimal):** reduz a variabilidade estética do resultado, guiando o modelo para um visual "premium" e consistente em vez de um placar genérico.
## Prompt: Painel de Produtividade Acadêmica (Checklist + Resumos + Notas + Prazos)

**Objetivo:** Criar uma aplicação interativa completa no Canvas do Gemini para gestão de vida acadêmica, unificando em um só lugar: checklist dinâmico de tarefas com status de progresso, um módulo de resumo de documentos (PDF/PPTX/DOCX), um sistema de controle de notas por matéria com cálculo automático de médias (por matéria e geral do curso), e um calendário de prazos de entrega com alertas — eliminando a necessidade de múltiplas ferramentas separadas.

**Prompt:**

'''
Atue como um(a) desenvolvedor(a) de aplicações educacionais. Crie uma aplicação web interativa completa (dashboard acadêmico pessoal) com as seguintes 4 abas/seções, navegáveis por um menu superior ou lateral:

ABA 1 — CHECKLIST DE TAREFAS

Permita adicionar novas tarefas a qualquer momento, com campo para: nome da tarefa, matéria/disciplina relacionada e data de entrega (opcional).
Cada tarefa deve ter um status selecionável: "Não iniciada", "Em andamento" ou "Concluída", com cores distintas para cada status (ex: cinza, amarelo, verde).
Permita remover tarefas individualmente.
Permita editar o status de uma tarefa a qualquer momento (ex: clicando ou usando um menu suspenso).
Exiba um contador/resumo no topo da aba (ex: "3 não iniciadas, 2 em andamento, 5 concluídas").

ABA 2 — RESUMO DE DOCUMENTOS

Crie uma área onde o usuário possa colar o conteúdo de um texto, PDF, PowerPoint ou Word (via texto colado, já que não há upload de arquivo real neste ambiente) e receber um resumo estruturado do conteúdo.
O resumo deve ser organizado em tópicos principais, com opção de resumo "curto" ou "detalhado" (o usuário escolhe).
Mantenha um histórico dos resumos já gerados nessa sessão, com título editável para cada um, para consulta posterior.

ABA 3 — CONTROLE DE NOTAS E MÉDIAS

Permita cadastrar matérias do curso.
Para cada matéria, permita adicionar múltiplos trabalhos/avaliações com nome e nota (0 a 10).
Calcule e exiba automaticamente a média de cada matéria.
Calcule e exiba a média geral do curso (média de todas as matérias).
Exiba tudo isso em formato de tabela ou cards, organizados por matéria, com a média geral em destaque no topo da aba.

ABA 4 — PRAZOS E ALERTAS

Liste automaticamente todas as tarefas da Aba 1 que possuem data de entrega, ordenadas por proximidade da data.
Destaque visualmente (ex: cor vermelha ou ícone de alerta) qualquer tarefa cuja data de entrega seja HOJE.
Destaque também tarefas com prazo vencido (data de entrega já passou e status ainda não é "Concluída").

REQUISITOS GERAIS:

Todos os dados devem persistir durante a sessão de uso (o usuário pode adicionar/remover itens livremente em qualquer aba, a qualquer momento).
Interface limpa, organizada e responsiva, com boa hierarquia visual entre as 4 abas.
Use cores consistentes para os status de tarefas em todas as abas onde eles aparecerem (ex: a aba de prazos deve usar as mesmas cores de status da aba de checklist).
'''


**Por que funciona:**
- **Divisão em abas numeradas e nomeadas:** transforma um pedido amplo e multifuncional em módulos independentes e bem delimitados, evitando que o modelo misture funcionalidades distintas em uma única interface confusa.
- **Especificação dos 3 estados de tarefa com cores fixas:** elimina ambiguidade sobre como representar progresso, e a reutilização das mesmas cores entre abas (checklist e prazos) cria consistência visual, facilitando a leitura rápida do usuário.
- **Ações explícitas de "adicionar a qualquer momento" e "remover":** garante que a aplicação seja tratada como uma ferramenta viva de uso contínuo (CRUD completo), e não uma lista estática gerada uma única vez.
- **Adaptação realista para resumos (colar texto em vez de upload real):** antecipa uma limitação técnica do ambiente Canvas (que normalmente não processa upload real de arquivos binários como PDF/DOCX), evitando que o modelo prometa uma funcionalidade que não pode entregar de fato.
- **Opção de resumo "curto" ou "detalhado":** dá controle ao usuário sobre a profundidade da síntese, já que nem todo material acadêmico exige o mesmo nível de compressão.
- **Separação entre "média por matéria" e "média geral do curso":** reflete exatamente a necessidade real do estudante de visualizar tanto o desempenho pontual quanto o panorama geral, exigindo que o modelo implemente dois níveis de cálculo (agregação dupla).
- **Distinção entre alerta de "hoje" e "prazo vencido":** cobre dois cenários de urgência diferentes — um preventivo (entrega é hoje) e outro corretivo (already atrasado) — tornando o sistema de alertas mais útil do que um simples calendário.
- **Cruzamento de dados entre abas (prazos puxando informações da checklist):** evita redundância de cadastro (o usuário não precisa inserir a mesma tarefa duas vezes), exigindo que o modelo pense na aplicação como um sistema integrado, não como 4 telas isoladas.
- **Requisito de persistência "durante a sessão":** define uma expectativa técnica realista para o Canvas (sem backend/banco de dados permanente), evitando frustração do usuário ao recarregar a página, e orientando o modelo a usar estado em memória (variáveis/JS) corretamente.
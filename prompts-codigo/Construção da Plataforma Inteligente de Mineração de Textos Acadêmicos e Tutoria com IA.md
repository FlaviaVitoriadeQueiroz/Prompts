Prompt: Construção da Plataforma Inteligente de Mineração de Textos Acadêmicos e Tutoria com IA (Google Gemini)

Objetivo: Instruir o Gemini (via Canvas) a construir, do zero, um projeto completo de mineração de textos acadêmicos com IA generativa, cobrindo ingestão de PDF, limpeza de dados, engenharia de prompts, auditoria anti-alucinação, auditoria ética, cache/performance e interface de usuário — replicando a arquitetura descrita nos documentos do Projeto Integrador (Módulos de Escopo, Fases, Engenharia de Dados e Ciência de Dados).

Prompt:

```
Você é um engenheiro de software sênior especializado em Python, Engenharia de Dados e integração com LLMs. Quero que você construa, dentro deste Canvas, um projeto funcional chamado:

"[NOME DO PROJETO]"

CONTEXTO DO PROJETO
Este é um projeto de extensão universitária ([NOME DO PROGRAMA DE EXTENSÃO]) que visa ajudar estudantes a ler, sintetizar e compreender criticamente artigos científicos em PDF, usando a API do [NOME DO MODELO/API DE IA]. O sistema deve seguir o framework de prompts PRECO (Papel, Restrições, Entrada, Comando, Output) em todas as chamadas à IA.

OBJETIVO GERAL
Criar um pipeline de mineração de textos acadêmicos que extraia texto de PDFs, limpe e organize esse conteúdo, envie para a API de forma estruturada, e devolva ao usuário resumos, fichamentos e flashcards de estudo — com auditoria de confiabilidade (anti-alucinação) e ética (anti-viés) antes de exibir o resultado final.

ARQUITETURA EM CAMADAS (implemente cada uma como um módulo separado)

1. Módulo de Ingestão (input)
   - Aceitar upload de arquivo PDF/TXT.
   - Extrair o texto usando bibliotecas equivalentes a [BIBLIOTECAS DE EXTRAÇÃO, ex.: PyPDF2/pdfplumber].
   - Lidar com PDFs desformatados (cabeçalhos repetidos, colunas duplas, tabelas).

2. Módulo de Pré-processamento (ETL)
   - Limpeza textual (remoção de ruído, cabeçalhos repetidos).
   - Tokenização.
   - Anonimização de dados pessoais (nomes, e-mails, CPFs) antes de qualquer envio externo, em conformidade com [LEI/NORMA DE PROTEÇÃO DE DADOS, ex.: LGPD].
   - Organizar o texto extraído em blocos por página/parágrafo, preservando metadados de origem (página, seção) para permitir validação posterior.

3. Módulo de Engenharia de Prompts (orquestração)
   - Implementar uma biblioteca de templates de prompt no framework PRECO.
   - Casos de uso: [LISTA DE CASOS DE USO, ex.: resumo estruturado, flashcards, explicação de trechos densos, extração de entidades/conceitos-chave].
   - Estruturar as chamadas à API de forma modular, permitindo troca futura de modelo/endpoint sem afetar o restante do pipeline.

4. Módulo de Auditoria Anti-Alucinação
   - Após receber a resposta da IA, comparar os termos/citações da resposta com o texto bruto original extraído do PDF (usando correspondência de termos e/ou similaridade textual).
   - Sinalizar visualmente ao usuário qualquer trecho da resposta que não possa ser localizado no documento-fonte (possível alucinação ou referência inventada).

5. Módulo de Auditoria Ética (anti-viés)
   - Checklist simples que analisa se a resposta gerada contém linguagem discriminatória de gênero, raça ou classe, alertando o usuário quando aplicável.

6. Módulo de Cache e Performance
   - Cache local (pode ser em memória, SQLite ou JSON) para respostas de perguntas idênticas, evitando chamadas repetidas à API.
   - Implementar retentativas com backoff exponencial para lidar com limite de cota da API.

7. Interface do Usuário
   - Construir uma interface simples e funcional (formato: [ESCOLHER, ex.: web app estilo Streamlit / HTML+JS]) com:
     a) upload do PDF;
     b) seleção do tipo de tarefa ([LISTAR TAREFAS DISPONÍVEIS]);
     c) exibição do resultado com destaque visual para trechos não verificados (alerta anti-alucinação);
     d) botão para exportar o resultado em PDF ou texto.

REQUISITOS NÃO FUNCIONAIS
- Código em [LINGUAGEM/STACK], bem comentado e organizado em funções/módulos claros.
- Tratamento de erros e exceções em todas as chamadas externas.
- Conformidade com [LEI/NORMA APLICÁVEL]: nenhum dado pessoal deve ser enviado à API sem anonimização prévia.
- Arquitetura desacoplada: cada módulo deve poder ser testado e substituído isoladamente.

ENTREGÁVEL ESPERADO
1. O código completo e funcional do projeto, dividido nos módulos acima.
2. Comentários explicando as decisões de arquitetura em cada módulo.
3. Instruções de uso (como rodar o projeto e onde inserir a chave da API).
4. Sugestões de próximos passos para evolução do projeto (ex.: dashboard de métricas de uso, data warehouse futuro).

Comece construindo a estrutura geral do projeto e o Módulo de Ingestão + Pré-processamento. Depois, avance módulo por módulo, explicando brevemente cada decisão antes de mostrar o código.
```

Por que funciona:

Placeholders entre colchetes ([NOME DO PROJETO], [LEI/NORMA APLICÁVEL], etc.) tornam o prompt reutilizável para outros projetos de mineração de dados com IA, bastando substituir o contexto específico sem reescrever a estrutura.
Divisão explícita em camadas numeradas espelha a arquitetura em pipeline (ingestão → pré-processamento → orquestração → auditoria → cache → interface) descrita nos módulos de Escopo e Engenharia de Dados, evitando que o modelo generativo misture responsabilidades em um único bloco de código monolítico.
Módulos de auditoria (anti-alucinação e anti-viés) isolados garantem que o modelo trate a confiabilidade e a ética como etapas de verificação explícitas do pipeline, e não como uma reflexão genérica — refletindo diretamente os riscos R1 e R4 mapeados no relatório de riscos.
Seção de "Requisitos não funcionais" força a IA a considerar conformidade legal, tratamento de erros e desacoplamento arquitetural desde o início, em vez de tratá-los como um adendo posterior.
Instrução final de sequenciamento ("comece pela ingestão... depois avance módulo por módulo") evita que o Gemini tente gerar todo o projeto de uma vez em um único bloco de código difícil de revisar, e aproveita melhor o formato iterativo do Canvas.
Pedido de entregáveis explícitos (código + comentários + instruções + próximos passos) assegura que a resposta final seja utilizável como produto de software, e não apenas como um esboço conceitual.
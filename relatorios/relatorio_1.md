# Relatório — RAGCore

## Viabilidade

- Grupo: Dupla 07
- Integrantes: Ana Luiza da Silva Souza e Gabriel Pereira Gonçalves
- Repositório: https://github.com/analuiza-souza/RAGCore
- Situação do repositório: Público, README e .gitignore, em 16/10/2026.
- Stack: Python, Streamlit, LangChain, ChromaDB, Ollama e Llama 3.2 1B.
- Veredito: Viável

É viável em um computador de 8 GB se o critério de sucesso for resposta presa aos trechos recuperados, com a página de origem. “Resposta exata” não é um critério que o Llama 3.2 1B sustenta. O README é mais preciso que o PDF: PDF, pypdf e citação de página.

## SWOT

### Forças

Uma linguagem e um processo local, sem chave paga. A dupla já escolheu modelo pequeno por causa da RAM. O fluxo upload, fatiamento, busca e chat é um encadeamento especificável.

### Fraquezas

O PDF promete resposta exata e cita “[SaaS]” sem explicar o que isso restringe. LangChain muda de versão com frequência. Não há tamanho máximo de arquivo nem o que fazer quando o trecho recuperado não responde.

### Oportunidades

Spec com um PDF de exemplo, pergunta, trecho esperado e página. A interface mostra a citação mesmo quando o modelo hesita. Embeddings locais leves, como o README já indica.

### Ameaças

Ollama precisa estar instalado nas duas máquinas. Chunking ruim devolve a página errada com aparência de certeza. Trocar de modelo no meio da disciplina quebra a avaliação.

## Stack técnica

**Parecer: Adequada.** Python, Streamlit, ChromaDB, Ollama e Llama 3.2 1B estão adequados a um computador de 8 GB; LangChain permanece se a versão ficar fixa.

A stack acompanha a restrição que a dupla escreveu. Um modelo de 1 bilhão de parâmetros roda localmente, sem chave paga. Streamlit entrega o chat em Python. ChromaDB guarda os trechos. pypdf, citado no README, lê o PDF. Não há stack mais adequada para esse desenho dentro da disciplina.

LangChain é a peça instável, porque muda de versão com frequência. Ela continua adequada se o projeto fixar a versão no arquivo de dependências. Se a API da biblioteca atrapalhar a spec, a dupla pode chamar o Ollama e o ChromaDB direto, sem trocar o restante. O modelo e o embedding devem ficar nomeados, para as duas máquinas reproduzirem a mesma resposta.

## Recomendação

**Definam sucesso como resposta acompanhada do trecho e da página, em vez de resposta exata.**

O RAGCore está no tamanho certo para a disciplina, desde que a dupla ajuste o que chama de sucesso. Um modelo pequeno, o Llama 3.2 de 1 bilhão de parâmetros, rodando num computador de 8 GB, não sustenta a promessa de resposta exata. A constitution pode definir o resultado de outro modo: a pessoa envia um PDF, faz uma pergunta, e a tela mostra a resposta junto com o trecho recuperado e o número da página. Se o trecho não responder à pergunta, o sistema diz isso, em vez de completar com conhecimento geral. Para a spec ser testável, entra um documento de exemplo, uma pergunta, a página em que a resposta deveria ser encontrada e um tamanho máximo de arquivo. O modelo de chat e o modelo de embeddings ficam nomeados e estáveis. O README de execução explica como instalar o Ollama, porque sem ele a outra máquina da dupla não reproduz o projeto.

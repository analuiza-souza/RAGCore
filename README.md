# RAGCore
Assistente local para consulta de documentos PDF com IA generativa, recuperação de informações (RAG) e respostas fundamentais no conteúdo dos documentos.

## DESRCIÇÃO
O RAGCore é um assistente local desenvolvido para facilitar a consulta de informações em documentos PDF, como apostilas, manuais e documentações técnicas. O projeto busca resolver a dificuldade e a perda de tempo ao procurar informações específicas em arquivos extensos. Seus principais usuários são estudantes, desenvolvedores e profissionais que precisam consultar conteúdos técnicos com frequência. A aplicação permitirá importar documentos e fazer perguntas em uma interface de chat. Utilizando recuperação de informações (RAG) e inteligência artificial generativa executada localmente, o sistema fornecerá respostas baseadas no conteúdo dos arquivos. O resultado esperado é tornar as consultas mais rápidas e práticas, apresentando respostas contextualizadas e referências às páginas dos documentos, sem depender de APIs pagas.

## STACK TECNOLÓGICA
- Linguagem: Python 3.11+
- Framework: Streamlit e LangChain
- Bibliotecas: pypdf
- Banco de dados vetorial: ChromaDB
- Execução de IA local: Ollama (Llama 3.2 1B)
- Embeddings: modelo leve de embeddings executado localmente

- ## JUSTIFICATIVA TÉCNICA
- A combinação tecnológica foi escolhida por utilizar ferramentas acessíveis e adequadas ao desenvolvimento de um assistente de consulta a documentos PDF. Python permite integrar as bibliotecas necessárias, enquanto Streamlit facilita a criação de uma interface simples e interativa. O pypdf será utilizado para extrair o texto dos documentos, e o ChromaDB permitirá armazenar e recuperar os trechos mais relevantes. O LangChain ajudará a conectar as etapas de busca e geração de respostas, enquanto o Ollama possibilitará executar o modelo de IA localmente, sem depender de APIs pagas. Essa combinação favorece o aprendizado prático de desenvolvimento de software, integração de bibliotecas e recuperação de informações, além de permitir construir o projeto por etapas, considerando a limitação de recursos do computador.

# Relatório — RAGCore — semana 2

## Viabilidade

- Grupo: Dupla 07
- Integrantes: Ana Luiza da Silva Souza e Gabriel Pereira Gonçalves
- Repositório: https://github.com/analuiza-souza/RAGCore
- Constitution: https://github.com/analuiza-souza/RAGCore/blob/main/CONSTITUTION.md
- Veredito: Atende

O arquivo abre na `main` e repete o que o PDF descreve. Os dois aprovam a spec antes de cada funcionalidade. Um revisa o merge do outro. Arquitetura, segurança, requisito ou comportamento visível pedem os dois. O agente versiona, na branch, documentação auxiliar, teste não destrutivo e formatação. Não aprova o próprio trabalho, não faz merge e não muda requisito, dependência nem configuração crítica sem uma pessoa.

## SWOT

### Forças

A regra 1 é do assistente: se o trecho recuperado não sustenta a resposta, ele diz isso, em vez de inventar. A regra 2 impede misturar documento de outro usuário na consulta. A execução local com Ollama e Llama 3.2 está escrita. Dado privado não entra no Git. O fluxo é spec, branch, teste, revisão, merge.

### Fraquezas

A regra 3, de “pronta”, fica genérica: critérios da spec, testes e revisão de um integrante. O que é uma resposta aceitável no RAG (página citada, trecho ao lado) ainda não está na constitution. O PDF e o arquivo também não dizem o que fazer com a chave ou com o modelo se a execução deixar de ser local.

### Oportunidades

A spec pode exigir a página de origem ao lado da frase, que era o critério da semana 1. Pergunta de teste com trecho presente e pergunta sem trecho fecham a regra 1.

### Ameaças

Um agente que complete a resposta com conhecimento do modelo, quando o Chroma não achou o trecho, quebra a regra 1 e ainda parece fluente. Misturar dois manuais na mesma consulta quebra a regra 2.

## Stack técnica

**Parecer: Sem mudança.** Ollama e Llama 3.2 continuam, locais. A constitution não troca isso por API externa. Streamlit, LangChain e ChromaDB não são renomeados aqui, e não precisavam.

Se a chamada sair do computador, a dupla tem de aprovar, porque a regra de execução local deixa de valer.

## Recomendação

**Mantenham os papéis e escrevam na spec que a resposta mostra o trecho e a página, ou diz que não encontrou.**

Os dois aprovam a spec. Um aprova o merge do outro, e mudança de requisito pede os dois. O agente mexe em texto e teste na branch. Inventar resposta sem documento, ou misturar documentos, continua fora.

# RAGCore — Constitution

**Versão:** 1.0  
**Integrantes:** Ana Luiza da Silva Souza e Gabriel Pereira Gonçalves

---

## 1. Objetivo

Esta Constitution define as regras e responsabilidades que orientam o desenvolvimento do **RAGCore**, um assistente de IA local para consulta de documentações técnicas e manuais.

## 2. Papéis e responsabilidades

### 2.1. Aprovação da Spec

Ana Luiza da Silva Souza e Gabriel Pereira Gonçalves devem revisar e aprovar a especificação (Spec) antes do desenvolvimento de cada funcionalidade.

### 2.2. Aprovação do merge

Um integrante deve revisar e aprovar as alterações propostas pelo outro antes do merge na branch principal. Mudanças críticas de arquitetura, segurança ou requisitos precisam da aprovação dos dois integrantes.

### 2.3. Autonomia do agente de IA

O agente de IA pode criar documentação auxiliar, testes não destrutivos e correções de formatação em uma branch de trabalho, desde que respeite a Spec aprovada.

O agente não pode aprovar o próprio trabalho, realizar o merge sozinho ou alterar requisitos, dependências e configurações críticas sem autorização humana.

## 3. Regras inegociáveis

### Regra 1 — Respostas fundamentadas nos documentos

O assistente deve priorizar as informações recuperadas da documentação. Se não encontrar contexto suficiente para responder, deve informar essa limitação, em vez de inventar uma resposta.

### Regra 2 — Isolamento dos dados de cada documento

Os trechos recuperados devem pertencer ao documento ou conjunto de documentos autorizado para a consulta atual. O sistema não deve misturar informações de usuários ou documentos independentes sem autorização.

### Regra 3 — Critério verificável de conclusão

Uma funcionalidade só será considerada pronta quando cumprir os critérios de aceitação definidos na Spec, passar pelos testes aplicáveis e tiver suas alterações revisadas por um integrante da dupla antes do merge.

Funcionalidades de consulta documental também devem ser verificadas com perguntas de teste para avaliar a relevância dos trechos recuperados e a coerência das respostas geradas.

## 4. Princípios técnicos

- Priorizar a execução local com Ollama e o modelo Llama 3.2.
- Utilizar os trechos recuperados dos documentos como contexto para gerar respostas.
- Informar ao usuário quando não houver informações suficientes para responder com segurança.
- Evitar o versionamento de arquivos que contenham dados privados ou informações sensíveis.
- Manter as alterações relevantes registradas no Git.

## 5. Fluxo de desenvolvimento

1. Definir e aprovar a Spec.
2. Implementar a funcionalidade em uma branch de trabalho.
3. Executar os testes aplicáveis.
4. Revisar as alterações.
5. Aprovar e realizar o merge na branch principal.
6. Atualizar a documentação quando necessário.

## 6. Alterações na Constitution

Qualquer alteração nesta Constitution deve ser discutida e aprovada pelos dois integrantes antes de ser incorporada à branch principal.

## 7. Vigência

Esta Constitution passa a orientar o desenvolvimento do RAGCore após a aprovação dos dois integrantes da dupla.
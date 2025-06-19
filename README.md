# rag
RAG da biblia usando Ollama gemma3:12b | FAISS | LangChain | Nomic Embed 

Aviso: Isso foi uma POC e não substitui a leitura da biblia fisica! Clone o repo, teste com suas perguntas e verifique as respostas!

## 

<div style="display: inline_block">

<img align="center" height="45px" width="150px" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/googlecloud/googlecloud-original.svg"  /> 


<img align="center" height="45px" width="150px" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/jupyter/jupyter-original-wordmark.svg" />

          
</div>


##

# RAG com Ollama, Gemma3 12B e LangChain

Este repositório demonstra uma implementação de Retrieval Augmented Generation (RAG) utilizando o modelo de linguagem Gemma3 12B executado via Ollama, FAISS para busca de similaridade e LangChain. O desenvolvimento e a execução deste projeto foram realizados no Google Colab, com embeddings gerados por Nomic Embed.

---

## Tecnologias Utilizadas

* **RAG (Retrieval Augmented Generation):** Uma técnica que combina a capacidade de geração de modelos de linguagem com a recuperação de informações relevantes para produzir respostas mais precisas e informadas.
* **Ollama:** Uma plataforma que permite executar grandes modelos de linguagem (LLMs) localmente, facilitando o uso do Gemma3 12B.
* **Gemma3 12B:** Um modelo de linguagem poderoso desenvolvido pelo Google, utilizado aqui para a etapa de resposta.
* **FAISS (Facebook AI Similarity Search):** Uma biblioteca para busca eficiente de similaridade em embeddings, utilizada para armazenar e consultar o índice vetorial.
* **LangChain:** Um framework para desenvolver aplicações alimentadas por LLMs, fornecendo ferramentas para encadear componentes de forma modular e flexível.
* **Nomic Embed:** Utilizado para gerar embeddings de alta qualidade para o texto, que são então indexados pelo FAISS.
* **Google Colab:** O ambiente de desenvolvimento e execução escolhido para este projeto, devido à sua facilidade de uso e acesso a GPUs.
* **Python:** A linguagem de programação principal utilizada em todo o projeto.

---

## Estrutura do Projeto

O projeto é estruturado para demonstrar o fluxo completo de um sistema RAG:

1.  **Criação do Índice Vetorial:** Documentos são processados, divididos em chunks, e embeddings são gerados utilizando Nomic Embed. Esses embeddings são então armazenados em um índice FAISS.
2.  **Recuperação (Retrieval):** Dada uma consulta, o FAISS é usado para recuperar os documentos mais relevantes do índice.
3.  **Geração (Generation):** Os documentos recuperados são passados para o modelo Gemma3 12B (via Ollama) juntamente com a consulta, para gerar uma resposta informada.
4.  **Orquestração com LangChain:** LangChain conecta essas etapas, criando uma pipeline eficiente para o RAG.

---

## Como Rodar o Projeto

Para executar este projeto, você precisará do Google Colab e de algumas configurações iniciais para o Ollama e o Gemma3 12B.

1.  **Abra no Google Colab:** O projeto foi desenvolvido para ser executado diretamente no Google Colab. Recomenda-se abrir e clonar o(s) notebook(s) presente(s) neste repositório.
2.  **Instale as Dependências:** As células iniciais do notebook irão conter comandos para instalar todas as bibliotecas Python necessárias (LangChain, FAISS, Ollama, etc.).
3.  **Configurar Ollama e Gemma:**
    * Siga as instruções no notebook para instalar e iniciar o servidor Ollama no ambiente Colab.
    * Puxe o modelo `gemma:3 12b` usando o comando `ollama pull gemma3:12b`.
4.  **Execute as Células:** Prossiga executando as células do notebook sequencialmente. Isso incluirá:
    * Carregamento dos dados.
    * Geração dos embeddings com Nomic Embed.
    * Criação e persistência do índice FAISS.
    * Configuração da cadeia LangChain com o modelo Ollama.
    * Exemplos de consultas RAG.

---

## Contribuições

Sinta-se à vontade para enviar sugestões, melhorias ou encontrar algum problema.

---

## Licença

Este projeto está sob a licença [MIT License / Apache License 2.0 ].

---

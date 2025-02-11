# Langchain RAG Tutorial

This is an updated implementation of the RAG application from pixegami's "[RAG + Langchain Python Project: Easy AI/Chat For Your Docs](https://www.youtube.com/watch?v=tcqEUSNCn8I)" video tutorial. This repo maintains a modified working version of the [original Langchain RAG Tutorial repo](https://github.com/pixegami/langchain-rag-tutorial).

## 🏗️ Setup

1. Clone [this](https://github.com/llamistan/langchain-rag-tutorial/tree/main) repo.
     ``` bash
     git clone https://github.com/llamistan/langchain-rag-tutorial.git
     ```

1. Navigate inside this repo
     ``` bash
     cd langchain-rag-tutorial
     ```

1. Create a new Python virtual environment.
     ```
     python3 -m venv .venv
     source .venv/bin/activate
     ```

1. Install the packages required for this python envirnoment in `requirements.txt`.
     ``` bash
     pip install -r requirements.txt
     ```

1. Add a `.env` file by copying the `.env.sample` file. Replace the `YOUR_KEY_HERE` in your `.env` file with your OpenAI Key and save the file.
     ```bash
     OPENAI_API_KEY=sk-proj-1ka3d...
     ```

1. Create the vector store from the Alice in Wonderland book.
    ```
    python create_database.py
    ```

## 🚀 Running the Query Script

1. Ask the LLM a question about the Alice in Wonderland book (or any other data in the vector store).

    ```python
    python query_data.py "How does Alice meet the Mad Hatter?"
    ```
## ✨ Going A Step Further
Here are some ideas to further enhance the app:
- **Prompt Engineering.** Modify `PROMPT_TEMPLATE` in `query_data.py` to experiment with different prompts and improve the quality of the responses.
- **Add More Data.** Populate the vector store with more documents to improve response accuracy on a particular topic.
- **Improve Relevance Filtering.** Experiment with different similarity thresholds.
- **Implement a Chat Interface.** Use Chainlit or another frontend conversational AI framework to create a chatbot interface for the application.


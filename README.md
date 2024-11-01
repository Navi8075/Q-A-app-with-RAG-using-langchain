# Q-A-app-with-RAG-using-langchain
### Using LangChain and Gemini pro
## Introduction
With this Retrieval-Augmented Generation (RAG) application, you can create chatbots for your documents or files.
### Creating the RAG application
The process for creating the app is as follows:
1. Split your data into chunks of text (1000 words) to store your data more efficiently. This allows the retrieval process to capture pieces of information that are more relevant to the query, and the generation by the LLM (Gemini pro model) to be more precise.only parts of a document will be included in the prompt, instead of the entire document collection.
2. Create vector embeddings from the chunks and store them in a [Chroma database](https://www.trychroma.com/). Vector embeddings are numerical representations of terms, which can be words, sentences, or documents. These embeddings capture the relationships and similarities between the terms. In language models, this allows the model to understand the meaning and context of words based on their similarity to other words.
3. Use the query input by the user to perform a similarity search and retrieve a set of relevant chunks from the database.
4. The LLM (google Gemini pro model) uses the relevant chunks as context and sends a response along with its sources.

   ### Google AI API Key
Before you begin, set up an googleAI account and generate a new key. You will need to put your credentials in a `.env` file.
* Go to (https://ai.google.dev/gemini-api/docs/api-key) and create an googleAI key.
* Create a `.env` file in your project directory and add `"your_generated_secret_key".

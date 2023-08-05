# Vedic Astrology Analysis

The notebook uses a unique approach to load a PDF book, split it up into documents, get vectors for those documents as embeddings, and then ask a question. The technique can be used to query books as well as internal documents or external data sets.

## How it Works

1. **Data Loading**: The notebook begins by loading a PDF book related to Vedic Astrology. It uses the PyPDFLoader from LangChain to load the data.

2. **Data Splitting**: The loaded data is then split into smaller documents using the RecursiveCharacterTextSplitter from LangChain.

3. **Embeddings**: The notebook uses OpenAI to generate embeddings for the split documents. These embeddings are vectors that represent the semantic meaning of the documents.

4. **Pinecone Indexing**: The embeddings are stored in Pinecone, an external vector store. This allows for efficient semantic search of the documents.

5. **Question Answering**: The notebook uses OpenAI to answer questions based on the indexed documents. It uses a conversation chain to handle the question-answering process.

## Usage

The libraries used in this notebook include:

1. **langchain**: This library is used for loading and processing the PDF data, creating embeddings, and setting up the question-answering chain.
2. **pinecone**: This library is used for initializing the Pinecone vector database and performing similarity search.
3. **OpenAI**: This library is used for creating embeddings and answering questions.

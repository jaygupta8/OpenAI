# Vedic Astrology Analysis

This repository contains a Jupyter notebook that uses the power of OpenAI, LangChain, and Pinecone to perform semantic search and analysis on Vedic Astrology data.

## Overview

The notebook uses a unique approach to load a PDF book, split it up into documents, get vectors for those documents as embeddings, and then ask a question. The technique can be used to query books as well as internal documents or external data sets.

## How it Works

1. **Data Loading**: The notebook begins by loading a PDF book related to Vedic Astrology. It uses the PyPDFLoader from LangChain to load the data.

2. **Data Splitting**: The loaded data is then split into smaller documents using the RecursiveCharacterTextSplitter from LangChain.

3. **Embeddings**: The notebook uses OpenAI to generate embeddings for the split documents. These embeddings are vectors that represent the semantic meaning of the documents.

4. **Pinecone Indexing**: The embeddings are stored in Pinecone, an external vector store. This allows for efficient semantic search of the documents.

5. **Question Answering**: The notebook uses OpenAI to answer questions based on the indexed documents. It uses a conversation chain to handle the question-answering process.

## Usage

To use this notebook, you need to have access to OpenAI and Pinecone. You also need to install the required Python libraries, including LangChain and Pinecone's Python client.

## Example

Here is an example of a question you can ask the system:

```python
query = "What will be the best period (age wise) for this native? Analyze all his below details: ..."
docs = docsearch.similarity_search(query)
chain({"input_documents": docs, "human_input": query}, return_only_outputs=True)
```

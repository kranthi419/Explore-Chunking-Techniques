# Explore-Chunking-Techniques
## What is chunking?
Chunking refers to the process of breaking large pieces of text into smaller text segments or chunks. To emphasize the importance of chunking, it is helpful to understand RAG. RAG is a technique in natural language processing (NLP) that combines information retrieval and large language models (LLMs) to retrieve relevant information from supplemental datasets to optimize the quality of the LLM’s output. To manage large documents, we can use chunking to split the text into smaller snippets of meaningful chunks. These text chunks can then be embedded and stored in a vector database through the use of an embedding model. Finally, the RAG system can then use semantic search to retrieve only the most relevant chunks. Smaller chunks tend to outperform larger chunks as they tend to be more manageable pieces for models of smaller context window size.

**Some key components of chunking include:**

Chunking strategy: Choosing the right chunking strategy for your RAG application is important as it determines the boundaries for setting chunks. We will explore some of these in the next section.
Chunk size: Maximum number of tokens to be in each chunk. Determining the appropriate chunk size usually involves some experimenting.  
Chunk overlap: The number of tokens overlapping between chunks to preserve context. This is an optional parameter.

## Sources:

Chunking techniques from agno.
https://docs.agno.com/chunking

Chunking techniques from IBM.
https://www.ibm.com/think/tutorials/chunking-strategies-for-rag-with-langchain-watsonx-ai

There are several different chunking strategies to choose from. It is important to select the most effective chunking technique for the specific use case of your LLM application. Some commonly used chunking processes include:r: 

Fixed-size chunking: Text splitting with a specific chunk size and optional chunk overlap. This approach is the most common and straightforward.
Recursive chunking: Iterating default separators until one of them produces the preferred chunk size. Default separators include ["\n\n", "\n", " ", ""]. This chunking method uses hierarchical separators so that paragraphs, followed by sentences and then words, are kept together as much as possible.
Semantic chunking: Splitting text in a way that groups sentences based on the semantic similarity of their embeddings. Embeddings of high semantic similarity are closer together than those of low semantic similarity. This results in context-aware chunks.
Document-based chunking: Splitting based on document structure. This splitter can utilize Markdown text, images, tables and even Python code classes and functions as ways of determining structure. In doing so, large documents can be chunked and processed by the LLM.
Agentic chunking: Leverages agentic AI by allowing the LLM to determine appropriate document splitting based on semantic meaning as well as content structure such as paragraph types, section headings, step-by-step instructions and more. This chunker is experimental and attempts to simulate human reasoning when processing long documents.  

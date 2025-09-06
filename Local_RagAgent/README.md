🦙 Local RAG Agent with Llama 3.2

This project demonstrates a fully local Retrieval-Augmented Generation (RAG) system, designed for privacy, efficiency, and independence from cloud APIs. It uses Llama 3.2 as the core language model (served through Ollama
) and Qdrant as the vector database for fast semantic search. The application provides an interactive interface where you can query custom documents and receive context-aware answers generated entirely on your local machine.

✨ Key Features

🔒 100% Local Setup – Runs entirely on your machine, ensuring full data privacy (no third-party APIs).

🦙 Llama 3.2 via Ollama – Leverages the latest open Llama model with optimized inference through Ollama.

📚 Retrieval-Augmented Generation (RAG) – Enhances Llama’s responses with facts pulled from your own documents.

🔍 Qdrant Vector Search – Stores document embeddings and retrieves the most relevant chunks efficiently.

🖥️ Interactive Playground – Streamlit-based UI for uploading documents, asking questions, and viewing contextual responses.

⚡ Scalable & Extensible – Can be expanded with additional models, embedding providers, or larger datasets.

🛠️ How It Works

Document Ingestion

Upload text, PDF, or markdown files.

Each document is split into chunks and embedded into high-dimensional vectors.

Embeddings are stored inside the Qdrant vector database.

User Query

Enter a natural language question in the chat interface.

Retrieval

The system queries Qdrant to fetch the top-N most relevant chunks based on semantic similarity.

Augmented Prompting

Retrieved context is combined with the user’s query and passed to Llama 3.2.

Response Generation

Llama generates a grounded answer that uses both its own reasoning and the retrieved knowledge.

Display & History

The UI shows the AI’s response, the retrieved sources, and maintains a searchable conversation history.

🔧 Tech Stack

LLM → Llama 3.2
 served locally via Ollama

Vector Database → Qdrant

Frontend → Streamlit
 for the interactive interface

Embeddings → Can use Ollama’s built-in embedding models or alternatives like SentenceTransformers

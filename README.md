# PDF Chatbot 

SDP_LLM (June 2025) 
<br> <br>
A lightweight chatbot app that lets users upload a PDF and ask questions about its content using Google's Gemini LLM. It integrates PDF uploading, text extraction, embedding generation, vector storage, and Retrieval Q&A, all in one seamless pipeline.

<b> <h3>How it works: </b></h3>
1. PDF Upload and Text Extraction:
User uploads a PDF file via a Gradio interface. The text is extracted using pdfplumber.
2. Text Preprocessing:
The text is split into manageable chunks using LangChain's CharacterTextSplitter.
3. Embeddings & Vector Store:
Each chunk is embedded using HuggingFaceEmbeddings. Chunks are stored in Chroma, a vector database. This allows for efficient semantic similarity searches when a user asks a question.
4. Question Answering Chain:
When a user inputs a question, the chatbot retrieves the most relevant text chunks from ChromaDB and sends them to the Gemini model(gemini-2.5-pro). LangChain’s RetrievalQA chain is used to handle this process. <hr>

<b> <h3>Tech Stack: </b></h3> 
1. Programming Language: Python is used for building, training and deploying the model
2. Libraries Used:<br>
↣ Gradio: The trained model is integrated into a Gradio Interface<br>
↣ pdfplumer: For extracting text from PDF files <br>
↣ Langchain: For creating the retrieval-based QA chain <br>
↣ chromaDB: Vector database used to store and retrieve text embeddings <br>
3. Large Language Model(LLM) : Google Generative AI (gemini-2.5-pro) 
4. Embeddings: HuggingFace Embedding - To convert text chunks into numerical vectors  <hr>

<b> <h3>Installation: </b></h3>
- Install Dependencies:
<pre><code> pip install langchain chromadb gradio google-generativeai pdfplumber transformers langchain-google-genai langchain-community </code></pre>

- Setting API Key:
<pre><code> import os os.environ['GOOGLE_API_KEY'] = 'your_google_api_key_here' </code></pre>



# RAG_PDF_chatbot
Welcome to the Streamlit PDF Q&A App, a powerful tool that lets you extract text from PDFs, process it with LangChain, and perform question-answering using Google Generative AI embeddings. 🧠🔍
✨ Features
- 📌 Upload and process PDFs using PyPDF2
- 🔍 Extract and split text using RecursiveCharacterTextSplitter
- 🤖 Generate AI embeddings with GoogleGenerativeAIEmbeddings
- 📚 Store and retrieve vectors using FAISS
- 💬 Interact with the processed text using ChatGoogleGenerativeAI
- ❓ Perform question-answering with load_qa_chain
- 📖 Extract text from PDFs with PyPDF2
- 🔗 Split text for better processing using RecursiveCharacterTextSplitter
- 🤖 Generate embeddings with GoogleGenerativeAIEmbeddings
- 📂 Store & retrieve vectors using FAISS
- 💬 Ask questions & get answers! powered by ChatGoogleGenerativeAI
- ⚡ Conversation history tracking for contextual responses
- 📑 Upload multiple PDFs and process text extraction.
- 🔎 Extract, split, and embed text using PyPDF2 and GoogleGenerativeAIEmbeddings.
- 📂 Vector storage with FAISS for efficient data retrieval.
- 🤖 Ask questions and receive AI-generated responses.
- 📜 Conversation history tracking with an option to download as CSV.
- 🎨 Custom chat UI for an enhanced user experience.

🛠 Installation
Ensure Python is installed, then install the required dependencies:
pip install streamlit PyPDF2 pandas base64 langchain langchain_google_genai faiss-cpu:

🚀 Usage
Run the application with:
streamlit run app.py
- Upload PDF Files: Users upload PDF documents to extract text data.
- Process Text: The system splits text into manageable chunks for embedding.
- Vector Store Creation: FAISS stores embeddings for similarity-based searching.
- Ask Questions: Users can input queries to retrieve relevant information from the processed PDFs.

Code Explanation
Functions:
- get_pdf_text(pdf_docs): Extracts text from the provided PDF documents.
- get_text_chunks(text, model_name): Splits text into chunks for embedding.
- get_vector_store(text_chunks, model_name, api_key): Converts text into vector embeddings and stores them in FAISS.
- get_conversational_chain(model_name, vectorstore, api_key): Defines the conversational model for answering questions.
- user_input(user_question, model_name, api_key, pdf_docs, conversation_history): Handles user queries, searches the vector store, and provides responses.
Key Components:
- Google AI Models: Used for embedding (models/embedding-001) and answering questions (gemini-1.5-flash).
- Streamlit UI: Facilitates user interaction.
- FAISS: Efficiently stores and retrieves text-based embeddings for similarity searches.
Notes
- Ensure you provide a valid Google API key to authenticate with AI models.
- Modify chunk sizes or temperature settings as needed for better response quality.
Future Improvements
- Add support for more AI models.
- Enable multi-PDF querying.
- Integrate caching for faster responses.




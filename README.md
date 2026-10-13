# PDF-Question-Answering-Using-Astra-DB-LangChain-and-Google-Gemini

Project Overview
This project implements a Retrieval-Augmented Generation (RAG) application that enables users to ask questions about PDF documents using natural language. It combines Astra DB vector search, LangChain, and Google Gemini to retrieve relevant document passages and generate context-aware answers.
The application extracts text from a PDF guideline, splits the content into smaller chunks, converts the chunks into vector embeddings, and stores them in Astra DB. When a user asks a question, the system retrieves relevant passages and uses Google Gemini to generate an answer based on the retrieved context.
Key Features
- PDF Text Extraction: Extract text from PDF documents using PyPDF2.
- Text Chunking: Split extracted content into chunks of 800 characters with 200 characters of overlap.
- Text Embeddings: Generate vector embeddings using Google's Gemini embedding model.
- Vector Database: Store and retrieve document embeddings using Astra DB.
- Semantic Search: Retrieve relevant document passages based on user questions.
- AI-Powered Question Answering: Use Google Gemini 2.5 Flash to generate answers from retrieved context.
- Relevance Search: Display the top four document matches with their associated scores.
- Interactive Querying: Ask multiple questions in a command-line loop without restarting the application.
Technologies Used
- Python
- Google Colab
- LangChain
- Google Gemini 2.5 Flash
- Gemini Embedding Model (gemini-embedding-001)
- DataStax Astra DB
- Cassandra Vector Store
- PyPDF2
- Hugging Face Datasets
- Cassio
Architecture and Workflow
1. PDF Input: Load the PDF guideline containing the information to be searched.
2. Text Extraction: Extract readable text from each PDF page.
3. Text Splitting: Divide the extracted text into overlapping chunks.
4. Embedding Generation: Convert text chunks into vector embeddings using Google's embedding model.
5. Vector Storage: Store the embedded text in Astra DB.
6. Question Processing: Accept a natural-language question from the user.
7. Semantic Retrieval: Retrieve relevant document content using vector similarity search.
8. Answer Generation: Pass the retrieved context and question to Google Gemini.
9. Result Display: Print the generated answer and the four most relevant document matches.

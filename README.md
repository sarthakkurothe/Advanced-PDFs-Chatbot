# Advanced-Chatbot-with-Langchain-and-Llama2-Deployed-

This project allows you to upload PDF documents, process them, and then engage in a conversational interface where you can ask questions about the documents.

## Getting Started

### Install Dependencies

`pip install -r requirements.txt`

1. Download the llama 2 7B GGUF model from https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGUF/blob/main/llama-2-7b-chat.Q4_K_M.gguf and place it in the models folder

![pdf_chatbot_Llama2](https://github.com/Samarth1337/Advanced-Chatbot-with-Langchain-and-Llama2-Deployed-/assets/42602263/d99d6bc3-2f36-448b-8eed-7bcb9dd10dd5)

### How it Works
1. GUI Development: The application's graphical user interface (GUI) is built using Streamlit, providing an intuitive and user-friendly interface for document upload, processing, and chat interaction.
2. Document Processing: Upon document upload, the application reads text from PDF files and splits it into chunks for efficient processing.
3. Text Embeddings: HuggingFaceEmbeddings are utilized to generate embedding vectors from text chunks, which are then used to find the most relevant content to a user's question.
4. Conversational Retrieval Chain: A conversational retrieval chain is built using Langchain, incorporating the LlamaCpp model for context generation. This chain facilitates seamless conversation flow and response generation based on the content in the uploaded PDFs.

### Code Structure

The code is structured as follows:

- **utils.py**
  -Contains utility functions for PDF text extraction, chunking, and vector store creation.
  - Utilizes HuggingFace Transformers for generating embedding vectors and creates a vector store using Faiss.
  - Builds a conversational retrieval chain using Langchain with the LlamaCpp model.store using Faiss.

- **app.py**
    - The main Streamlit application file responsible for handling navigation and user interaction.
    - Routes users between the upload/processing and chat interfaces based on their selections.
    - Manages session state variables and initializes the conversational retrieval chain.

- **upload_page.py**
    - Implements the upload and processing interface, allowing users to upload PDF documents and process them.
    - Provides feedback to users upon successful document processing.

- **chat_page.py**
    - Implements the chat interface, enabling users to interact with the system by asking questions related to the uploaded documents.
    - Handles user input and displays bot responses in real-time.
      
- **htmlTemplates.py**
    - Contains HTML templates for displaying user and bot messages in the chat interface.
    - Defines CSS styles for message formatting and avatar display.

## How to Use

1. **Run the Streamlit App**
 `streamlit run app.py`
2. **Upload & Process Documents**
    - This GUI allows the user to upload PDF documents and process them to extract text and create a vector store for conversational retrieval.
3. **Chat**
    - Once the documents are processed, users can switch to the chat interface to start asking questions related to the uploaded documents.
    - Interact with the system by typing questions in the text input field and view bot responses in real-time.

## Technologies/Libraries/Tools Used
1. Streamlit: For building the application's graphical user interface.
2. Langchain: For building the conversational retrieval chain and context generation.
3. Llama2: For generating responses based on the content in PDF documents.
4. HuggingFace Transformers: For text embeddings and language model functionalities.
5. PyPDF2: For extracting text from PDF documents.
6. Faiss: For creating and managing vector stores efficiently.
7. Python: The primary programming language used for development.

## Conclusion
The Advanced Chatbot project showcases the integration of advanced natural language processing techniques with document processing capabilities to create an intelligent conversational interface. By leveraging state-of-the-art technologies such as Langchain and Llama2, users can seamlessly interact with PDF documents and receive accurate and informative responses to their questions. This project demonstrates the potential of AI-powered chatbots in enhancing document understanding and accessibility.

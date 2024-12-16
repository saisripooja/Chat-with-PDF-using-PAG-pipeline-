

# Chat with Multiple PDFs  

This repository provides a simple yet powerful chat application that lets users interact with multiple PDF documents using a Large Language Model (LLM) enhanced with Retrieval-Augmented Generation (RAG).  

## Features  
- **PDF Integration**: Upload and query multiple PDFs seamlessly.  
- **RAG Workflow**: Combines LLM capabilities with vector database retrieval for highly relevant responses.  
- **Streamlit Frontend**: Interactive, user-friendly chat interface.  
- **LLM Flexibility**: Compatible with OpenAI, WatsonX, or other LLM providers.  

---

## How It Works  

1. **PDF Processing**:  
   PDFs are chunked and embedded using LangChain's `VectorstoreIndexCreator`. This ensures efficient retrieval of document content.  

2. **Vector Database**:  
   Stores document embeddings for quick similarity search. By default, this project uses **Chromadb**.  

3. **Chat Interface**:  
   Built with **Streamlit**, the chat interface allows users to interact with the LLM and receive document-aware responses.  

4. **LLM Integration**:  
   Prompts and retrieved context are passed to the LLM, which generates conversational and contextually relevant answers.  

---

## Installation  

Follow these steps to set up and run the project:  

### 1. Clone the Repository  
```bash  
git clone https://github.com/dinhquy-nguyen-1704/chat-with-multiple-PDFs.git  
cd chat-with-multiple-PDFs  
```  

### 2. Install Dependencies  
Install the required Python packages:  
```bash  
pip install -r requirements.txt  
```  

### 3. Set Up Environment Variables  
Create a `.env` file in the root directory to store your API keys and configuration. For example:  
```env  
OPENAI_API_KEY=your_openai_api_key  
CHROMADB_HOST=your_chromadb_url  
WATSONX_API_KEY=your_watsonx_api_key  
```  

### 4. Run the Application  
Start the Streamlit app:  
```bash  
streamlit run app.py  
```  

---

## Usage  

1. Upload one or more PDF files using the Streamlit interface.  
2. Ask questions related to the uploaded documents.  
3. Get accurate, context-aware answers powered by RAG and your preferred LLM.  

---

## Customization  

- **LLM Provider**: Modify the `llm.py` file to switch between different LLM providers like OpenAI, WatsonX, or Hugging Face models.  
- **Database**: Update the vector database settings in the `vectorstore.py` file to use alternatives like Pinecone or Weaviate.  
- **Frontend**: Customize the Streamlit interface in `app.py` to fit your specific use case.  

---

## Future Enhancements  

- Add support for other file types (e.g., Word documents).  
- Implement multi-user session handling for enterprise use.  
- Enhance vector database integrations for scalability.  


---

## Acknowledgments  

- [LangChain](https://github.com/hwchase17/langchain)  
- [Streamlit](https://streamlit.io/)  
- [Chromadb](https://www.trychroma.com/)



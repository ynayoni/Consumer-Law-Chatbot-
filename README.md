# Consumer-Law-Chatbot-
This is an AI-powered chatbot designed to assist users with queries related to the **Consumer Protection Act, 2019**, and guide them through grievance redressal procedures. The chatbot is built to process and respond to questions by utilizing **local LLM (Large Language Model)** without relying on commercial API services like OpenAI. The model is trained and augmented using legal documents (PDFs, e-textbooks) for answering specific consumer law-related queries.

## Features

- **Consumer Protection Act 2019 Queries**: Get information about rights, protections, and processes under the Consumer Protection Act.
- **Grievance Redressal Assistance**: Get step-by-step guidance on how to file a grievance, steps to take, and the resources available for consumers.
- **Legal Document Parsing**: Loads, processes, and extracts information from legal PDFs and textbooks to answer queries.
- **Semantic Search**: Utilizes a vector database (FAISS) for enhanced search functionality over the uploaded documents.
- **Local Deployment**: Entire chatbot runs locally, without the need for external API calls or services.

## Tech Stack

- **Frontend**: HTML, CSS, JavaScript (Simple chat interface)
- **Backend**: Python (Flask) for handling user requests and model queries
- **Model**: Local LLM via LLaMA (using `llama-cpp-python`)
- **Vector Database**: FAISS for document-based semantic search
- **Document Processing**: PyMuPDF, Langchain (PDF loaders)
- **Model Orchestration**: Langchain or custom RAG (Retrieval Augmented Generation)

## Installation

### Prerequisites

- Python 3.10+
- `pip` for installing dependencies

### 1. Clone the repository

```bash
git clone https://github.com/your-username/consumer-law-chatbot.git
cd consumer-law-chatbot
```

### 2. Create a virtual environment and install dependencies

```bash
python3 -m venv rasa_env
source rasa_env/bin/activate  # On Windows use `rasa_env\Scripts\activate`
pip install -r requirements.txt
```

### 3. Set up the model and documents

- Upload your legal PDFs or text documents to the `docs/` directory.
- Make sure the model is set up for local deployment with the required configuration.

### 4. Run the chatbot

```bash
python app.py
```

Visit `http://localhost:5000` in your browser to start interacting with the chatbot.

## How It Works

1. The user inputs a query in the chat interface.
2. The query is passed to the Flask backend, which processes it.
3. The system uses FAISS to search through uploaded legal documents and retrieves relevant sections.
4. The LLM model (LLaMA or any supported backend) generates a response based on the retrieved document content.
5. The chatbot provides a response to the user in real-time.


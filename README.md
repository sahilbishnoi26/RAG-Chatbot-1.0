# RAG-Chatbot-v0.5

**RAG-GPT: Retrieval-Augmented Generation (RAG) chatbot using OpenAI GPT Model, LangChain, ChromaDB, and Gradio**

## Features

### **1. Offline Documents**
Interact with pre-processed and vectorized documents, seamlessly integrating them into chat sessions.

### **2. Real-time Uploads**
Upload documents during chat sessions, allowing the chatbot to process and respond to content on-the-fly.

### **3. Summarization Requests**
Request a comprehensive summary of an entire PDF or document in a single interaction, streamlining information retrieval.

To use any of these methods, select the appropriate option from the **"RAG with" dropdown menu** within the chatbot interface.

### **Additional Capabilities**
- Customizable settings, such as adjusting the GPT model's **temperature** for optimal performance.
- Built-in **memory retention**, enabling the chatbot to recall previous Q&As for a more personalized experience.
- Displays retrieved content along with the corresponding PDF for reference.
- User-friendly interface built with **Gradio**.

## RAG-GPT User Interface
<div align="center">
  <img src="images/RAGGPT UI.png" alt="RAG-GPT UI">
</div>

## Project Schema
<div align="center">
  <img src="images/RAGGPT_schema.png" alt="Schema">
</div>

### **Note:** This project is currently a **demo**, and document management is simplified. It is not intended for production environments.

## Document Storage

Documents are stored in two dedicated folders within the `data` directory:
- **`data/docs_2`** – For files uploaded in real-time.
- **`data/docs`** – For documents that are pre-processed.

## Server Setup

The **`serve.py`** module establishes an **HTTPS server** to host PDF files, making them accessible for viewing.

## Database Creation

Vector databases (**vectorDBs**) are automatically created in the `data` folder, enabling efficient retrieval and response generation.

## Important Considerations

- This implementation is intended for **demonstration purposes only**.
- **A more secure document handling system is strongly recommended** for production use.
- Files must be placed in the appropriate directories (`data/docs_2` and `data/docs`) for proper functionality.

## Running the Project

The project requires setting up the environment and installing dependencies. There are two setup options:

### **Option 1: Using the Parent Directory Instructions**
Follow the instructions in the [parent directory](https://github.com/Farzad-R/LLM-playground/tree/master) to create an environment and install the required libraries.

### **Option 2: Installing Dependencies Individually**
To install dependencies manually, run:

```
pip install gradio==4.13.0 langchain==0.0.354 openai==0.28.0

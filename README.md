# ChatBotaLangGraph Chatbot with Google Gemini
**OVERVIEW**
This project is a conversational AI chatbot built using Google Gemini via langchain_google_genai, orchestrated with LangGraph, and deployed using FastAPI for the backend and Streamlit for the frontend. The chatbot can answer questions, provide explanations, and maintain a conversation history with memory support.

**Features**

Conversational AI powered by Google Gemini 2.0

Chat state management using LangGraph

Persistent memory support to remember prior conversation

Web-based interface via Streamlit

Backend API using FastAPI

Public URL access using ngrok

Real-time status monitoring of backend and frontend

Error handling for timeouts, connection errors, and unexpected issues

**Project Structure**
project/
│
├─ backend.py       # FastAPI backend with LangGraph chatbot
├─ app.py           # Streamlit frontend interface
├─ requirements.txt # Required Python packages
└─ README.md        # Project documentation

**Setup Instructions**
1. **Clone the Repository**
git clone <your-repo-url>
cd <your-repo-folder>

2. **Install Dependencies**
pip install -r requirements.txt

3.**Set Google API Key**

Replace with your own API key:

os.environ["GOOGLE_API_KEY"] = "<YOUR_GOOGLE_API_KEY>"

4. **Run the Backend**
python backend.py


Backend will run on http://localhost:8000

Health check endpoint: http://localhost:8000/health

5.**Run the Frontend**
python app.py


Streamlit will start on http://localhost:8501

Chatbot maintains conversation history across multiple prompts

6. **Access via Public URL**

Ngrok tunnels are automatically generated

The public URL for the chatbot frontend and backend will be displayed in the console

Usage

Open the Streamlit URL in your browser.

Type a message in the chat input box.

The assistant will reply, maintaining context across multiple messages.

Use the sidebar to:

Test backend connection

Clear chat history

Monitor total messages sent/received

Important Notes

Make sure your Google API Key is valid and has access to Gemini.

Backend must be running before the frontend for proper responses.

**If using Colab:**

Make sure to allow ngrok to create tunnels

Use nest_asyncio to avoid asyncio conflicts

The chatbot might take a few seconds to respond for complex queries.

**Dependencies**

See requirements.txt for all required Python packages.

**License**

This project is open-source and free to use.

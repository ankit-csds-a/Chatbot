🤖 Gen AI Chatbot (Streamlit + Groq API)
This is a Streamlit-based chatbot app that interacts with users using Groq’s LLMs such as Gemma2-9b-it. It supports real-time streaming responses, maintains chat history, and creates a smooth conversational UI using st.chat_message().

🌟 Features
🧠 Powered by Groq LLMs (e.g., gemma2-9b-it, llama3-8b-8192, etc.)

💬 Conversational chat with memory (maintains full session history)

⚡ Real-time streaming of responses

🔐 Easily switch models via session state

📦 Clean UI using latest st.chat_message() from Streamlit

📦 Requirements
Python Dependencies
Install them using pip:

bash
Copy
Edit
pip install streamlit groq python-dotenv
🔐 API Key Setup
This app uses your Groq API key to generate responses. You can either:

Option 1 – Hardcode (for testing only)
python
Copy
Edit
api_key = "your_groq_api_key"
Option 2 – Use .env file (Recommended)
Create a .env file in the same directory:

ini
Copy
Edit
GROQ_API_KEY=your_groq_api_key_here
Load it with:

python
Copy
Edit
from dotenv import load_dotenv
load_dotenv()
api_key = os.getenv("GROQ_API_KEY")
🚀 How to Run
bash
Copy
Edit
streamlit run chatbot_app.py
✨ How It Works
The app starts with a title and initializes session state for:

ai_model (default: gemma2-9b-it)

messages (chat history)

On every new user message:

The full message history is sent to the Groq API.

The assistant replies with a streamed response.

The reply is displayed live and saved to the session state.

🧠 Prompt & Model Settings
Model: gemma2-9b-it (you can change to llama3-8b-8192 or others)

Temperature: 1.0 (more creative responses)

Max Tokens: 1024

Streaming: Enabled

Top-p Sampling: 1.0

🖼️ UI Demo (Sample)
vbnet
Copy
Edit
User: What is the capital of France?
Bot: The capital of France is Paris.
📌 Notes
Model switching (via st.session_state.ai_model) is already supported in backend logic.

You can customize temperature, max tokens, and model easily.

📍 Future Improvements
Model selector in sidebar

System prompt customization

Markdown rendering for code answers

File upload or retrieval-augmented generation (RAG)

👨‍💻 Author
Ankit Yadav
ML Developer | GenAI & LLMs Enthusiast

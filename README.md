# AI Assistant

A fast and lightweight AI Assistant built using Flask and Groq API. It can answer user queries and summarize emails efficiently.

## Features
- Ask anything (chat interface)
- Email summarization (2–3 line summary)
- Fast responses using Groq LLMs
- Clean backend using Flask

## Tech Stack
- Python (Flask)
- Groq API (LLM inference)
- HTML, CSS (Frontend)

## Project Structure
AI-ASSISTANT/

│── main.py

│── templates/

│── static/

│── requirements.txt

│── README.md

## Setup Instructions

### 1. Clone the repo
git clone https://github.com/Ayushgit51/AI-ASSISTANT.git
cd AI-ASSISTANT

### 2. Create virtual environment
python -m venv venv
venv\Scripts\activate

### 3. Install dependencies
pip install -r requirements.txt

## Add Groq API Key

1. Go to https://console.groq.com  
2. Generate your API key  

### Option 1 (Recommended): Using .env
Create a `.env` file:
GROQ_API_KEY=your_api_key_here

In main.py:
from groq import Groq
import os
from dotenv import load_dotenv

load_dotenv()
client = Groq(api_key=os.getenv("GROQ_API_KEY"))

### Option 2 (Not recommended)
client = Groq(api_key="your_api_key_here")

## Run the App
python main.py

Open in browser:
http://127.0.0.1:5000

## API Endpoints

### /ask
Method: POST

### /summarize
Method: POST

## Models Used
- llama-3.3-70b-versatile
- llama-3.1-8b-instant

## Important
- Do NOT push your .env file  
- Add .env to .gitignore

## Future Improvements
- Voice assistant
- File/PDF summarization
- Chat history
- Deployment

## Author
Ayush Kumar  
GitHub: https://github.com/Ayushgit51

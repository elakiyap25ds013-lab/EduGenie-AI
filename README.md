

# EduGenie 🎓

EduGenie is an AI-powered educational assistant web app built with **FastAPI** and **Google Gemini API**. It helps learners summarize content, generate quizzes, get explanations, and ask questions — all from a simple web interface.

## Features

- 📄 **Summarize a Paragraph** — Paste long content and get a concise summary.
- 📝 **Generate a Quiz** — Enter a topic and get auto-generated quiz questions.
- ❓ **Ask a Question (QnA)** — Ask any question and get an AI-generated answer.
- 💡 **Explanation Module** — Get detailed explanations on topics.
- 🛤️ **Learning Path** — Generate a structured learning path for a subject.

## Tech Stack

- **Backend:** Python, FastAPI, Uvicorn
- **AI Model:** Google Gemini API (`google-generativeai` / `google-genai`)
- **Frontend:** HTML, CSS (Jinja2 templates)

## Project Structure

```
EduGenie/
├── main.py                  # FastAPI app entry point
├── gemini_client.py         # Handles Gemini API connection/calls
├── qna.py                   # Question & Answer module
├── quiz_module.py           # Quiz generation module
├── summary_module.py        # Paragraph summarization module
├── explanation_module.py    # Explanation generation module
├── learning_path.py         # Learning path generation module
├── templates/
│   └── index.html           # Main web page
├── static/
│   └── style.css             # Stylesheet
├── requirements.txt         # Python dependencies
├── .gitignore                # Files/folders excluded from Git
└── .env                      # Environment variables (API key) - not committed
```

## Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/EduGenie.git
   cd EduGenie
   ```

2. **Create a virtual environment (optional but recommended)**
   ```bash
   python -m venv venv
   venv\Scripts\activate      # Windows
   source venv/bin/activate   # macOS/Linux
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables**

   Create a `.env` file in the project root and add your Gemini API key:
   ```
   GOOGLE_API_KEY=your_api_key_here
   ```
   Get a free API key from [Google AI Studio](https://aistudio.google.com/apikey).

5. **Run the app**
   ```bash
   uvicorn main:app --reload
   ```

6. Open your browser and go to:
   ```
   http://127.0.0.1:8000/
   ```

## Notes

- The free tier of the Gemini API has a daily request quota (e.g., 20 requests/day for some models). If you see a `429 quota exceeded` error, wait for the quota to reset or use a different API key.
- Do **not** commit your `.env` file to GitHub — add it to `.gitignore` to keep your API key private.

## License

This project is open-source and available for educational purposes.

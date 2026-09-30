# Development – EduGenie source code

```
5. Project Development Phase/
├── main.py                 # FastAPI app & routes
├── gemini_client.py        # Gemini connection, retry, error handling
├── qna.py                  # Q&A
├── explanation_module.py   # Explanation (LaMini-Flan-T5)
├── summary_module.py       # Summarizer
├── quiz_module.py          # Quiz generator (JSON)
├── learning_path.py        # Learning recommendations
├── templates/index.html
├── static/style.css
├── requirements.txt
├── .env.example
└── .gitignore
```

## Run
```bash
pip install -r requirements.txt
cp .env.example .env        # then put your key in .env
uvicorn main:app --reload
```
Open http://127.0.0.1:8000/

> The variable name is **GEMINI_API_KEY** (this is what the code reads).

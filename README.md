# EduGenie – Google Gemini Powered Learning Assistant 🎓

AI-powered learning assistant built with **FastAPI** and **Google Gemini**: ask questions, get explanations, summarize text, generate quizzes and receive learning paths.

**Team:** Elakiya P (Leader) · Agalya R · Lavanya B · Nagajothi M

## Repository Structure
1. Brainstorming & Ideation
2. Requirement Analysis
3. Project Design Phase
4. Project Planning Phase
5. Project Development Phase (source code)
6. Project Testing
7. Project Documentation
8. Project Demonstration

## Quick Start
```bash
cd "5. Project Development Phase"
pip install -r requirements.txt
cp .env.example .env     # add GEMINI_API_KEY
uvicorn main:app --reload
```
Open http://127.0.0.1:8000/

## Features
Q&A · Explanation · Summary · Quiz · Learning Path

## Tech Stack
Python, FastAPI, Uvicorn, Jinja2, Google Gemini API, LaMini-Flan-T5, HTML/CSS/JS

## Notes
- Gemini free tier has a daily quota (429 errors are handled with a retry and a friendly message).
- Never commit your `.env` file.

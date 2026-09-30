# 2. Requirement Analysis

## Functional Requirements
| ID | Requirement |
|----|-------------|
| FR-1 | The user can type a question and receive an AI-generated answer (`/qa`). |
| FR-2 | The user can enter a topic and receive a simplified explanation (`/explain/`). |
| FR-3 | The user can paste text and receive a concise summary (`/summarize/`). |
| FR-4 | The system generates exactly 3 MCQs (4 options each) as JSON (`/quiz`). |
| FR-5 | The user can select an option and check whether it is correct. |
| FR-6 | The user can enter a topic and receive a beginner→advanced learning path (`/learn/recommendations`). |
| FR-7 | Empty input returns a clear error message (HTTP 400). |

## Non-Functional Requirements
| ID | Requirement |
|----|-------------|
| NFR-1 | **Usability** – single simple page, one input + one button per feature. |
| NFR-2 | **Performance** – Gemini responses shown with a "loading" message; retry on quota errors. |
| NFR-3 | **Reliability** – errors from Gemini are caught and shown as friendly messages. |
| NFR-4 | **Security** – API key is stored in `.env`, never committed to Git. |
| NFR-5 | **Maintainability** – one Python module per feature. |
| NFR-6 | **Portability** – runs locally with `uvicorn main:app --reload`. |

## Software Requirements
| Category | Requirement |
|----------|-------------|
| Language | Python 3.10+ |
| Backend | FastAPI, Uvicorn |
| Templating | Jinja2 |
| AI | Google Gemini API (`google-generativeai`), LaMini-Flan-T5-783M (`transformers`, `torch`) |
| Frontend | HTML, CSS, JavaScript (fetch API) |
| Config | `python-dotenv` |
| Tools | VS Code, Git/GitHub |

## Hardware Requirements
- Any laptop/PC, 8 GB RAM recommended (the local T5 model is loaded into memory)
- Internet connection for Gemini calls and the first-time model download

## Constraints & Assumptions
- Gemini free tier has a daily request quota (HTTP 429 possible).
- AI answers may not always be accurate and should be verified.
- The first run downloads the LaMini-Flan-T5 model.

## Dependencies (`requirements.txt`)
fastapi, uvicorn[standard], jinja2, python-multipart, python-dotenv, google-generativeai, transformers, torch, sentencepiece, accelerate

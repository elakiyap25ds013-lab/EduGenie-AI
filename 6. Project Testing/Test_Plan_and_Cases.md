# 6. Project Testing

## Approach
Manual functional testing through the web UI and API (browser / `curl` / FastAPI docs at `/docs`), followed by error-handling checks.

## Functional Test Cases
| ID | Feature | Input | Expected Result | Status |
|----|---------|-------|-----------------|--------|
| TC-01 | Q&A | "what is python" | AI-generated answer shown | ☐ |
| TC-02 | Q&A | (empty) | Browser blocks submit / API returns 400 | ☐ |
| TC-03 | Explanation | "Photosynthesis" | Short simple explanation | ☐ |
| TC-04 | Summary | Long paragraph | Concise summary | ☐ |
| TC-05 | Quiz | "Solar System" | 3 MCQs, 4 options each | ☐ |
| TC-06 | Quiz check | Correct option | "✅ Correct!" | ☐ |
| TC-07 | Quiz check | Wrong option | "❌ Incorrect" + correct answer | ☐ |
| TC-08 | Quiz check | No option selected | "Please select an option." | ☐ |
| TC-09 | Learning path | "Linear Regression" | Beginner→advanced plan + resources | ☐ |

## Error-Handling Test Cases
| ID | Scenario | Expected |
|----|----------|----------|
| ET-01 | `GEMINI_API_KEY` missing | App stops with clear RuntimeError |
| ET-02 | Gemini quota exhausted (429) | Retries, then "quota exceeded" message |
| ET-03 | Gemini returns invalid JSON for quiz | "Could not parse quiz JSON" message |
| ET-04 | Server unreachable | UI shows "⚠ Something went wrong." |

## Sample `curl` Checks
```bash
curl "http://127.0.0.1:8000/qa?question=what%20is%20python"
curl -X POST http://127.0.0.1:8000/quiz -H "Content-Type: application/json" -d '{"text":"Solar System"}'
curl "http://127.0.0.1:8000/learn/recommendations?topic=Linear%20Regression"
```

## Known Issues / Improvement Notes
- The T5-783M explanation model gives shorter, less detailed answers than Gemini.
- Generated text is inserted with `innerHTML`; escape output before rendering in a production version.
- The summary input is a single-line field; a `<textarea>` suits long paragraphs better.

## Results
Tick the **Status** column (✅ Pass / ❌ Fail) after running each test and add screenshots to this folder.

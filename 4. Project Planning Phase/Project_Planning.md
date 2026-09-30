# 4. Project Planning Phase

## Team & Roles
| Member | Role |
|--------|------|
| Elakiya P | Team Leader – coordination, backend integration, GitHub |
| Agalya R | Backend modules (Q&A, Summary) |
| Lavanya B | Quiz & Learning Path modules, testing |
| Nagajothi M | Frontend (HTML/CSS/JS), documentation |

*(Adjust roles to match who actually did what.)*

## Timeline
| Phase | Activities | Duration |
|-------|-----------|----------|
| 1. Ideation | Problem, idea, features | Week 1 |
| 2. Requirements | Functional / non-functional, tools | Week 1 |
| 3. Design | Architecture, API, UI | Week 2 |
| 4. Planning | Roles, sprints, risks | Week 2 |
| 5. Development | Gemini client, 5 modules, frontend | Weeks 3–4 |
| 6. Testing | Functional tests, bug fixes | Week 5 |
| 7. Documentation | Report, README | Week 5 |
| 8. Demonstration | Demo video / presentation | Week 6 |

## Sprint Plan
| Sprint | Goal |
|--------|------|
| 1 | Project setup, `gemini_client.py`, Q&A endpoint |
| 2 | Summary, Explanation, Learning Path modules |
| 3 | Quiz module (JSON) + frontend for all features |
| 4 | Testing, error handling, documentation, demo |

## Risk Register
| Risk | Impact | Mitigation |
|------|--------|-----------|
| Gemini quota exceeded (429) | Feature stops | Retry with back-off, friendly message, alternate key |
| Invalid quiz JSON | Quiz fails | Strict prompt + fence cleaning + error message |
| Large T5 model download / slow start | Slow first run | Document requirement; load once at startup |
| API key leak | Security | `.env` + `.gitignore` |
| Inaccurate AI answers | Wrong learning | Verify with trusted sources |

## Tools
VS Code, Git & GitHub, Python venv, Uvicorn, browser DevTools.

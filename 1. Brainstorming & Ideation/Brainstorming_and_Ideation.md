# 1. Brainstorming & Ideation

## Project: EduGenie – Google Gemini Powered Learning Assistant
**Team:** Elakiya P (Team Leader), Agalya R, Lavanya B, Nagajothi M

## Problem Statement
Students spend a lot of time searching for explanations, preparing practice questions, summarizing long passages and deciding what to study next. These tasks are spread across many websites and tools.

## Idea
One lightweight web app where a learner can **ask, understand, revise, test and plan** using generative AI.

## Ideas Considered
| # | Idea | Decision |
|---|------|----------|
| 1 | Q&A chatbot only | Too narrow – merged into the main idea |
| 2 | Quiz generator only | Useful, kept as a module |
| 3 | Notes summarizer | Useful, kept as a module |
| 4 | Concept explainer using a small local model | Kept – works without a cloud call |
| 5 | Learning-path recommender | Kept – gives structure to self-learners |
| 6 | **All-in-one learning assistant (1–5 combined)** | **Selected** |

## Target Users
- School and college students
- Self-learners preparing for exams or picking up a new subject
- Teachers who need quick quiz/summary material

## Core Features (Selected)
1. **Q&A** – answer any academic/general question in simple language
2. **Explanation** – simplify a concept (LaMini-Flan-T5 local model)
3. **Summary** – shorten long passages for revision
4. **Quiz** – 3 MCQs with 4 options each, with answer checking
5. **Learning Path** – beginner → advanced plan with resources

## Empathy Map
| Says | Thinks | Does | Feels |
|------|--------|------|-------|
| "Explain this simply" | "Where do I even start?" | Searches many sites, re-reads notes | Overwhelmed, short of time |

## Expected Outcome
A modular FastAPI + Gemini web app that saves study time and supports self-assessment.

## Future Ideas (Parked)
Voice input, multilingual support, mobile app, progress tracking, gamification, LMS integration, image/PDF input.

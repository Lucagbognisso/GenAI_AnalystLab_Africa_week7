# HealthConnect AI Assistant - Week 7

## Overview
Week 7 tested the robustness of the Week 6 HealthConnect system prompt by running 
it on two different model backends, **Gemini** and **ChatGPT**, against an 
identical 9-prompt test set. The goal was to confirm the prompt reliably guides 
assistant behavior regardless of which model runs it.

## What Was Tested
- 9 prompts (5 core Knowledge-Base questions, 4 boundary/stretch questions), 
several with adversarial or multi-turn follow-ups.
- Evaluated for correctness, groundedness, completeness, safety, and escalation 
success.

## Key Results
- **Safety:** Strong on both backends: no invented medical or clinic information; 
symptom and diagnostic questions were consistently refused.
- **Escalation:** Succeeded in most scenarios on both backends.
- **Issue found (ChatGPT backend):** Refused a reschedule question the Knowledge 
Base could already answer.
- **Weakness found (both backends):** Emergency-scenario responses repeated the 
same scripted line without acknowledging what the user had just said.

## Refinements Proposed
1. **KB-first answering** - check the Knowledge Base before declining a question; escalate only when it doesn't cover the request.
2. **Adaptive emergency acknowledgement** - acknowledge stated constraints (e.g., "can't travel tonight") instead of repeating a fixed response.

## Status
Refinements are drafted but not yet applied or retested. This is the priority carry-over into Week 8, along with closing the evidence gap and building the app that connect user and the model.

## Week 8 Priorities
- Apply and retest Refinements.
- Close the outstanding evidence gap.
- Build the public web app connecting users to the assistant.

## Files
- `week 7 work`: full Week 7 testing & refinement report.
- `Response evaluation/Model evaluation Gemini` / `Response evaluation/Model evaluation chatGPT` — raw test transcripts and scoring grilles per backend.



## Author

Luc Agbognisso

Generative AI Intern, AnalystLab Africa


*#AnalystLabAfrica*


# 📘 Technical Documentation – Interia Voice AI Assistant

## Overview
This system captures voice-based customer queries, interprets them using LLMs, stores leads in Airtable, and optionally triggers n8n automation. It also supports FAISS for memory-based retrieval of similar past projects.

---

## Workflow Summary

1. **Voice Input (.wav):**
   - Input from mic or uploaded file
   - Handled via Whisper

2. **ASR with Whisper:**
   - Transcribes audio into text
   - Uses base or small model for balance of speed and accuracy

3. **OpenAI LLM:**
   - ChatGPT-style prompt with context
   - Responds to queries and asks follow-ups

4. **FAISS Retrieval (Optional):**
   - Encodes queries using embeddings
   - Retrieves closest match from sample projects
   - Injected into prompt for personalization

5. **Lead Qualification:**
   - Entity extraction: Name, Location, Budget, Project Type
   - Checks if enough data exists to qualify

6. **Airtable Integration:**
   - Sends lead info using Airtable API
   - Maps fields manually using record IDs

7. **n8n Automation:**
   - Optional no-code flow for lead tracking or alerts
   - Exported as `n8n_workflow.json`

---

## Files & Assets

- `README.md` – Overview, instructions, and structure
- `Multi_agent_voice_system_For_Interia.ipynb` – Main code
- `requirements.txt` – All Python packages
- `n8n_workflow.json` – Visual workflow export
- `flow_diagram.png` – System diagram
- `airtable_schema.md` – Airtable field documentation

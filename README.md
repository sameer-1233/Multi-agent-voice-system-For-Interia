# Interia Voice AI Assistant

This project is a voice-enabled AI assistant designed for luxury interior design firm **Interia**. It captures voice input, interprets it using OpenAI, and stores qualified leads in Airtable. It also optionally uses **FAISS** to retrieve relevant past project examples based on user queries.

---

## 🔧 Features

- 🎤 Voice input via microphone or `.wav` file
- 🧠 OpenAI LLM for understanding user intent and preferences
- 🔍 **FAISS** vector search to retrieve similar past projects (optional)
- 📋 Airtable integration for structured lead storage
- ⚙️ Optional **n8n** workflow to automate lead handling and updates
- 🔊 Text-to-speech response using gTTS

---

## 📁 Project Contents

- `Multi_agent_voice_system_For_Interia.ipynb` – Full working notebook
- `README.md` – This documentation
- `requirements.txt` – Python dependencies
- `n8n_workflow.json` – Exported workflow from n8n
- `assets/screenshots/` – Screenshots of Airtable and n8n
- `sample_voice.wav` – (Optional) Sample voice input file
- `flow_diagram.png` – Visual overview of the full system including FAISS

---

## ✅ How to Run

1. Clone the repo or unzip the folder  
2. Install requirements:
   ```bash
   pip install -r requirements.txt

📋 **Airtable Schema:** [airtable_schema.md](./airtable_schema.md)


⚠️ Note: The OpenAI API key is **not included** in the notebook.
To run this notebook, enter your own key when prompted, or store it securely as an environment variable.

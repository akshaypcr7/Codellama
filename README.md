# Codellama


# CodeGuru — Custom Local LLM Coding Assistant

A lightweight, locally-hosted AI coding assistant built on top of **CodeLlama** using **Ollama** and **Gradio**. CodeGuru answers code-related questions through a clean chat interface and runs entirely on your own machine — no internet required after setup.

---

## What It Does

CodeGuru is a custom large language model assistant configured with a tailored system prompt that makes it behave like a focused coding tutor. You type a coding question, it gives you a clear answer. The conversation history is maintained across turns, so it remembers the context of your session.

---

## Tech Stack

| Component | Technology |
|---|---|
| Base Model | CodeLlama (via Ollama) |
| Custom Persona | Ollama Modelfile |
| UI | Gradio |
| API | Ollama REST API (localhost:11434) |
| Language | Python |

---

## Project Structure

```
├── app.py              # Gradio UI and Ollama API integration
├── modelfile           # Custom Ollama model configuration
└── requirements.txt    # Python dependencies
```

---

## Getting Started

### Prerequisites

- [Ollama](https://ollama.com) installed on your machine
- Python 3.8+
## How It Works

1. The `modelfile` extends `codellama` with a custom system prompt, giving the model a focused coding tutor persona and setting the temperature to 1 for varied responses.
2. `app.py` sends user prompts to the locally running Ollama model via HTTP POST requests to `localhost:11434`.
3. Conversation history is maintained in memory so the model retains context across multiple turns in the same session.
4. Gradio provides the front-end chat interface.

---

## Example Usage

> **You:** How do I reverse a list in Python?
>
> **CodeGuru:** You can reverse a list in Python in a few ways...

---

## Dependencies

```
gradio
langchain
```
---

## Notes

- This project runs fully offline after the initial model download.
- The model and persona can be customised by editing the `modelfile`.
- Conversation history resets when the app is restarted.

---

## Author

**Akshay Pisal** — [LinkedIn](https://linkedin.com/in/akshaypisal) | [GitHub](https://github.com/akshaypisal)

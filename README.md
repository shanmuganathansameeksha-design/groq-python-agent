# Groq Python Agent

A simple Python agent powered by Groq's LLM API with tool calling.

Features:
- Groq chat completions integration
- ReAct-style tool-calling loop
- Built-in tools: `web_search`, `calculator`, and `current_time`
- Easy to extend with more tools
- Works with a `GROQ_API_KEY` environment variable

## Quick start

1. Create a virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Set your Groq API key:

```bash
cp .env.example .env
# edit .env and add your Groq API key
```

4. Run the agent:

```bash
python agent.py
```

Example prompts:
- `What is 42 * 7?`
- `Search the web for Python agents and summarize what they do.`
- `Tell me the current time and calculate 15 + 22.`

## Files
- `agent.py` - main agent logic
- `.env.example` - example environment variables
- `requirements.txt` - Python dependencies

## Notes
- The web search tool is intentionally lightweight and easy to replace with a real search service if needed.
- The default model is `llama-3.3-70b-versatile`, but you can change it with `GROQ_MODEL`.

# langchain-chains

LangChain chain examples (simple, sequential, parallel, conditional), 
to run on [OpenRouter](https://openrouter.ai) with a single `OPENROUTER_API_KEY`.

## Setup

```bash
python -m venv venv && source venv/bin/activate
pip install -r requirements.txt
cp .env.example .env   # then put your OpenRouter key in .env
```

## Run

```bash
python simple_chain.py
python sequential_chain.py
python parallel_chain.py
python conditional_chain.py
```

## Changes from the original

- Models are created via `models.py` and routed through OpenRouter (`openai/gpt-4o-mini`; `anthropic/claude-haiku-4.5` in the parallel chain).
- `langchain.schema.runnable` imports replaced with `langchain_core.runnables`.
- `conditional_chain.py`: fixed the branch so the original feedback text is passed to the response prompts, and fixed a typo.

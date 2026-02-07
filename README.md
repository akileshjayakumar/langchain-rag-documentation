# LangChain RAG Documentation Notebook

Build and evaluate a retrieval-augmented generation (RAG) pipeline over LangChain docs in a single Jupyter notebook.

## Quick Start

### Prerequisites
- Python 3.10+
- Jupyter Notebook or JupyterLab

### Install
```bash
python3 -m venv .venv
source .venv/bin/activate
python3 -m pip install -U pip
python3 -m pip install jupyter langchain langsmith langchainhub langchain_benchmarks chromadb openai huggingface pandas langchain_experimental sentence_transformers pyarrow anthropic tiktoken
```

### Run
```bash
jupyter notebook rag-over-langchain-docs.ipynb
```

## Features
- Loads the public **LangChain Docs Q&A** retrieval benchmark task.
- Builds a Chroma vector store using HuggingFace embeddings (`thenlper/gte-base`).
- Runs a question-answering chain grounded in retrieved documents.

## Configuration
Set these environment variables before running cells that query models or LangSmith:

- `LANGCHAIN_API_KEY`: LangSmith API key.
- `LANGCHAIN_ENDPOINT`: set to `https://api.smith.langchain.com`.
- `OPENAI_API_KEY`: OpenAI API key for `ChatOpenAI`.
- `ANTHROPIC_API_KEY`: optional, if using Anthropic models in experiments.
- `TOKENIZERS_PARALLELISM`: recommended `false` to reduce tokenizer warnings.

## Usage
After the notebook builds the retriever and chain, run:

```python
chain.invoke({"question": "Tell me how a chain works in LangChain. In 3 sentences."})
```

This returns an answer constrained to retrieved LangChain documentation context.

## Contributing and Testing
This repo is notebook-first. Keep changes reproducible by running the notebook from top to bottom in a clean environment and verifying key cells (indexing + `chain.invoke`) execute successfully.

## License
Licensed under the `MIT` license. See [LICENSE](./LICENSE) for full text.

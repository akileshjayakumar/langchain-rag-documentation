# LangChain RAG Documentation Notebook
Build and evaluate a retrieval-augmented generation (RAG) pipeline over LangChain docs in a single Jupyter notebook.

## Quick Start
```bash
python3 -m venv .venv
source .venv/bin/activate
python3 -m pip install -U pip
python3 -m pip install jupyter langchain langsmith langchainhub langchain_benchmarks chromadb openai huggingface pandas langchain_experimental sentence_transformers pyarrow anthropic tiktoken
```

## Capabilities
- Python 3.10+
- Jupyter Notebook or JupyterLab
- Loads the public **LangChain Docs Q&A** retrieval benchmark task.
- Builds a Chroma vector store using HuggingFace embeddings (`thenlper/gte-base`).

## Configuration
- `ANTHROPIC_API_KEY`: Required for related integrations/features.
- `LANGCHAIN_API_KEY`: Required for related integrations/features.
- `OPENAI_API_KEY`: Required for related integrations/features.

## Usage
```bash
jupyter notebook rag-over-langchain-docs.ipynb
```

## Contributing and Testing
- Contributions are welcome through pull requests with clear, scoped changes.
- No automated test suite is currently documented for this repository.

## License
Licensed under the `MIT` license. See [LICENSE](./LICENSE) for full text.

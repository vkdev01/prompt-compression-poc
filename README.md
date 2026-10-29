# Prompt Compression POC

Input-token compression experiments with **Selective Context** and **LLMLingua-2**, including cost tracking, RAG/chat/long-doc scenarios, and a production service/FastAPI design.

## Structure

```
prompt-compression-poc/
├── prompt_compression_poc.ipynb   # main notebook (run from this folder)
├── models/                        # local model weights (git-ignored)
│   ├── gpt2/
│   └── llmlingua-2-xlm-roberta-large-meetingbank/
├── outputs/                       # generated charts
├── requirements.txt
├── .env.example                   # copy to .env and fill in
└── final.pem                      # corporate CA bundle (git-ignored)
```

## Setup

```bash
python -m venv .venv && source .venv/bin/activate
pip install selective-context --no-deps
pip install -r requirements.txt
python -m spacy download en_core_web_sm
cp .env.example .env   # fill in credentials
```

Models are downloaded into `models/` by the notebook (`download_hf_model`). `gpt2` must be placed at `models/gpt2`.

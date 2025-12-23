Prerequisites

```sh
set PATH "/usr/bin:$PATH"; uv pip install --system -U assemblyai colpali-engine'>0.3.12' docling fast-plaid fastkmeans flagembedding'>1.3.4' litellm morphik_rust pymupdf
```

Start db

```sh
docker compose -f redis-and-pg.yml up
```

Ollama

```sh
ollama serve
```

Backend

```sh
python start_server.py
```

Frontend

```sh
cd ee/ui-component
bun i && bun run build --no-lint && bun start
```

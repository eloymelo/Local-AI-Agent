# Local AI Agent

A Docker-based setup combining **LM Studio**, **OpenWebUI**, and **SearXNG** 
for a local AI assistant with web search capabilities.

## Stack
| Component | Role |
|-----------|------|
| [LM Studio](https://lmstudio.ai) | Runs local LLMs |
| [Open WebUI](https://github.com/open-webui/open-webui) | Chat interface |
| [SearXNG](https://github.com/searxng/searxng) | Privacy-focused web search |

---

## Requirements
- [Docker](https://www.docker.com/) and Docker Compose
- [LM Studio](https://lmstudio.ai/download) installed
- A compatible LLM model (see [Recommended Models](#recommended-models))

---

## Installation

### 1. Clone the repository
```bash
git clone https://github.com/eloymelo/Local-AI-Agent
cd Local-AI-Agent
```

### 2. Start SearXNG
```bash
cd searxng
docker compose up -d
```

> This creates two folders inside `searxng/`: `config/` and `data/`

### 3. Configure SearXNG
1. Open `./searxng/config/settings.yml`
2. Copy the value of `secret_key`
3. Delete `settings.yml`
4. Rename `example_settings.yml` to `settings.yml`
5. Paste your `secret_key` into the new file

### 4. Restart SearXNG
```bash
docker compose down && docker compose up -d
```

### 5. Verify
SearXNG should now be available at `http://localhost:8888`

---

## Recommended Models
- **General use**: Qwen2.5-14B-Instruct Q4_K_M
- **Coding**: Qwen2.5-Coder-14B-Instruct Q4_K_M
- **Vision**: Gemma-4-26B

---

## Docs
- [Full Setup Guide](docs/setup.md)
- [Troubleshooting](docs/troubleshooting.md)
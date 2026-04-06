# Open WebUI

Web-based chat interface for LM Studio with SearXNG search integration.
Requires an Nvidia GPU for the CUDA image.

## Ports
| Port | Purpose |
|------|---------|
| 3000 | Web UI |

## Usage
```bash
docker compose up -d
```

Access Open WebUI at `http://localhost:3000`

## Notes
- Requires Nvidia GPU and CUDA drivers installed on the host
- LM Studio must be running and listening on port 1234 before connecting
- SearXNG query URL: `http://host.docker.internal:8888/search?q=<query>&format=json`
- Data persisted via named volume `open-webui`
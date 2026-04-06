# SearXNG

Privacy-focused metasearch engine integrated as the web search backend for Open WebUI.

## Ports
| Port | Purpose |
|------|---------|
| 8888 | Web UI |

## Usage
1. Start the container:
```bash
docker compose up -d
```
2. Open `./config/settings.yml` and copy the `secret_key` value
3. Delete `settings.yml`
4. Rename `example_settings.yml` to `settings.yml` and move it to `./config/`
5. Paste your `secret_key` into the new file
6. Restart the container:
```bash
docker compose down && docker compose up -d
```

## Notes
- Config persisted in `./config/`, cache in `./data/`
- Available at `http://localhost:8888`
- JSON search endpoint used by Open WebUI: `/search?q=<query>&format=json`
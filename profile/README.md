# Ujeebu

**One API for web data.** Scrape any page with headless Chrome and rotating proxies, get Google results as JSON, turn pages into clean Markdown for LLMs, and capture ChatGPT and Gemini answers with their citations. One API key, one credit pool.

[Website](https://ujeebu.com) · [Docs](https://ujeebu.com/docs) · [Playground](https://ujeebu.com/playground) · [Pricing](https://ujeebu.com/pricing) · [MCP server](https://ujeebu.com/mcp)

## Endpoints

| Endpoint | What it does |
|---|---|
| `GET /scrape` | Fetch any URL with JavaScript rendering, rotating datacenter, premium or residential proxies, and anti-bot handling. Returns HTML, text, a screenshot or a PDF. |
| `GET /serp` | Google organic, news, images, videos, places and AI Mode results as structured JSON, by country and language. |
| `GET /markdown` | Clean, chunked Markdown from any page, ready for RAG pipelines. |
| `POST /extract` | Article title, author, date, body text and images. |
| `POST /chatgpt`, `POST /gemini` | Submit a prompt, get the answer text and citations as JSON. |
| MCP | Every endpoint as a typed tool for Claude, Cursor and other agents at `mcp.ujeebu.com`. |

You only pay for successful requests: blocked requests, timeouts and server errors are free.

## SDKs and integrations

| Repo | Package |
|---|---|
| [ujeebu-python](https://github.com/ujeebu/ujeebu-python) | `pip install ujeebu-python` |
| [ujeebu-node](https://github.com/ujeebu/ujeebu-node) | `npm install @ujeebu-org/ujeebu-sdk` |
| [ujeebu-go](https://github.com/ujeebu/ujeebu-go) | `go get github.com/ujeebu/ujeebu-go` |
| [ujeebu-scrapy](https://github.com/ujeebu/ujeebu-scrapy) | Scrapy middleware: `pip install ujeebu-scrapy` |
| [ujeebu-langchain-py](https://github.com/ujeebu/ujeebu-langchain-py) | LangChain (Python): `pip install langchain-ujeebu` |
| [ujeebu-langchain-js](https://github.com/ujeebu/ujeebu-langchain-js) | LangChain (JavaScript): `npm install @ujeebu-org/langchain` |
| [ujeebu-n8n](https://github.com/ujeebu/ujeebu-n8n) | n8n community node: `n8n-nodes-ujeebu` |
| [ujeebu-tutorials](https://github.com/ujeebu/ujeebu-tutorials) | Runnable code for the how-to tutorials in cURL, Python, JavaScript, PHP and Go |

## Quick start

```bash
curl -X POST "https://api.ujeebu.com/scrape" \
  -H "ApiKey: YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"url": "https://example.com", "js": true}'
```

Start with a 7-day trial: 5,000 credits, no credit card. [Get a key](https://ujeebu.com/signup).

<p align="center">
  <a href="https://0g.ai">
    <img src="https://cdn.prod.website-files.com/680b884d38733122a923739b/68789e2725add3b7788ad45a_0G-Logo-Purple_Hero.avif" alt="0G Network" width="180"/>
  </a>
</p>

<h1 align="center">0G Compute Adapter</h1>


<p align="center">
  <strong>Cut your AI coding costs by up to 90% — use 0G models in Cursor, Claude Code, Aider, and more</strong>
</p>

<p align="center">
  Drop-in OpenAI-compatible proxy that routes your AI dev tools through the <a href="https://0g.ai">0G Network</a>, where models like GLM-5, DeepSeek V3, and GPT-OSS cost a fraction of what you pay today. Same tools, same workflow, massively lower bill.
</p>

<h5 align="center"><p><b>Note</b>: Not in anyway this repo is associated with Official 0G, its basically I love the low compute inference cost so i had to contribute, so people can use it more</p></h5>


<p align="center">
  <a href="#quick-start">Quick Start</a>&nbsp;&nbsp;&bull;&nbsp;&nbsp;<a href="#pricing-comparison">Pricing</a>&nbsp;&nbsp;&bull;&nbsp;&nbsp;<a href="#dashboard">Dashboard</a>&nbsp;&nbsp;&bull;&nbsp;&nbsp;<a href="#usage-examples">Examples</a>&nbsp;&nbsp;&bull;&nbsp;&nbsp;<a href="#api-reference">API Reference</a>&nbsp;&nbsp;&bull;&nbsp;&nbsp;<a href="#how-tool-calling-works">How It Works</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT"/>
  <img src="https://img.shields.io/badge/node-%3E%3D18-brightgreen" alt="Node.js 18+"/>
  <img src="https://img.shields.io/badge/Docker-ready-blue" alt="Docker"/>
  <img src="https://img.shields.io/badge/Single_file-1400_LOC-orange" alt="Single File"/>
  <img src="https://img.shields.io/badge/0G-Mainnet-7c3aed" alt="0G Mainnet"/>
</p>

<br/>

<p align="center">
  <img src="assets/screenshots/dashboard.png" alt="0G Compute Adapter Dashboard" width="900"/>
</p>

---

## Why 0G Compute Adapter?

AI coding assistants are expensive. A power user on Claude Code or Cursor can easily burn through **$200-$300/month** on API calls. Most of that spend goes to proprietary model pricing with huge margins.

The [0G Compute Network](https://0g.ai) offers the same class of models — GLM-5, DeepSeek V3, GPT-OSS 120B, Qwen3 — through a decentralized network of GPU providers, at a fraction of the cost. The problem: the raw network only speaks basic chat completions, and your dev tools expect the full OpenAI API.

**0G Compute Adapter** bridges that gap. It gives you full OpenAI compatibility (tool calling, streaming, structured output, vision) on top of 0G's cheap inference. Point your tools at it and keep working exactly as before — just pay 70-90% less.

## Pricing Comparison

<a id="pricing-comparison"></a>

### 0G Network Pricing (in 0G tokens)

Pricing is denominated in **0G tokens**. At the current market rate (~$0.06/token), actual USD costs are even lower.

| Model | Input (per 1M tokens) | Output (per 1M tokens) | ~USD Equivalent (in/out) |
|---|---|---|---|
| **GLM-5** | 1.0 0G | 3.2 0G | ~$0.60 / ~$1.92 |
| **DeepSeek V3** | 0.5 0G | 1.5 0G | ~$0.30 / ~$0.90 |
| **GPT-OSS 120B** | 0.8 0G | 2.4 0G | ~$0.48 / ~$1.44 |
| **Qwen3 VL** | 0.5 0G | 1.5 0G | ~$0.30 / ~$0.90 |
| **Z-Image** | 0.02 0G/image | — | ~$0.012/image |
| **Whisper** | 0.01 0G/min | — | ~$0.006/min |

---

**Change one line of code** — your `base_url` — and start saving immediately:

```python
from openai import OpenAI

client = OpenAI(
    base_url="http://localhost:8000/v1",  # <- that's it
    api_key="your-api-key",
)
```

## Use with AI Dev Tools

Works anywhere that supports custom OpenAI-compatible endpoints — set the base URL to `http://localhost:8000/v1` and go.

<table>
<tr>
<td align="center" width="120">
<a href="docs/cursor.md">
<img src="https://cursor.com/apple-touch-icon.png" alt="Cursor" width="40"/><br/>
<strong>Cursor</strong>
</a>
</td>
<td align="center" width="120">
<a href="docs/windsurf.md">
<img src="https://raw.githubusercontent.com/Exafunction/codeium.vim/main/windsurf.png" alt="Windsurf" width="40"/><br/>
<strong>Windsurf</strong>
</a>
</td>
<td align="center" width="120">
<a href="docs/cline.md">
<img src="https://raw.githubusercontent.com/cline/cline/main/assets/icons/icon.png" alt="Cline" width="40"/><br/>
<strong>Cline</strong>
</a>
</td>
<td align="center" width="120">
<a href="docs/roo-code.md">
<img src="https://raw.githubusercontent.com/RooCodeInc/Roo-Code/main/src/assets/icons/icon.png" alt="Roo Code" width="40"/><br/>
<strong>Roo Code</strong>
</a>
</td>
<td align="center" width="120">
<a href="docs/vscode-continue.md">
<img src="https://raw.githubusercontent.com/continuedev/continue/main/extensions/vscode/media/icon.png" alt="Continue" width="40"/><br/>
<strong>Continue</strong>
</a>
</td>
<td align="center" width="120">
<a href="docs/claude-code.md">
<img src="https://upload.wikimedia.org/wikipedia/commons/8/8a/Claude_AI_logo.svg" alt="Claude Code" width="40"/><br/>
<strong>Claude Code</strong>
</a>
</td>
<td align="center" width="120">
<a href="docs/aider.md">
<img src="https://aider.chat/assets/logo.svg" alt="Aider" width="40"/><br/>
<strong>Aider</strong>
</a>
</td>
<td align="center" width="120">
<a href="docs/open-webui.md">
<img src="https://raw.githubusercontent.com/open-webui/open-webui/main/static/favicon.png" alt="Open WebUI" width="40"/><br/>
<strong>Open WebUI</strong>
</a>
</td>
<td align="center" width="120">
<a href="docs/litellm.md">
<img src="https://raw.githubusercontent.com/BerriAI/litellm/main/docs/my-website/static/img/logo.svg" alt="LiteLLM" width="40"/><br/>
<strong>LiteLLM</strong>
</a>
</td>
</tr>
</table>

> Click any tool above for a step-by-step setup guide. Most tools just need the base URL (`http://localhost:8000/v1`) and your API key.

## Features

| | Feature | Description |
|---|---|---|
| **API** | Full OpenAI compatibility | `/v1/chat/completions`, `/v1/models`, `/v1/images/generations`, `/v1/audio/transcriptions` |
| **Tools** | Tool calling emulation | Model-specific prompt strategies for GLM-5, DeepSeek, Qwen. 9+ output format parsers |
| **JSON** | Structured output | `json_schema` and `json_object` response formats with schema enforcement |
| **Stream** | Native streaming | SSE pass-through for real-time responses, simulated streaming for post-processed responses |
| **Vision** | Auto-routing | Send images to any model — automatically routes to Qwen3-VL |
| **Image** | Image generation | OpenAI-compatible endpoint via Z-Image on the 0G network |
| **Audio** | Transcription | Whisper Large V3 via standard `/v1/audio/transcriptions` |
| **Dashboard** | Admin UI | Real-time stats, model browser, playground, logs, wallet management |
| **Auth** | API key management | Multi-key auth, per-key rate limiting, create/revoke from dashboard |
| **Cost** | Usage tracking | Per-model pricing, per-request cost, total spend, CSV export |
| **Wallet** | 0G token management | Deposit, transfer to providers, balance monitoring, low-balance alerts |
| **Claude** | Anthropic API built-in | Native `/v1/messages` endpoint — Claude Code connects directly, no proxy needed |
| **Logs** | Persistent logging | JSONL logs with level/category filters, searchable from dashboard |

## Quick Start

### Prerequisites

- **Node.js 18+** (or Docker)
- **Ethereum wallet** with [0G tokens](https://0g.ai) on 0G mainnet

### Option 1: Docker (recommended)

```bash
git clone https://github.com/claraverse-space/0G-Compute-Adapter.git
cd og-proxy
cp .env.example .env
# Edit .env — add your wallet private key
docker compose up -d
```

### Option 2: Node.js

```bash
git clone https://github.com/claraverse-space/0G-Compute-Adapter.git
cd og-proxy
npm install
cp .env.example .env
# Edit .env — add your wallet private key
npm start
```

### Verify

```bash
curl http://localhost:8000/v1/models \
  -H "Authorization: Bearer YOUR_API_KEY"
```

Your API key is printed in the startup logs. Open `http://localhost:8000` for the admin dashboard.

## Supported Models

Models are **auto-discovered** from the 0G mainnet and refreshed every 5 minutes.

| Model | ID | Type | Capabilities |
|---|---|---|---|
| **GLM-5** | `zai-org/GLM-5-FP8` | Chat | Tool calling, reasoning, streaming |
| **DeepSeek V3** | `deepseek/deepseek-chat-v3-0324` | Chat | Tool calling, streaming |
| **GPT-OSS 120B** | `openai/gpt-oss-120b` | Chat | General purpose, streaming |
| **Qwen3 VL 30B** | `qwen/qwen3-vl-30b-a3b-instruct` | Chat + Vision | Image understanding, tool calling |
| **Whisper Large V3** | `openai/whisper-large-v3` | Speech-to-Text | Audio transcription |
| **Z-Image** | `z-image` | Text-to-Image | Image generation |

## Dashboard

Full-featured admin dashboard with real-time monitoring, built-in playground, and wallet management. Access it at `http://localhost:8000` with your API key or admin key.

### Overview — Real-time usage stats, cost tracking, 24h usage chart, per-model breakdowns

<p align="center">
  <img src="assets/screenshots/dashboard.png" alt="Dashboard — real-time stats, usage chart, per-model breakdown" width="900"/>
</p>

### Models — Auto-discovered from 0G network with capability badges

<p align="center">
  <img src="assets/screenshots/modelslist.jpg" alt="Models — auto-discovered with capability badges" width="900"/>
</p>

### Playground — Test any model with streaming, tool calling, vision, image gen

<p align="center">
  <img src="assets/screenshots/playground.png" alt="Playground — test chat, vision, image generation, audio" width="900"/>
</p>

### Logs — Persistent JSONL log viewer with level and category filters

<p align="center">
  <img src="assets/screenshots/Logs.png" alt="Logs — searchable persistent log viewer" width="900"/>
</p>

## Usage Examples

### Chat Completion

```python
from openai import OpenAI

client = OpenAI(
    base_url="http://localhost:8000/v1",
    api_key="your-api-key",
)

response = client.chat.completions.create(
    model="zai-org/GLM-5-FP8",
    messages=[{"role": "user", "content": "What is the 0G network?"}],
)
print(response.choices[0].message.content)
```

### Tool Calling

```python
response = client.chat.completions.create(
    model="zai-org/GLM-5-FP8",
    messages=[{"role": "user", "content": "What's the weather in Tokyo?"}],
    tools=[{
        "type": "function",
        "function": {
            "name": "get_weather",
            "description": "Get current weather for a city",
            "parameters": {
                "type": "object",
                "properties": {"city": {"type": "string"}},
                "required": ["city"],
            },
        },
    }],
)

# Works exactly like OpenAI — tool_calls in the response
for tc in response.choices[0].message.tool_calls:
    print(f"{tc.function.name}({tc.function.arguments})")
```

### Streaming

```python
stream = client.chat.completions.create(
    model="zai-org/GLM-5-FP8",
    messages=[{"role": "user", "content": "Count from 1 to 10."}],
    stream=True,
)
for chunk in stream:
    if chunk.choices[0].delta.content:
        print(chunk.choices[0].delta.content, end="")
```

### Structured Output (JSON Schema)

```python
response = client.chat.completions.create(
    model="zai-org/GLM-5-FP8",
    messages=[{"role": "user", "content": "List 3 programming languages"}],
    response_format={
        "type": "json_schema",
        "json_schema": {
            "name": "languages",
            "schema": {
                "type": "object",
                "properties": {
                    "languages": {
                        "type": "array",
                        "items": {"type": "object", "properties": {
                            "name": {"type": "string"},
                            "year": {"type": "integer"},
                        }},
                    }
                },
            },
        },
    },
)
# Returns clean JSON matching your schema
```

### Vision

```python
# Send to any model — auto-routes to Qwen3-VL when images are detected
response = client.chat.completions.create(
    model="zai-org/GLM-5-FP8",
    messages=[{
        "role": "user",
        "content": [
            {"type": "text", "text": "What's in this image?"},
            {"type": "image_url", "image_url": {"url": "https://example.com/photo.png"}},
        ],
    }],
)
```

### Image Generation

```python
response = client.images.generate(
    model="z-image",
    prompt="A futuristic city with flying cars",
    n=1,
    size="1024x1024",
)
print(response.data[0].url)
```

### Audio Transcription

```python
with open("audio.mp3", "rb") as f:
    response = client.audio.transcriptions.create(
        model="whisper-large-v3",
        file=f,
    )
print(response.text)
```

### Node.js

```javascript
import OpenAI from "openai";

const client = new OpenAI({
  baseURL: "http://localhost:8000/v1",
  apiKey: "your-api-key",
});

const response = await client.chat.completions.create({
  model: "zai-org/GLM-5-FP8",
  messages: [{ role: "user", content: "Hello from 0G!" }],
});
console.log(response.choices[0].message.content);
```

### curl

```bash
curl http://localhost:8000/v1/chat/completions \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "zai-org/GLM-5-FP8",
    "messages": [{"role": "user", "content": "Hello!"}],
    "stream": true
  }'
```

See the [`examples/`](examples/) directory for complete runnable scripts.

## Configuration

| Variable | Required | Default | Description |
|---|---|---|---|
| `OG_PRIVATE_KEY` | **Yes** | — | Ethereum private key with 0G tokens |
| `OG_API_KEYS` | No | Auto-generated | Comma-separated client API keys |
| `OG_ADMIN_KEY` | No | Auto-generated | Admin key for dashboard & wallet management |
| `OG_RPC_URL` | No | `https://evmrpc.0g.ai` | 0G mainnet RPC endpoint |
| `OG_RATE_LIMIT` | No | `60` | Max requests per minute per API key |
| `OG_LOG_DIR` | No | `./logs` | Directory for persistent JSONL logs |
| `PORT` | No | `8000` | Server port |

API keys and admin key are printed to the console on startup. If not set via environment variables, they are auto-generated and persisted in `logs/api-keys.json`.

## API Reference

### OpenAI-Compatible Endpoints

All endpoints require an API key via `Authorization: Bearer <key>` header.

| Method | Endpoint | Description |
|---|---|---|
| `GET` | `/v1/models` | List available models |
| `POST` | `/v1/chat/completions` | Chat completion — OpenAI format (streaming & non-streaming) |
| `POST` | `/v1/messages` | Chat completion — Anthropic format (Claude Code, Anthropic SDK) |
| `POST` | `/v1/images/generations` | Generate images |
| `POST` | `/v1/audio/transcriptions` | Transcribe audio |

### Management Endpoints

Require the admin key.

| Method | Endpoint | Description |
|---|---|---|
| `GET` | `/api/usage` | Usage statistics, cost data, recent requests |
| `GET` | `/api/wallet` | Wallet balance and provider sub-accounts |
| `POST` | `/api/deposit` | Deposit 0G tokens into the inference ledger |
| `POST` | `/api/transfer` | Transfer funds to a provider sub-account |
| `GET` | `/api/models` | Detailed model info with provider addresses |
| `GET` | `/api/logs` | Query persistent JSONL logs |
| `GET` | `/api/keys` | List all API keys |
| `POST` | `/api/keys` | Create a new API key |
| `DELETE` | `/api/keys/:key` | Revoke an API key |
| `GET` | `/api/export/usage` | Export usage data as CSV |

### Public Endpoints

| Method | Endpoint | Description |
|---|---|---|
| `GET` | `/health` | Health check (`{"status":"healthy","models":N}`) |
| `GET` | `/` | Admin dashboard UI |

## How Tool Calling Works

Models on the 0G network don't natively support OpenAI's tool calling protocol. The adapter solves this transparently in three steps:

**1. Prompt injection** — When your request includes `tools`, the adapter injects tool definitions into the system prompt using model-specific formatting:
  - **GLM-5**: `<tool_call>` XML format (the model's native preference)
  - **DeepSeek/Qwen**: ` ```tool_calls``` ` JSON format

**2. Response parsing** — The model's free-text response is parsed for tool calls. The parser handles **9+ output formats** that models produce in the wild:

| Format | Example |
|---|---|
| ` ```tool_calls [JSON] ``` ` | Standard backtick format |
| `<tool_call>{"name":...}</tool_call>` | XML with JSON body |
| `<tool_call>func({"key":"val"})</tool_call>` | Function call syntax |
| `<tool_call>func\nkey: value</tool_call>` | YAML-style arguments |
| Bare `[{"name":...}]` JSON | Embedded in text |
| `</think>` prefix | After reasoning block |
| Mixed tag formats | Broken/partial XML tags |

**3. Format conversion** — Parsed tool calls are converted to standard OpenAI format. Your app never sees the intermediate formats. Multi-turn agentic loops work automatically.

## Deployment

### Docker Compose (recommended)

```bash
git clone https://github.com/claraverse-space/0G-Compute-Adapter.git
cd og-proxy
cp .env.example .env
# Edit .env with your private key
docker compose up -d
```

### Production with Nginx

Put Nginx in front for TLS, rate limiting, and public access:

```nginx
server {
    listen 443 ssl;
    server_name your-domain.com;

    ssl_certificate     /path/to/cert.pem;
    ssl_certificate_key /path/to/key.pem;

    location / {
        proxy_pass http://127.0.0.1:8000;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection "upgrade";
        proxy_buffering off;          # Required for SSE streaming
        proxy_read_timeout 300s;
        client_max_body_size 25m;     # For audio file uploads
    }
}
```

### Security Checklist

- [ ] Set strong `OG_API_KEYS` and `OG_ADMIN_KEY` (don't use auto-generated in production)
- [ ] Put behind Nginx with TLS
- [ ] Restrict firewall to ports 80/443 only
- [ ] Use encrypted storage for the `.env` file
- [ ] Monitor wallet balance — models consume 0G tokens per request

## Architecture

```
og-proxy/
  server.js            # The entire proxy — intentionally single-file (~1400 LOC)
  public/
    index.html          # Admin dashboard (single-page app)
  docs/
    cursor.md           # Cursor setup guide
    windsurf.md         # Windsurf setup guide
    cline.md            # Cline setup guide
    roo-code.md         # Roo Code setup guide
    vscode-continue.md  # Continue (VS Code/JetBrains) setup guide
    claude-code.md      # Claude Code setup guide
    aider.md            # Aider setup guide
    open-webui.md       # Open WebUI setup guide
    litellm.md          # LiteLLM setup guide
  examples/
    python-client.py    # Python + OpenAI SDK examples
    node-client.mjs     # Node.js examples
    curl-examples.sh    # curl examples for every endpoint
  assets/               # Logos and screenshots
  .env.example          # Configuration template
  docker-compose.yml    # One-command Docker deployment
  Dockerfile            # Container build
```

The single-file architecture is a **deliberate design choice**. One file means:
- **Easy to audit** — read the entire proxy in one sitting
- **Easy to deploy** — copy one file, `npm install`, done
- **Easy to fork** — modify behavior without navigating a dependency tree
- **Easy to understand** — clear section banners, no abstraction layers

Three dependencies: `express` (HTTP), `ethers` (0G blockchain), `@0glabs/0g-serving-broker` (0G SDK).

## Contributing

We welcome contributions. See [CONTRIBUTING.md](CONTRIBUTING.md) for development setup and guidelines.

## License

MIT License. See [LICENSE](LICENSE).

---

<p align="center">
  Built by <a href="https://claraverse.ai"><strong>Claraverse</strong></a>
  &nbsp;&bull;&nbsp;
  Powered by <a href="https://0g.ai"><strong>0G Network</strong></a>
</p>

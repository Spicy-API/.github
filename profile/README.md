<div align="center">

# SpicyAPI

**One API for image, video and text models — including the uncensored ones.**

[Get an API key](https://spicyapi.ai) · [Models](https://spicyapi.ai/models) · [Docs](https://docs.spicyapi.ai) · [Status](https://status.spicyapi.ai)

</div>

---

## What this is

A single endpoint in front of **83 model families across 121 callable endpoints**. One key, one
request shape, one bill — instead of an account, a contract and a client library per provider.

Two things are unusual enough to state plainly:

- **No content review on our side.** What a model will produce is decided by the model you pick, not
  by a per-request declaration or an approval queue. Every model page carries the filtering tier we
  measured for it, so you can tell before you spend.
- **Cash pricing, no credit system.** Prices are in USD and quoted per request. You can ask what a
  call will cost *before* you make it, and the quote is what gets held.

## Models

| | |
|---|---|
| 🎬 **Video** | Seedance 2.5 · Seedance 2.0 · MiniMax H3 · Wan 2.7 · LTX 2.5 · Vidu Q3 · Krea 2 · HappyHorse 1.1 |
| 🎨 **Image** | Seedream 5.0 Pro · Qwen Image 3.0 · Z-Image · Face Swap · Head Swap · Prefect Pony XL |
| 💬 **Text** | Claude Opus 5 · Gemini 3.1 Pro · DeepSeek V4 Pro · Kimi K3 · GLM 5.3 · Grok 4.6 |
| 🎧 **Audio** | HeartMuLa Transcribe |

27 of those 121 endpoints are LoRA-tuned for adult work. They live in their own families, priced and
documented separately, so nothing about them leaks into the general catalogue. [Browse the full catalogue »](https://spicyapi.ai/models)

## Build with it

| | Install | |
|---|---|---|
| **TypeScript** | `npm i @spicyapi/sdk` | [spicy-devkit](https://github.com/Spicy-API/spicy-devkit) |
| **Python** | `pip install spicyapi` | [spicy-python](https://github.com/Spicy-API/spicy-python) |
| **Go** | `go get github.com/Spicy-API/spicy-go` | [spicy-go](https://github.com/Spicy-API/spicy-go) |
| **PHP** | `composer require spicyapi/spicyapi` | [spicy-php](https://github.com/Spicy-API/spicy-php) |
| **Java** | `ai.spicyapi:spicyapi-java` | [spicy-java](https://github.com/Spicy-API/spicy-java) |

Also shipped: a **CLI** (`npx @spicyapi/cli`), an **MCP server** so agents can generate media
directly, and an **Agent Skill** for Claude.

```bash
npx @spicyapi/cli status        # no key needed
npx @spicyapi/cli models list
```

## How a generation goes

```
quote  →  create (202, funds held)  →  poll or webhook  →  settle at the real cost
```

Media generation is asynchronous and every task is quotable first. The hold is an estimate; you are
charged what it actually cost, never more than the hold. Text models speak the OpenAI, Anthropic and
Gemini wire formats, so existing clients work by changing the base URL.

<div align="center">
<sub>

[spicyapi.ai](https://spicyapi.ai) · [docs](https://docs.spicyapi.ai) · [support@spicyapi.ai](mailto:support@spicyapi.ai)

</sub>
</div>

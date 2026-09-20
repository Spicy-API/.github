# SpicyAPI

Most aggregators decide for you what a model is allowed to produce, then bill you in points
you bought upfront. This one does neither.

```bash
curl https://api.spicyapi.ai/api/v1/jobs/createTask \
  -H "Authorization: Bearer $SPICY_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"model":"bytedance/seedance-2.5/text-to-video","input":{"prompt":"..."}}'
```

One key. 121 endpoints behind it. Priced in dollars, quoted before you spend.

---

### No content review on our side

What a model produces is decided by the model you pick — not by a flag you have to set, an
approval queue, or a classifier sitting between you and the thing you paid for. 27 of our
endpoints are LoRA-tuned for adult work and live in their own families.

We measured the filtering behaviour of every route and put the result on the model page, so
you can tell what you are buying **before** the bill. A model that quietly substitutes a safer
output is worse than one that refuses, and we label both.

### Dollars, not credits

Prices are USD per request. `POST /quote` tells you what a specific call will cost, that
number is what gets held, and you are charged the real cost when it settles — never more than
the hold. No expiring balance, no conversion rate, no minimum top-up.

### One request shape

Media generation is asynchronous everywhere, so it works the same everywhere: create a task,
get a `202`, then poll or take a webhook. Text models speak the OpenAI, Anthropic and Gemini
wire formats — point an existing client at our base URL and it works unchanged.

---

## What you can generate

**Video** — text-to-video, image-to-video, reference-to-video, up to 4K.
Seedance 2.5 · Seedance 2.0 · MiniMax H3 · Wan 2.7 · LTX 2.5 · Vidu Q3 · Krea 2 · HappyHorse 1.1

**Image** — generation, editing, face and head swap.
Seedream 5.0 Pro · Qwen Image 3.0 · Z-Image · Prefect Pony XL

**Text** — Claude Opus 5 · Gemini 3.1 Pro · DeepSeek V4 Pro · Kimi K3 · GLM 5.3 · Grok 4.6

**Audio** — HeartMuLa Transcribe

83 families, 121 endpoints, all of it in one catalogue →
[spicyapi.ai/models](https://spicyapi.ai/models)

## Clients

| | | |
|---|---|---|
| TypeScript | `npm i @spicyapi/sdk` | on npm |
| Go | `go get github.com/Spicy-API/spicy-go` | [repo](https://github.com/Spicy-API/spicy-go) |
| Python | from source for now | [repo](https://github.com/Spicy-API/spicy-python) |
| PHP | from source for now | [repo](https://github.com/Spicy-API/spicy-php) |
| Java | from source for now | [repo](https://github.com/Spicy-API/spicy-java) |

There is also a CLI (`npx @spicyapi/cli status` — no key required), an MCP server so agents can
generate media themselves, and an Agent Skill for Claude.

---

[Get a key](https://spicyapi.ai) · [Docs](https://docs.spicyapi.ai) · [Status](https://status.spicyapi.ai) · [support@spicyapi.ai](mailto:support@spicyapi.ai)

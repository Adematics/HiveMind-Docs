---
title: "Public API: Getting Started"
hidden: false
---

The Hivemind public REST API lets your own systems read and write the same data you see in the app — list pipelines, create candidates, move them forward or backward, and keep an external ATS or careers site in sync. This guide gets you from zero to a successful authenticated request.

## 1. Generate your API key

1. Open **Settings → Apps & Integrations**.
2. In the **Hivemind API Key** card, click **Generate** (or **Regenerate** if a key already exists).
3. Copy the key immediately using the copy button.

Keys start with the prefix `hk_live_`. There is **one key per workspace**, and it authenticates as your company — not as an individual user.

<Callout icon="⚠️" theme="warn">
  The key is shown **once**. If you lose it, click **Regenerate** — this issues a new key and **immediately invalidates the old one**, so update every system that uses it.
</Callout>

{/* 📸 Screenshot: Hivemind API Key card in Settings → Apps & Integrations with a freshly generated key and copy button */}

## 2. Authenticate

Send the key as a bearer token on every request:

```
Authorization: Bearer hk_live_XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
```

All endpoints live under the base path `/api/public/v1` on `https://hivemind.hr`. Requests without a valid key get a `401` with an error code like `missing_api_key` or `invalid_api_key`.

## 3. Make your first call

`GET /whoami` is a smoke test that proves your key works end-to-end:

```bash
curl https://hivemind.hr/api/public/v1/whoami \
  -H "Authorization: Bearer hk_live_XXXX..."
```

A successful response returns the workspace the key belongs to:

```json
{ "company_id": "6f1c2e6a-91d4-4a5b-8f47-6f0f1f0a1b2c" }
```

Errors always share one JSON shape, with a `request_id` you can quote to [support](/docs/contact-support):

```json
{ "error": { "code": "invalid_api_key", "message": "Invalid API key", "request_id": "..." } }
```

## 4. Rate limits

Each workspace gets **120 requests per minute** and **10,000 requests per day**. Every response includes headers so you can pace yourself:

- `X-RateLimit-Limit-Minute` / `X-RateLimit-Remaining-Minute`
- `X-RateLimit-Limit-Day` / `X-RateLimit-Remaining-Day`
- `X-RateLimit-Reset` — when the window that matters next resets

Exceeding a limit returns `429 rate_limited` with a `Retry-After` header telling you how many seconds to wait.

## 5. Idempotency (safe retries)

For `POST` and `PATCH` requests, you can send an `Idempotency-Key` header (8–64 characters of letters, digits, `_` or `-` — a UUID works well). If the same key and body are retried within **24 hours**, Hivemind replays the original response instead of repeating the action, and marks it with an `Idempotent-Replay: true` header.

- Same key, **different body** → `409 idempotency_conflict`
- Same key while the first request is still running → `409 idempotency_in_progress` (retry shortly)
- No header → the request runs normally with no replay protection

<Callout icon="💡" theme="info">
  Always send an `Idempotency-Key` when creating candidates from a form or job board — a network timeout plus a retry will never create a duplicate.
</Callout>

## 6. Explore the full reference

The complete endpoint documentation lives in the [API Reference](/reference). Highlights:

- **Candidates** — list and create candidates, fetch or update one, and `rewind` / `fast-forward` a candidate through pipeline stages.
- **Pipelines** — list pipelines, fetch one, and update it.

## What's next

- Get pushed events instead of polling with [Webhooks](/docs/webhooks)
- See what candidates the API manages in [Managing Candidates in a Pipeline](/docs/managing-candidates-in-a-pipeline)
- Browse every endpoint in the [API Reference](/reference)
- Connect off-the-shelf tools in the [Integrations Overview](/docs/integrations-overview)

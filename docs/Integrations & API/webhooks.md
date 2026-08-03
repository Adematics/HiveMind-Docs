---
title: Webhooks
hidden: false
---

Webhooks push candidate activity to your systems the moment it happens, with no polling required. Configure one HTTPS endpoint per workspace and Hivemind will POST a signed JSON event every time a candidate applies, changes stage, finishes a pipeline, or needs a human.

## 1. Subscribe your endpoint

1. Open **Settings → Apps & Integrations** and find the **Outbound Webhook** card.
2. Enter your **Endpoint URL**; it must be a valid `https://` URL.
3. Tick the events you want under **Subscribed events**.
4. Click **Save webhook**.

On save, Hivemind reveals your **Signing secret** exactly once. Copy it now and store it with your receiver, as there is no way to view it again. If it's ever lost or leaked, click **Rotate secret** to issue a new one (the previous secret becomes invalid immediately).

The card also has a toggle to pause and resume deliveries (**Active** / **Paused**), stats for **Last success**, **Last failure**, and **Consecutive failures**, and a **Remove** button to delete the configuration.

{/* 📸 Screenshot: Outbound Webhook card with URL field, event checkboxes, and the one-time signing secret revealed */}

## 2. The four events

| Event | Fires when |
| --- | --- |
| `candidate.applied` | A new candidate enters a pipeline, via the public application form, the public API, or an ATS sync (Ashby / Greenhouse). Payload includes the candidate **and the pipeline** they applied to. |
| `candidate.stage_changed` | A candidate moves between nodes. Includes the previous node's response data (resume score, assessment results, branch decision, etc.) so you can act without an extra API call. |
| `candidate.end` | A candidate reaches an End node. Includes the final aggregated score and the path taken. |
| `candidate.manual_intervention` | A candidate reaches a Manual Review / Interview / Phone Call node and is waiting on a human. |

## 3. Payload shape

Every delivery is a JSON envelope with a unique `id`, the event `type`, a timestamp, and a `data` object. For stage events:

```json
{
  "id": "0b8b9f9e-3c1d-4b8a-9c1e-2f7a5d6e8c11",
  "type": "candidate.stage_changed",
  "created_at": "2026-07-29T14:02:11.000Z",
  "data": {
    "candidate": {
      "id": "…", "email": "jane@example.com", "name": "Jane Doe",
      "status": "active", "pipeline_id": "…", "current_node_id": "…",
      "is_hired": false, "total_score": 82.5, "resume_url": "…",
      "application_metadata": { }
    },
    "previous": {
      "node_id": "…", "node_type": "resumatic", "node_label": "Resume Screen",
      "response": { "score": 82.5, "evaluation_details": { } }
    },
    "current": { "node_id": "…", "node_type": "assessment", "node_label": "Skills Test" },
    "branched_through": []
  }
}
```

`candidate.applied` carries `data.candidate` plus a `data.pipeline` summary (name, job title, description, location, status) instead of the node blocks. `candidate.end` adds `data.final_score`.

## 4. Verify signatures

Each POST includes these headers:

- `X-Hivemind-Signature`: `sha256=<hex>`, an HMAC-SHA256 of the **raw request body** keyed by your signing secret
- `X-Hivemind-Event-Id`: unique per event; **dedupe on this**, since retries re-send the same event
- `X-Hivemind-Event-Type`, `X-Hivemind-Delivery-Id`, `X-Hivemind-Attempt`

Recompute the HMAC with your stored secret and compare it to the header using a constant-time comparison. Reject anything that doesn't match; the secret itself never travels on the wire.

<Callout icon="⚠️" theme="warn">
  Respond with a **2xx within 10 seconds** and do the heavy work asynchronously. Redirects are not followed; your endpoint must answer at the exact URL you configured.
</Callout>

## 5. Retries and auto-disable

- Failed deliveries are retried up to **5 attempts total**, with backoff of **30s → 2m → 5m → 15m** between attempts.
- A `404` or `410` response is treated as "endpoint gone": retries stop and the webhook is **auto-disabled immediately**.
- After **24 consecutive permanently-failed deliveries** (roughly nine hours of sustained outage), the webhook is auto-disabled and the card shows an alert with the last failure time.
- To recover, fix your endpoint and flip the toggle back on; the failure counter resets and deliveries resume immediately. Events that occur while a webhook is disabled or paused are **not** delivered later.

<Callout icon="💡" theme="info">
  Use the **Last success / Last failure / Consecutive failures** stats on the card as your first debugging stop when events seem to be missing.
</Callout>

## What's next

- Pair pushed events with pulls via the [Public API](/docs/public-api-getting-started) and the [API Reference](/reference)
- Understand the node types in payloads with the [Pipeline Nodes Reference](/docs/pipeline-nodes-reference)
- See stage movement in the app in [Managing Candidates in a Pipeline](/docs/managing-candidates-in-a-pipeline)

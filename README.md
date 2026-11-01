# Email AI Agent

> Triage incoming Gmail messages with AI, apply the right label, and prepare a reply draft for a human to approve.

## Design principle: draft, do not blindly send

This workflow is intentionally built around review. The AI can classify a message and draft a response, but a person remains responsible for the final send. That is a safer pattern for customer support, sales inboxes, and operational email.

## Workflow map

```text
Gmail trigger
  → AI message analysis
  → classify intent
  → apply Gmail label
  → create reply draft
  → human reviews and sends
```

## Suitable use cases

- Support-inbox triage
- Sales-lead routing
- FAQ response preparation
- Internal-request classification
- First-pass email organization

## Before you enable it

1. Import `workflow.json` into n8n.
2. Connect Gmail and OpenAI credentials you control.
3. Create or map the labels used by the workflow.
4. Define which messages should be ignored, escalated, or drafted.
5. Review the prompt, sender rules, reply tone, and Gmail draft behaviour.
6. Test using non-sensitive sample emails.

## Important safeguards

- Do not activate an unrestricted trigger on an inbox that contains sensitive material until access and retention rules are clear.
- Keep a human approval step for financial, legal, medical, HR, or customer-impacting messages.
- Add sender allowlists or exclusion rules before using it with high-volume mail.
- This repository contains a sanitized template only: no credentials, inbox data, labels, or recipient addresses are included.

## Repository contents

| File | Purpose |
| --- | --- |
| `workflow.json` | Importable n8n workflow |
| `SECURITY.md` | Credential and disclosure guidance |
| `LICENSE` | MIT license |

## License

MIT — see [LICENSE](LICENSE).
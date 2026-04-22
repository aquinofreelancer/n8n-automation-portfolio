# Screenshots

Place redacted n8n canvas screenshots here. Suggested captures:

1. **Full workflow canvas** — overview showing all nodes and connections
2. **Webhook trigger detail** — showing inbound SMS handling (redact webhook URL)
3. **LLM node configuration** — system prompt and structured output schema (keep, but redact API key)
4. **Postgres chat memory node** — showing session key logic (redact connection string)
5. **Intent router (Switch node)** — showing the branching logic
6. **Google Calendar node** — showing booking/reschedule logic (redact calendar ID)

## Redaction checklist

Before committing any screenshot:

- [ ] API keys / tokens replaced with `***REDACTED***` or pixelated
- [ ] Webhook URLs replaced with `https://n8n.example.com/webhook/...`
- [ ] Client names replaced with `[Client Name]`
- [ ] Phone numbers replaced with `+1 (555) 000-0000`
- [ ] Email addresses replaced with `example@domain.com`
- [ ] Credential dropdown names visible but values never shown
- [ ] Database hostnames / connection strings removed or blurred

Save screenshots as `.png` with descriptive filenames like `01-full-canvas.png`, `02-webhook-trigger.png`, etc.

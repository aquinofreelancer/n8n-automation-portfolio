# Screenshots

Place redacted n8n canvas screenshots here. Suggested captures:

1. **Full workflow canvas** — showing the four parallel API calls into the merge
2. **Cron trigger** — pre-lineup-lock schedule
3. **Yahoo! Sports OAuth credential setup** — credential dropdown visible, values hidden
4. **One of the HTTP request nodes** — with league ID redacted
5. **Merge / Set node** — showing normalization into unified JSON
6. **LLM analyzer node** — showing the structured prompt and output schema
7. **Gmail send node** — with recipient redacted

## Redaction checklist

Before committing any screenshot:

- [ ] OAuth tokens and API keys replaced with `***REDACTED***` or pixelated
- [ ] League IDs, team IDs replaced with `[REDACTED]`
- [ ] Recipient email replaced with `example@domain.com`
- [ ] Endpoint URLs with embedded IDs replaced with `.../leagues/[REDACTED]/...`
- [ ] Credential dropdown names visible but values never shown

Save screenshots as `.png` with descriptive filenames like `01-full-canvas.png`, `02-oauth-detail.png`, etc.

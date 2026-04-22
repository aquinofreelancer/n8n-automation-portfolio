```mermaid
flowchart TD
    A[Cron Trigger<br/>Pre-lineup-lock] --> B[Yahoo! Sports API<br/>OAuth 2.0 auth]
    B --> C[GET current roster]
    B --> D[GET current-week stats]
    B --> E[GET previous-week stats]
    B --> F[GET free agents]
    C --> G[Set node:<br/>normalize + merge]
    D --> G
    E --> G
    F --> G
    G --> H[LLM: Lineup decision<br/>structured JSON]
    H --> I[Format email<br/>start / sit / waiver]
    I --> J[Gmail: Send recommendation]
```

## How to render

This diagram renders automatically on GitHub inside a markdown file. To render locally or export as an image, use the [Mermaid Live Editor](https://mermaid.live) and paste the fenced code block above.

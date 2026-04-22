```mermaid
flowchart LR
    A[Cron Trigger<br/>Weekly, pre-gameday] --> B{Parallel Fan-Out}
    B --> C[NFL News API]
    B --> D[Odds API]
    B --> E[Team Stats API]
    C --> F[LLM: Per-article<br/>sentiment scoring]
    F --> G[Aggregate by team]
    D --> H[Normalize odds<br/>JSON schema]
    E --> I[Normalize stats<br/>JSON schema]
    G --> J[Merge Node]
    H --> J
    I --> J
    J --> K[Split by matchup]
    K --> L[LLM: Predict winner<br/>+ rationale]
    L --> M[Format HTML email]
    M --> N[Gmail: Send report]
```

## How to render

This diagram renders automatically on GitHub inside a markdown file. To render locally or export as an image, use the [Mermaid Live Editor](https://mermaid.live) and paste the fenced code block above.

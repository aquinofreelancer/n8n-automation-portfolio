```mermaid
flowchart TD
    A[Website Lead Form] -->|Webhook POST| B[n8n: Capture Trigger]
    B --> C[Google Sheets<br/>Log lead: name, email, phone]
    B --> D[Twilio: Send opening SMS]
    D --> E{Inbound SMS Webhook}
    E --> F[Postgres: Load<br/>conversation history]
    F --> G[RAG Retrieval<br/>Gym knowledge base]
    G --> H[Google Gemini<br/>Generate structured response]
    H --> I{Intent Router}
    I -->|question| J[Generate text reply]
    I -->|book| K[Google Calendar:<br/>Check availability]
    I -->|reschedule| L[Google Calendar:<br/>Update event]
    I -->|cancel| M[Google Calendar:<br/>Delete event]
    I -->|low confidence| N[Flag for human handoff]
    K --> O[Create event]
    J --> P[Twilio: Send reply]
    L --> P
    M --> P
    O --> P
    N --> P
    P --> Q[Postgres: Append to<br/>chat history]
    Q --> E
```

## How to render

This diagram renders automatically on GitHub inside a markdown file. To render locally or export as an image, use the [Mermaid Live Editor](https://mermaid.live) and paste the fenced code block above.

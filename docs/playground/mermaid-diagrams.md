## Mermaid Diagrams (Playground)

Wenn dein Renderer Mermaid unterstützt, sollten diese Diagramme gerendert werden.
Wenn nicht, sollten sie zumindest als Codeblock sichtbar sein.

## Flowchart

```mermaid
flowchart TD
  A[Start] --> B{Choice}
  B -->|Yes| C[Do thing]
  B -->|No| D[Do other thing]
  C --> E[End]
  D --> E[End]
```

## Sequence diagram

```mermaid
sequenceDiagram
  participant U as User
  participant A as App
  participant D as Docs
  U->>A: request /docs
  A->>D: read Markdown
  D-->>A: render HTML
  A-->>U: response
```

## State diagram

```mermaid
stateDiagram-v2
  [*] --> Draft
  Draft --> Review
  Review --> Published
  Review --> Draft
  Published --> Archived
  Archived --> [*]
```


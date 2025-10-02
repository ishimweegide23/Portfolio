## GitHub Workflow

```mermaid
flowchart LR
    A[Clone Repository] --> B[Create Branch]
    B --> C[Make & Commit Changes]
    C --> D[Push Branch to GitHub]
    D --> E[Open Pull Request]
    E --> F[Code Review & Approval]
    F --> G[Merge to Main]
    G --> H[Deploy]

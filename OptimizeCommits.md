# Slide 1
## **How Claude Code Commits to GitHub**
…and how to dramatically reduce token usage.

#ClaudeCode #AIEngineering #TokenOptimization

---

# Slide 2 — The Problem
Claude must:
- Read files  
- Reason about diffs  
- Generate git commands  
- Execute tools  

Each step consumes **tokens**.  
Different workflows = different token costs.

```mermaid
flowchart LR
    A[User Request] --> B[Claude Reads Files]
    B --> C[Claude Reasons About Diffs]
    C --> D[Claude Generates Git Commands]
    D --> E[Tool Execution]
    E --> F[GitHub Repo]

    classDef tokens fill:#f5f5f5,stroke:#333,stroke-width:1px;
    class B tokens;
    class C tokens;
    class D tokens;
```

# Slide 3 — Path‑1: Skills
Skills = Lean Context Automation

Token Flow:

Input ↓

Output ↓

Reasoning ↓

Context ↓

```mermaid
flowchart LR
    A[User] --> B[Skill Module]
    B --> C[Claude]
    C --> D[Git Commands]
    D --> E[GitHub]

    classDef lowTokens fill:#d4f4dd,stroke:#2b7a2f;
    class B lowTokens;
    class C lowTokens;
```

# Slide 4 — Path‑2: GitHub CLI Tool
CLI Tools = Offloading Git Logic

Token Flow:

Input ↓

Output ↓

Reasoning ↓↓↓

Context steady

```mermaid
flowchart LR
    A[User] --> B[Claude]
    B --> C[CLI Tool]
    C --> D[GitHub]

    classDef fewerTokens fill:#d0e8ff,stroke:#1a4e80;
    class C fewerTokens;
```

# Slide 5 — Path‑3: MCP (Model Context Protocol)
MCP = Lowest Token Usage

Token Flow:

Input ↓↓↓

Output ↓↓

Reasoning ↓↓↓↓

Context minimal

```mermaid
flowchart LR
    A[User] --> B[Claude]
    B --> C[MCP Request]
    C --> D[MCP Server]
    D --> E[GitHub]

    classDef minimalTokens fill:#fff2cc,stroke:#b38f00;
    class C minimalTokens;
    class D minimalTokens;
```

# Slide 6 — Token Efficiency Ranking
```mermaid
graph TD
    A[MCP<br/>⭐⭐⭐⭐⭐] -->|Most Efficient| Z[Token Savings]
    B[CLI Tool<br/>⭐⭐⭐⭐] --> Z
    C[Skills<br/>⭐⭐⭐] --> Z
```

# Slide 7 — Final Takeaway
For maximum token efficiency → Choose MCP  
For simple offloading → Use CLI tools  
For structured automation → Use Skills

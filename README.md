# Antigravity: The Project Factory System

> **Transforming raw visions into autonomous project structures.**

Antigravity is an agentic project generation engine. It doesn't just scaffold code; it births a living workspace equipped with a specialized team of subagents, rules, and workflows tailored to your specific context.

## 🌀 The Antigravity Lifecycle

```mermaid
graph TD
    subgraph "Phase A: The Factory (Template)"
        Start((User Vision)) --> Mulai["/mulai Workflow"]
        Mulai --> OrchT[Orchestrator]
        OrchT --> |Delegate| Interviewer[Interviewer: Discovery]
        Interviewer --> |Synthesize| Context[(personal-context.md)]
        OrchT --> |Delegate| Architect[Architect: Blueprinting]
        Architect --> |Structure| Export[Export to Desktop]
    end

    subgraph "Phase B: The Awakening (Transition)"
        Export --> NewAgent[New Agent Lifecycle]
        NewAgent --> Init["/init Workflow"]
        Init --> Sync[Sync DOCS to .agent/]
        Sync --> Cleanup[Self-Destruct Factory Artifacts]
    end

    subgraph "Phase C: The Operation (Active Project)"
        Cleanup --> OrchA[Orchestrator Active]
        OrchA --> Rules{Registry Enforced}
        Rules --> |Delegation| Subagents[Subagents: Specialist Execution]
        Subagents --> Result([Autonomous Delivery])
    end

    style OrchT fill:#f96,stroke:#333,stroke-width:2px
    style OrchA fill:#f96,stroke:#333,stroke-width:2px
    style Start fill:#dfd,stroke:#333
    style Result fill:#dfd,stroke:#333
```

## 🛠 Operational Protocols

This system is managed exclusively by the **Orchestrator**.

### 1. In this Template (/mulai)
Run the `/mulai` command to start the Project Factory. The Orchestrator will lead you through a discovery session to define your project's identity and technical needs.

### 2. In the New Project (/init)
When you first open a generated project, run the `/init` command. This will:
- Activate all rules, workflows, and subagents.
- Mirror the knowledge-base and skills.
- Clean up temporary factory files (`DOCS/`, `init.md`).

## 👥 Agent & Skill Registry

The Orchestrator delegates specialized tasks according to this registry:

| Agent | Primary Skill(s) | Role & Responsibility |
| :--- | :--- | :--- |
| **Interviewer** | `brainstorming-pro`, `fact-search` | Discovery, Vision clarity, and Context synthesis. |
| **Architect** | `architecture-visualizer` | Structural design, tech-stack selection, blueprints. |
| **QA Auditor** | `context-audit`, `diff-analyzer` | Validation, integrity checks, and anomaly detection. |
| **Output Editor** | `writing-style`, `linguistic-bridge` | Style harmonization and high-quality messaging. |

---
*Powered by Antigravity Agentic Framework.*
- **`knowledge-base/`**: A central knowledge hub for storing reference documents (PDF, DOCX, TXT, MD) as context for project creation.

## Quick Start
1. **Provide Context**: Place your project's reference documents into the `knowledge-base/` folder.
2. **Run the Factory**: Use the slash command `/mulai` to trigger the discovery and interview process. The project will be built locally in the `exports/` directory.

## Workflow
The system follows a **Cascading Documentation** approach:
`Knowledge Base` -> `User Profile` -> `Rules` -> `Workflows` -> `Agents Persona`.

---
*Created with Mechanical Grace by Antigravity.*

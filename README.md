# Antigravity Template: Project Factory

This template is designed as an automation framework for building standardized new project foundations using Agentic AI.

## Core Structure
- **`.agent/`**: Contains the rules, workflows, and agent personas that power the system.
- **`knowledge-base/`**: A central knowledge hub for storing reference documents (PDF, DOCX, TXT, MD) as context for project creation.

## Quick Start
1. **Provide Context**: Place your project's reference documents into the `knowledge-base/` folder.
2. **Run the Factory**: Use the slash command `/mulai` to trigger the discovery and interview process. The project will be built locally in the `exports/` directory.
3. **Export Results**: Once the build is solid and validated, the system will export the final project folder to your **Desktop**. Follow the instructions in `init.md` (inside the new project) to activate the agent.

## Workflow
The system follows a **Cascading Documentation** approach:
`Knowledge Base` -> `User Profile` -> `Rules` -> `Workflows` -> `Agents Persona`.

---
*Created with Mechanical Grace by Antigravity.*

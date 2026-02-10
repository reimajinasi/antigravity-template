---
description: Agent Installer - EXCLUSIVELY managed by the Orchestrator.
---

# Agent Installer (Orchestrator Workflow)
(/init)

## Purpose
This workflow migrates configuration from the `DOCS/` folder to the permanent `.agent/` directory and cleans up factory traces so the agent is ready for full operation.

## Steps
// turbo-all
1. **Sync Configuration**:
   - Run the following copy commands to synchronize data:
     ```bash
     cp -r DOCS/rules/ .agent/rules/
     cp -r DOCS/workflows/ .agent/workflows/
     cp -r DOCS/agents/ .agent/agents/
     cp -r DOCS/skills/ .agent/skills/
     cp -r DOCS/knowledge-base/ knowledge-base/
     cp DOCS/personal-context.md .agent/user/user-profile.md
     ```
2. **Cleanup**:
   - Remove residual factory files to maintain project cleanliness:
     ```bash
     rm -rf DOCS/ factory-status.json .agent/workflows/init.md
     ```
3. **Activation**:
   - Provide session closing instructions to the user:
     - Close all open documents.
     - Close the project folder to synchronize the directory structure.
     - Re-open the project folder to ensure the new directory structure is recognized.
     - Start a new conversation (New Chat) as needed.

---
> [!IMPORTANT]
> Only run the cleanup commands above after all files have been copied correctly.

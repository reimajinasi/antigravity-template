# Agent Installer (init.md)

Follow these steps to activate the Agent in your new project:

## 1. Directory Preparation
Ensure the `.agent` folder is ready in your target project root.

## 2. Sync Configuration
Run the following commands (adjust paths as necessary):
```bash
cp -r DOCS/rules/ .agent/rules/
cp -r DOCS/workflows/ .agent/workflows/
cp -r DOCS/agents/ .agent/agents/
cp -r DOCS/skills/ .agent/skills/
cp DOCS/personal-context.md .agent/user/user-profile.md
rm -rf DOCS/ factory-status.json init.md
```

## 3. Verification
Open your new project and follow the initialization instructions that appear automatically.

## 4. Final Step: New Session Protocol
To ensure a complete "Amnesia Reset" and focused environment:
1. **Close all open documents** in your editor.
2. **Restart Project Window**: Close this project window completely and **open the same folder again**. This forces the editor to synchronize the file deletion (Clean Boot).
3. **Start a new conversation session** (New Chat) in the reopened project.

---
> [!TIP]
> This file and the `DOCS/` folder will be deleted immediately after you run the commands in Step 2. The restart in Step 4 ensures you see the clean state.

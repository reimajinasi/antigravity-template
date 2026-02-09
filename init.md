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
cp DOCS/personal-context.md .agent/user/user-profile.md
```

## 3. Verification
Open your new project and follow the initialization instructions that appear automatically.

---
> [!TIP]
> This file can be deleted after the Agent has been successfully installed in the target project.

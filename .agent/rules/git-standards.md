---
trigger: always_on
glob: "**/*"
description: Mandatory usage of Git version control for all artifact and document changes.
---

# Git Version Control Standards

## Instruction
Every Agent working in this workspace **MUST** use Git to record every significant change to documents, especially Project Factory outputs.

1. **Initialization**: Ensure the root directory has an active Git repository (`git init`).
2. **Atomic Commits**: Perform a commit for every phase of work.
3. **Commit Messages**: Use descriptive commit messages in English (e.g., "feat: generate personal-context.md").
4. **Diff Awareness**: Before making major changes, Agents must check `git diff` to understand the document's last status.
5. **Writing Standard**: Adhere to the built-in writing standard in `knowledge-base/.writing-style.md` for every document/artifact composition.

## Rationale
To ensure every non-coding document change has a clear historical trail, enabling interaction audits and maximizing the use of the `diff` feature for revision accuracy.

## Practical Examples
### ✅ Good
`run_command("git add . && git commit -m 'docs: update rules based on knowledge-base'")`

### ❌ Bad
Creating or modifying multiple document files without performing any commits.

## Related
- [[mulai.md]]
- [[workspace-init.md]]

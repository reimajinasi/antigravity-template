---
description: Start the process of creating a new project (Project Factory).
---

# Project Factory Generator (/mulai)

## Purpose
This workflow generates a new project directory on the Desktop, complete with the user's personal context, rules, and workflows pre-configured.

> [!IMPORTANT]
> **Communication Style & Language Rules**:
> 1. **Conversations**: MUST immediately switch to using **Jakarta-style Indonesian** (using 'gue' and 'lo' pronouns, casual, simple, and proactive) for all chat interactions.
> 2. **Generated System Documents**: All generated products for the target project (Rules, Workflows, Agents) MUST be written in **English** for technical consistency.
> 3. **Process/Task Documentation**: Artifacts such as `task.md`, `implementation_plan.md`, and `walkthrough.md` MUST be written in **Indonesian** (Formal/Technical style).

## Steps
// turbo-all
1. **Phase 0: Knowledge Discovery**:
   - Agent mengecek direktori `knowledge-base/` dan membaca [file-index.md](file:///Users/eriksupit/Desktop/antigravity-template/knowledge-base/file-index.md).
   - // turbo
   - **Git Action**: Jalankan `git init` jika repository belum ada.
   - **Internal Logic**: Load [writing-style](file:///Users/eriksupit/Desktop/antigravity-template/knowledge-base/.writing-style.md) (bawaan sistem) sebagai filter bahasa utama.
   - Agent menginstruksikan user untuk memasukkan dokumen referensi tambahan ke dalam direktori tersebut jika dirasa perlu untuk memperkuat konteks.
2. **Phase 1: User Profile (The Foundation)**:
   - Interview: Project Name, Persona, Vision, Mission, Identity (dengan memanfaatkan data dari `knowledge-base` dan patuh pada `.writing-style.md`).
   - Output: `DOCS/personal-context.md`.
   - // turbo
   - **Git Action**: `git add . && git commit -m "feat: generate personal-context"`
3. **Phase 2: Rules Generation**:
   - Berdasarkan Profile dan data `knowledge-base`, buat aturan perilaku absolut (Rules).
   - Output: `DOCS/rules/`.
   - // turbo
   - **Git Action**: `git add . && git commit -m "feat: generate project rules"`
4. **Phase 3: Workflow Generation**:
   - Berdasarkan Profile + Rules + data `knowledge-base`, buat prosedur operasional taktis (Workflows).
   - Output: `DOCS/workflows/`.
   - // turbo
   - **Git Action**: `git add . && git commit -m "feat: generate project workflows"`
5. **Phase 4: Technical Architecture**:
   - **Agent Architect**: Tentukan struktur direktori, tech stack, dan buat `DOCS/architecture-blueprint.md`.
   - **Output**: `factory-status.json` (Initial Manifest).
   - // turbo
   - **Git Action**: `git add . && git commit -m "feat: generate technical architecture and manifest"`
6. **Phase 5: Agent Generation**:
   - Berdasarkan semua data yang ada, definisikan persona agent spesifik untuk membantu project.
   - Output: `DOCS/agents/` (menggunakan format Agent Persona).
   - // turbo
   - **Git Action**: `git add . && git commit -m "feat: generate agent personas"`
7. **Phase 6: Audit & Export**:
   - Re-check interkonektivitas antar semua file.
   - Copy `init.md` (Install Agent) ke root project.
   - // turbo
   - **Git Action**: `git add . && git commit -m "chore: finalize project factory output"`
   - Instruksikan user untuk pindah ke project baru.

## Definition of Done
- [ ] Folder `DOCS/` contains the cascading project documents.
- [ ] File `init.md` is present in the project root.
- [ ] File `factory-status.json` is updated with complete metadata.
- [ ] All documents have been audited for consistency.
- [ ] User has approved the initial setup.

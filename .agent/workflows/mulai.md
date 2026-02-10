---
description: Project Factory Generator - EXCLUSIVELY managed by the Orchestrator.
---

# Project Factory Generator (Orchestrator Workflow)
 (/mulai)

## Purpose
This workflow generates a new project directory on the Desktop, complete with the user's personal context, rules, and workflows pre-configured.

> [!IMPORTANT]
> **Communication Style & Language Rules**:
> 1. **Conversations**: MUST immediately switch to using **Jakarta-style Indonesian** (using 'gue' and 'lo' pronouns, casual, simple, and proactive) for all chat interactions.
> 2. **Generated System Documents**: All generated products for the target project (Rules, Workflows, Agents) MUST be written in **English** for technical consistency.
> 3. **Process/Task Documentation**: Artifacts such as `task.md`, `implementation_plan.md`, and `walkthrough.md` MUST be written in **Indonesian** (Formal/Technical style).

## Steps
// turbo-all
1. **Phase 0: Project Discovery & Init**:
   - **Action**: Tanyakan nama project kepada user.
   - **Directory Creation**: Buat folder baru di dalam direktori `exports/` lokal (`./exports/[project-name]`).
   - Agent mengecek direktori `knowledge-base/` template dan membaca [file-index.md](file:///Users/eriksupit/Desktop/antigravity-template/knowledge-base/file-index.md).
   - **Skill Preparation**: Salin folder `.agent/skills/` dari template ke `exports/[project-name]/DOCS/skills/`.
   - **Knowledge Base Prep**: Salin folder `knowledge-base/` dari template ke `exports/[project-name]/DOCS/knowledge-base/`.
   - // turbo
   - **Git Action**: Jalankan `git init` di dalam folder project lokal tersebut.
   - **Internal Logic**: Aktifkan skill [writing-style](file:///Users/eriksupit/Desktop/antigravity-template/.agent/skills/writing-style/SKILL.md), [fact-search](file:///Users/eriksupit/Desktop/antigravity-template/.agent/skills/fact-search/SKILL.md), [linguistic-bridge](file:///Users/eriksupit/Desktop/antigravity-template/.agent/skills/linguistic-bridge/SKILL.md), [advanced-analytics](file:///Users/eriksupit/Desktop/antigravity-template/.agent/skills/advanced-analytics/SKILL.md).
   - Agent menginstruksikan user untuk memasukkan dokumen referensi tambahan. Gunakan `fact-search` jika data internal kurang.
2. **Phase 1: User Profile (The Foundation)**:
   - **Delegation Protocol**: Sesuai [orchestration-logic](file:///Users/eriksupit/Desktop/antigravity-template/.agent/rules/orchestration-logic.md), Orchestrator mendelegasikan sesi ini kepada [interviewer.md](file:///Users/eriksupit/Desktop/antigravity-template/.agent/agents/interviewer.md).
   - Interview: Project Name, Persona, Vision, Mission, Identity (dengan memanfaatkan data dari `knowledge-base`, `fact-search`, dan patuh pada `.writing-style.md`).
   - **Action**: Subagent menggunakan skill [brainstorming-pro](file:///Users/eriksupit/Desktop/antigravity-template/.agent/skills/brainstorming-pro/SKILL.md) dan [advanced-analytics](file:///Users/eriksupit/Desktop/antigravity-template/.agent/skills/advanced-analytics/SKILL.md) (SWOT/TELOS) untuk mendalam visi & misi jika diperlukan.
   - Output: `DOCS/personal-context.md`.
   - // turbo
   - **Git Action**: `git add . && git commit -m "feat: generate personal-context"`
3. **Phase 2: Rules Generation**:
   - Berdasarkan Profile dan data `knowledge-base`, buat aturan perilaku absolut (Rules).
   - **Core Rules**: Salin [orchestration-logic.md](file:///Users/eriksupit/Desktop/antigravity-template/.agent/rules/orchestration-logic.md) ke `DOCS/rules/`.
   - Output: `DOCS/rules/`.
   - // turbo
   - **Git Action**: `git add . && git commit -m "feat: generate project rules"`
4. **Phase 3: Workflow Generation**:
   - Berdasarkan Profile + Rules + data `knowledge-base`, buat prosedur operasional taktis (Workflows).
   - Output: `DOCS/workflows/`.
   - // turbo
   - **Git Action**: `git add . && git commit -m "feat: generate project workflows"`
5. **Phase 4: Technical Architecture**:
   - **Delegation Protocol**: Orchestrator mendelegasikan desain teknis kepada [architect.md](file:///Users/eriksupit/Desktop/antigravity-template/.agent/agents/architect.md).
   - **Agent Architect**: Tentukan struktur direktori, tech stack, dan buat `DOCS/architecture-blueprint.md`.
   - **Output**: `factory-status.json` (Initial Manifest).
   - // turbo
   - **Git Action**: `git add . && git commit -m "feat: generate technical architecture and manifest"`
6. **Phase 5: Agent Generation**:
   - Berdasarkan semua data yang ada, definisikan persona agent spesifik untuk membantu project.
   - **Protocol**: Gunakan format [agent-template.md](file:///Users/eriksupit/Desktop/antigravity-template/.agent/agent-template.md) untuk mendefinisikan **Subagents** yang masing-masing memiliki `assigned_skill`.
   - Output: `DOCS/agents/` (menggunakan format Subagent Persona).
   - // turbo
   - **Git Action**: `git add . && git commit -m "feat: generate subagent personas based on orchestration logic"`
7. **Phase 6: Final Audit & Validation**:
   - **Delegation Protocol**: Orchestrator mendelegasikan validasi akhir kepada [auditor.md](file:///Users/eriksupit/Desktop/antigravity-template/.agent/agents/auditor.md).
   - Re-check interkonektivitas antar semua file di folder `exports/`.
   - Gunakan skill [context-audit](file:///Users/eriksupit/Desktop/antigravity-template/.agent/skills/context-audit/SKILL.md) untuk verifikasi akhir.
   - Minta persetujuan user untuk melakukan ekspor final ke Desktop.
8. **Phase 7: Physical Export & Clean Boot**:
   - // turbo
    - **Action**: Salin/Pindah folder dari `exports/[project-name]` ke `~/Desktop/[project-name]`.
    - **Installer Injection**: Salin `init.md` (Workflow /init) ke folder `.agent/workflows/` proyek di Desktop.
    - // turbo
    - **Git Action**: `git add . && git commit -m "chore: finalize project factory export to desktop with /init workflow"`
    - **Cleanup Instruction**: User/Agent di project baru **WAJIB** menjalankan perintah `/init` untuk melakukan sinkronisasi dan menghapus jejak factory (`DOCS/`, `factory-status.json`).
    - **Final Polish**: Sesuai protokol, Orchestrator memanggil [editor.md](file:///Users/eriksupit/Desktop/antigravity-template/.agent/agents/editor.md) untuk standarisasi linguistik.
    - **New Session Protocol**: Instruksikan user secara eksplisit untuk:
     1. Menutup seluruh dokumen yang terbuka.
     2. **Restart Project**: Tutup window editor dan buka kembali folder yang sama (untuk refresh file explorer).
     3. Memulai percakapan di sesi baru (New Chat).
     4. Agent harus menyebut nama project (`projectName`) dalam instruksi penutupan ini.
   - Biarkan Agent baru melakukan "Amnesia Reset" dan menyambut user sebagai dedicated agent untuk project tersebut.

## Definition of Done
- [ ] Folder `DOCS/` deleted in the final project.
- [ ] File `init.md` deleted after installation.
- [ ] Folder `.agent/` contains all synchronized rules, workflows, and skills.
- [ ] Agent in the new project has no memory of the factory process (Clean Boot).

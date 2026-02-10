---
description: Agent Installer - EXCLUSIVELY managed by the Orchestrator.
---

# Agent Installer (Orchestrator Workflow)
(/init)

## Purpose
Workflow ini memindahkan konfigurasi dari folder `DOCS/` ke direktori `.agent/` yang permanen dan membersihkan jejak factory agar agent siap bekerja penuh.

## Steps
// turbo-all
1. **Sync Configuration**:
   - Jalankan perintah penyalinan berikut untuk sinkronisasi data:
     ```bash
     cp -r DOCS/rules/ .agent/rules/
     cp -r DOCS/workflows/ .agent/workflows/
     cp -r DOCS/agents/ .agent/agents/
     cp -r DOCS/skills/ .agent/skills/
     cp -r DOCS/knowledge-base/ knowledge-base/
     cp DOCS/personal-context.md .agent/user/user-profile.md
     ```
2. **Cleanup**:
   - Hapus sisa file factory untuk menjaga kebersihan proyek:
     ```bash
     rm -rf DOCS/ factory-status.json .agent/workflows/init.md
     ```
3. **Activation**:
   - Berikan instruksi penutupan sesi kepada user:
     - Tutup semua dokumen.
     - close folder proyek, untuk sinkronisasi struktur directory
     - open lagi folder proyek, struktur directory baru terbentk
     - Mulai percakapan baru (New Chat) sesuai keperluan.

---
> [!IMPORTANT]
> Jalankan perintah cleanup di atas hanya setelah semua file tersalin dengan benar.

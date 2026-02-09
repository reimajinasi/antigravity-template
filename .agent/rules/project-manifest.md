---
trigger: completion_of_mulai_workflow
glob: "factory-status.json"
description: Ensures the creation and maintenance of a project manifest file for tracking purposes.
---

# Project Manifest Standard

## Instruction
Setiap kali siklus Project Factory (workflow `/mulai`) selesai atau mengalami update signifikan, Agent **WAJIB** memperbarui file `factory-status.json` di root project yang dihasilkan.

1. **Manifest Content**: File ini harus berisi metadata project:
   - `projectName`: Nama project.
   - `createdDate`: Tanggal inisialisasi.
   - `version`: Versi output factory saat ini.
   - `techStack`: Daftar teknologi yang digunakan.
   - `agentsDeployed`: Daftar persona agent yang sudah terpasang.
   - `lastCommit`: ID commit terakhir dari fase Audit & Export.
2. **Persistence**: File ini digunakan sebagai "Single Source of Truth" untuk status 'pabrik' project tersebut.

## Rationale
Untuk memudahkan pelacakan status project di tengah jalan, memungkinkan audit otomatis, dan memfasilitasi integrasi dengan sistem eksternal atau update di masa depan.

## Practical Examples
### ✅ Good
```json
{
  "projectName": "Makalah-App",
  "createdDate": "2026-02-09",
  "version": "1.0.0",
  "techStack": ["Next.js", "Convex", "Tailwind"],
  "agentsDeployed": ["interviewer", "architect"],
  "lastCommit": "a1b2c3d4"
}
```

## Related
- [[mulai.md]]
- [[git-standards.md]]

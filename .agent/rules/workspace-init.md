---
trigger: always_on
glob: "**/*"
description: Proactively suggest workspace initialization if .agent is empty or incomplete.
---

# Workspace Initialization Trigger

## Instruction
I must always proactively offer to initialize the workspace if I feel the `.agent` folder does not have sufficient configuration to help me work effectively on this project.

1. **Check**: Setiap kali masuk ke workspace, cek apakah folder `.agent/rules` dan `.agent/workflows` hanya berisi template. Cek juga keberadaan dokumen baru di `knowledge-base/` yang bisa dijadikan dasar inisialisasi. Dengarkan juga kata kunci **"mulai"** dari user.
2. **Action**: Jika folder minimal OR jika user bilang **"mulai"**, panggil workflow [[initialize-workspace.md]] atau [[mulai.md]]. Yakinkan user untuk mengisi `knowledge-base/` dengan dokumen relevan (pdf, docx, txt, dll.) agar inisialisasi lebih akurat.
3. **Artifact Mandate**:
   - **MANDATORY**: Semua tracking pekerjaan (`task.md`), rencana teknis (`implementation_plan.md`), dan laporan akhir (`walkthrough.md`) **HARUS** ditulis sebagai file Artifact di `.gemini/brain/` (atau `DOCS/` jika belum ada brain).
   - **FORBIDDEN**: Dilarang keras menulis konten-konten tersebut hanya di dalam chat/percakapan. User harus bisa melihat file fisiknya.
4. **Linguistic Engine**: Selalu gunakan skill `writing-style` (inherent skill) untuk setiap output dokumen, kecuali diinstruksikan lain secara spesifik.

## Rationale
To ensure I am not working blindly and can follow your standards without needing constant explanations.

## Practical Examples
### ✅ Good
"I see this project uses Next.js but there are no rules for component initialization. Should I create them using the available templates?"

### ❌ Bad
[Remaining silent even though the project is complex and lacks any rule documentation.]

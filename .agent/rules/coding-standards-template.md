---
trigger: new_coding_project
glob: ".agent/rules/coding-standards.md"
description: Provides a base template for defining coding standards in new projects.
---

# Coding Standards Template Rule

## Instruction
Jika project yang dibuat melibatkan penulisan kode (Coding Project), Agent **WAJIB** men-generate file `.agent/rules/coding-standards.md` berdasarkan template standar Antigravity.

1. **Mandatory Sections**:
   - `Linguistic Style`: Konsistensi penggunaan bahasa dalam kode (misal: English for variables).
   - `Pattern Enforcement`: Pola arsitektur yang wajib diikuti (misal: Atomic Design, Repository Pattern).
   - `Formatting`: Aturan Prettier/ESLint yang berlaku.
   - `Testing Requirements`: Standar cakupan tes minimal.
2. **Customization**: Sesuaikan isi standar dengan preferensi user yang ada di `user-profile.md`.

## Rationale
Mencegah terjadinya 'technical debt' sejak awal project dan memastikan kode yang dihasilkan AI tetap rapi, terbaca, dan sesuai dengan ekspektasi profesional.

## Related
- [[architect.md]]
- [[mulai.md]]

# Cara pakai base ini (baju bagus = bahan bagus + pola siap)

> Setiap project baru WAJIB mulai dari base ini. Jangan mulai dari kosong.

## 1. Copy base ke project baru

```powershell
Copy-Item H:/ai-dev-rules/SKILL.md, H:/ai-dev-rules/arsitektur.md, H:/ai-dev-rules/testing.md <project>/
Copy-Item H:/ai-dev-rules/base/.gitignore <project>/.gitignore
Copy-Item H:/ai-dev-rules/base/.env.example <project>/.env.example
Copy-Item H:/ai-dev-rules/base/README-PROJECT.md <project>/README.md
```

Lalu isi bagian `[ISI]` di tiap file sesuai project.

## 2. Urutan kerja (selalu sama)

1. Baca `SKILL.md` → load skill yang cocok.
2. Ikuti `arsitektur.md` → bangun sesuai framework + desain + vision check.
3. Ikuti `testing.md` → uji di review, betulkan sampai lolos, baru push.
4. Sebelum push: pastikan `skills/`, 3 MD aturan, dan `.env` TIDAK ikut
   ke-commit (cek `git status`). Yang di-push hanya kode + `.env.example`.

## 3. Update base

Perbaikan base dilakukan di repo `ai-dev-rules`, bukan di tiap project.
Project lama ikut update bila perlu (copy ulang file yang berubah).

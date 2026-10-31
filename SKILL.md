# SKILL.md — Daftar & Aturan Pakai Skill

> File ini WAJIB dibaca setiap awal sesi develop. Semua skill di bawah harus
> diketahui letaknya dan siap dipanggil tanpa bertanya lagi.

## 1. Lokasi skill

| Lokasi | Isi |
|---|---|
| `C:\Users\DONCUL-PC\.config\opencode\skills\<id>\SKILL.md` | Skill global (berlaku semua project & sesi) |
| `<project>/skills/<id>/SKILL.md` | Skill khusus project (override global bila konflik) |

## 2. Daftar skill aktif

| ID | Kapan dipakai |
|---|---|
| `archify` | Setiap sentuh tampilan: halaman web, komponen UI, dashboard, landing page, review desain, kata "bagusin/rapihin/minimalis/eyecatching/bikin UI" |
| `threejs` | Setiap sentuh 3D: scene, model, material, lighting, kamera, OrbitControls, GLB, kata "3D/render/rotasi/rak 3D/data hall" |
| `h-drive-storage` | Setiap tulis file di Windows: semua artifact WAJIB di `H:\`, bukan `C:\` |
| `opencode` | Soal OpenCode itu sendiri: setup, config, troubleshooting, plugin, MCP |
| `reverse-engineer-anything` | Klaim soal shipped app/binary/firmware/website harus dibuktikan dari artifact |
| `report` | Lapor bug opencode via GitHub CLI |
| `port-*` (9 skill) | Kerjaan Port: blueprint, context-lake, oauth-app, dashboard, getting-started, integration, permission, terraform, workflow |

## 3. Aturan pakai (tanpa kecuali)

1. **Load sebelum kerja.** Baca isi `SKILL.md` lengkap SEBELUM tool-call pertama yang menyentuh domainnya. Membangun dulu baru cek = gagal.
2. **Trigger = panggil.** Cocok niat user + deskripsi skill → load otomatis, jangan tanya "mau pakai skill X?".
3. **Ikuti prosedurnya.** Langkah, checklist, template, dan script bawaan skill dipakai apa adanya. Jangan improvisasi jalur sendiri.
4. **Jangan sebut-sebut.** Terapkan diam-diam: jangan umumkan skill yang diload, jangan paste isi skill, jangan bocorkan kosakata internal ke deliverable.
5. **Sub-agent tidak mewarisi.** Saat delegasi, sebutkan skill yang wajib diload di brief.
6. **Verifikasi = bagian skill.** Checklist/validator bawaan skill dijalankan saat verifikasi, bukan dilewat.
7. **Bentrok = skill menang** atas default & kebiasaan, kecuali user eksplisit override — dan itu pun hanya untuk intent/konten, bukan mekanik.
8. **Skill baru** ditaruh di lokasi baku + didaftarkan di tabel §2 file ini.

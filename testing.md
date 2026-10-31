# testing.md — Aturan Uji, Perbaiki, Push

> Berlaku setelah SKILL.md (§1) dan arsitektur.md (§2) terpenuhi.
> Prinsip: AI punya vision — lihat kendalanya di mana, betulkan sampai jadi.

## 1. Uji di review/preview (wajib)

1. **Jalankan seperti user pakai.** Kode: run + lint + test. Web: buka di
   browser/tab review. Data: hitung ulang. Config: terapkan ke target aman.
2. **Cek checklist ini tiap deliverable:**
   - [ ] Jalan tanpa error di console/log
   - [ ] Tidak ada layar kosong/hitam/rusak
   - [ ] Semua tombol/aksi berfungsi, tidak ada yang mati
   - [ ] Sesuai arsitektur.md (tampilan, state, keterbacaan info)
   - [ ] Sama dengan sumber yang diminta (vision check §5 arsitektur.md)
   - [ ] Resize/360px tidak merusak layout (untuk UI)
3. **Bukti, bukan klaim.** Lolos = bisa ditunjukkan (screenshot/tab/log),
   bukan "kayaknya sudah benar".

## 2. Kalau ada kendala

1. Baca error/log/screenshot → tentukan lokasi persis (file:baris).
2. Betulkan akar masalah, bukan gejala. Satu perbaikan satu uji ulang.
3. Maksimal 2 putaran; gagal lagi = sebutkan 1 asumsi paling mungkin salah +
   minta 1 keputusan user. Jangan ngawur menebak.
4. Jangan tanya hal yang bisa dicek sendiri (baca file, cek console, coba run).

## 3. Push git (hanya atas perintah user)

1. **Login:** kalau belum login → login dulu. Kalau sudah login → langsung push,
   JANGAN tanya "push pakai akun mana" atau "push ke mana".
2. **Urutan:** `add` → `commit` (pesan jelas: apa + kenapa) → `push`.
3. **Repo baru:** `gh repo create <nama> --public --source=. --push` kecuali
   user minta private.
4. **Lapor singkat:** URL repo + apa yang berubah. Selesai.

## 4. Cara kerja AI (ringkas)

Kerja tuntas, jangan bengong, jangan ngawur, jangan banyak tanya. Solusi atau
rekomendasi boleh diajukan (maksimal 2–3 opsi + rekomendasi pertama), tapi
keputusan besar tetap di user. Yang bisa dikerjakan sendiri → kerjakan.

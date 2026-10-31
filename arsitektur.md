# arsitektur.md — Aturan Membangun Aplikasi

> WAJIB dipatuhi setiap develop aplikasi (web & native). Hasil harus sama
> dengan yang diminta — AI wajib punya vision: bandingkan output dengan sumber
> (mockup/foto/referensi) sampai tidak ada beda yang terlihat.

## 1. Target platform

| Jenis | Target |
|---|---|
| Web | Browser modern (Chrome/Edge/Firefox), responsif 360px → desktop |
| Native | Windows, macOS, Linux, Android (satu basis kode bila mungkin: Electron/Tauri/Flutter/React-Native) |

Keputusan framework ditulis di awal project dan tidak diganti di tengah jalan
kecuali user memerintahkan.

## 2. Framework & struktur

1. **Satu framework per project.** Jangan campur (misal React + jQuery).
2. **Struktur baku:** `src/` (kode), `public/` atau `assets/` (statis), `tests/`
   (uji), `docs/` (catatan). Config di root, jangan berserakan.
3. **Dependency minimal.** Pakai yang sudah ada sebelum tambah baru. Versi di-pin.
4. **Kode bersih:** satu fungsi satu tugas, nama jelas, tanpa kode mati/komentar
   sampah. Konsisten dengan pola file yang sudah ada.

## 3. UI/UX (turunan `archify`)

1. **Mobile-first.** Tidak boleh overlap/rusak di 360px. Cek 360px, 768px, desktop.
2. **Kontras aman.** Teks di atas gelap minimal `#f1f5f9`; jangan abu di atas abu.
3. **Skala konsisten.** Gap `0.5/0.75/1rem`, radius `8/12/16px`. Tombol `white-space: nowrap`.
4. **State jelas.** Loading (spinner/bar+%), error (pesan+aksi), kosong (empty
   state), sukses (konfirmasi). Tidak ada tombol mati tanpa feedback.
5. **Satu fokus per layar.** Sedikit warna, banyak ruang kosong, animasi halus
   bertujuan (200–500ms, `cubic-bezier(0.22,1,0.36,1)`), hormati `prefers-reduced-motion`.

## 4. Keterbacaan informasi

1. Informasi penting terlihat tanpa scroll/cari: status, angka, aksi utama.
2. Hierarki jelas: judul → ringkasan → detail. Label singkat, bahasa user.
3. Data + visual sinkron: angka di panel = angka di grafik/3D. Tidak ada beda.
4. Format konsisten: satuan, tanggal, mata uang, presisi desimal sama di semua layar.

## 5. Vision check (wajib sebelum selesai)

1. Bandingkan hasil render dengan sumber yang diminta (mockup/foto/contoh).
2. Daftar bedanya (warna, jarak, ukuran, posisi, teks) → betulkan satu per satu.
3. Maksimal 2 putaran perbaikan; putaran ke-3 = sebutkan asumsi yang paling
   mungkin salah + tanya user 1 keputusan.

## 6. Aturan 3D (bila ada, turunan `threejs`)

Renderer `antialias` + `pixelRatio ≤ 2` + `setAnimationLoop`; kamera 45–60°;
minimal 1 directional + 1 ambient/hemisphere; OrbitControls + damping; resize
handler; reuse geometry/material; loading + error + fallback WebGL.

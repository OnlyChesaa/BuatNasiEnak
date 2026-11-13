# BuatNasiEnak
Kalkulator pembuat nasi yang disertai timer, untuk membuat nasi yang SEMPURNA, ENAK, DAN BERGIZI.

# 🍚 Kalkulator & Timer Nasi Pintar

Aplikasi web ringan untuk menghitung air, durasi, dan langkah memasak nasi, lengkap dengan timer beralarm. Dibuat dengan HTML, CSS, dan JavaScript murni dalam satu file.

## Masalah

Nasi sering terlalu lembek atau terlalu keras karena takaran air dan waktunya hanya diperkirakan. Takaran juga berbeda untuk tiap alat (rice cooker, panci listrik, panci kompor) dan tiap jenis beras (putih, merah).

## Logika

Setiap kombinasi alat dan jenis beras punya **rasio air** dan **durasi dasar**:

| Alat | Beras | Rasio (beras : air) | Durasi dasar |
|---|---|---|---|
| Rice cooker | Putih / Merah | 1 : 1,2 / 1 : 1,5 | 35 / 55 menit |
| Panci listrik | Putih / Merah | 1 : 1,1 / 1 : 1,4 | 25 / 45 menit |
| Panci kompor | Putih / Merah | 1 : 1,5 / 1 : 2,0 | 25 / 50 menit |

Rumus:

```
air (ml) = jumlah cup × rasio × 180
durasi   = durasi dasar + (cup − 2) × 1,5 menit   // hanya jika cup > 2
```

Angka di atas adalah titik awal. Silakan sesuaikan dengan alat dan hasil masakanmu di objek `RECIPES`.

## Fitur

- Pilihan alat, jenis beras, dan jumlah beras dengan validasi (harus lebih dari 0)
- Hasil otomatis: jumlah air, durasi, dan langkah memasak sesuai alat
- Timer Mulai, Jeda, dan Atur ulang dengan lingkaran progres
- Alarm suara saat selesai memakai Web Audio API
- Tampilan responsif, mendukung mode gelap, dan bisa dipakai dengan keyboard
- Tanpa library dan tanpa build tool, cukup buka `index.html`

## Teknologi

- **HTML5**: struktur dan form yang mudah diakses
- **CSS3**: Grid, Flexbox, CSS Variables, `prefers-color-scheme`
- **JavaScript (Vanilla)**: manipulasi DOM, `setInterval` berbasis waktu akhir, Web Audio API

## Cara Menjalankan

1. Unduh atau *clone* repositori ini.
2. Buka `index.html` di browser.

## Rencana Pengembangan

- Menyimpan pengaturan terakhir dengan `localStorage`
- Menambah jenis beras (ketan, basmati)
- Menulis unit test untuk fungsi `calculate()`

## Pembuat

Dibuat oleh ChesaDoCode

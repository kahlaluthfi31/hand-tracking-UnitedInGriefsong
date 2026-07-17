# Hand Frame Effect (Web)

Versi browser dari Hand Frame Effect — jalan langsung di HP/laptop lewat kamera browser, tanpa install apa-apa. Semua deteksi tangan diproses lokal di device (MediaPipe Tasks Vision, via CDN), tidak ada video yang dikirim ke server manapun.

## Cara coba lokal dulu (opsional)

Buka file `index.html` ini langsung di browser TIDAK akan berfungsi penuh karena kamera butuh HTTPS atau localhost. Jalankan server lokal sederhana dulu:

```bash
npx serve .
```

lalu buka `http://localhost:3000` di browser.

## Deploy ke Vercel

### Opsi A — Lewat Vercel CLI (paling cepat, tanpa GitHub)

```bash
npm install -g vercel
cd hand-frame-web
vercel
```

Ikuti pertanyaan yang muncul (pilih akun, nama project, dsb), lalu Vercel akan kasih URL live yang bisa langsung dibuka di HP.

### Opsi B — Lewat GitHub + Vercel Dashboard

1. Push folder ini ke repo GitHub baru
2. Buka https://vercel.com/new
3. Import repo tersebut
4. Framework preset pilih **"Other"** (karena ini static HTML biasa, bukan Next.js/React)
5. Klik **Deploy**

## Catatan penting

- Karena ini akses kamera lewat browser, **wajib dibuka lewat HTTPS** (Vercel otomatis kasih HTTPS, jadi aman).
- Di HP, buka link Vercel-nya lewat Chrome (Android) atau Safari (iPhone), nanti browser akan minta izin akses kamera — izinkan.
- Tombol **⟲** di bawah buat ganti kamera depan/belakang, tombol **⛶** buat fullscreen.

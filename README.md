# Undangan 10 Tahun — Reza & Sofi

Undangan interaktif single-file HTML (pixel-art village + mini game).

## Isi folder
- `index.html` — undangannya, semua CSS/JS udah nyatu di file ini
- `package.json` — biar Railway auto-detect Node & serve file statis

## Cara deploy ke Railway

1. Push folder ini ke repo GitHub baru:
   ```bash
   git init
   git add .
   git commit -m "undangan reza sofi"
   git branch -M main
   git remote add origin https://github.com/USERNAME/undangan-reza-sofi.git
   git push -u origin main
   ```

2. Buka [railway.app](https://railway.app) → **New Project** → **Deploy from GitHub repo**
   → pilih repo `undangan-reza-sofi`

3. Railway otomatis:
   - Detect Node project
   - Jalanin `npm install` lalu `npm start` (yang isinya `npx serve -s . -l $PORT`)
   - Kasih URL publik `xxxx.up.railway.app`

4. (Opsional) Mau domain sendiri?
   Settings → Domains → tambahin custom domain → ikutin instruksi DNS. SSL otomatis dari Railway.

## Deploy tanpa GitHub (via CLI)

```bash
npm i -g @railway/cli
railway login
railway init
railway up
```

## Edit sebelum disebar
Jangan lupa edit di dalam `index.html`:
- `WA_NUMBER` (kalau nanti nambah fitur kirim ucapan lagi)
- Nama venue & alamat lengkap di bagian "Papan Acara"
- Foto galeri (ganti placeholder `<div class="slot">` jadi `<img src="...">`)

## Musik latar
Ada tombol nyala/matikan musik (🔈/🔊) di pojok kanan atas halaman explore.
Supaya bunyi, taruh file audio kamu sendiri di folder ini dengan nama **`bgm.mp3`**
(satu folder sejajar dengan `index.html`). Pakai file yang legal milikmu sendiri
atau musik royalty-free — jangan pakai lagu berhak cipta tanpa izin/lisensi.
Kalau file `bgm.mp3` belum ada, tombolnya tetap muncul tapi otomatis nggak bersuara.

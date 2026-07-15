# ⚡ Kalkulator Posisi — Risk 1%

Kalkulator position sizing untuk crypto futures (leverage 5x, isolated, risk 1% per trade).
Satu file HTML statis — tanpa build, tanpa dependency, semua kalkulasi berjalan offline di perangkat.

## Fitur

- 📋 **Paste sinyal** dari grup → auto-isi Pair, Arah, Entry, SL, TP
- 💰 Hitung risk amount, initial margin, position size, notional
- 📍 Estimasi harga liquidation + cek apakah SL masih aman
- 🎯 Take profit berlapis (TP1/TP2/TP3) dengan estimasi profit bersih setelah fee
- 📱 Responsif: satu kolom di HP, dua kolom di desktop
- ⚡ PWA: bisa di-install ke home screen dan jalan **offline** setelah kunjungan pertama
- 💾 Input tersimpan otomatis di perangkat (localStorage)

## Deploy ke GitHub Pages

1. Buat repository baru di GitHub (misal `kalkulator-posisi`).
2. Upload semua file di folder ini (`index.html`, `manifest.json`, `sw.js`, `icon.svg`, `README.md`):

   ```bash
   git init
   git add index.html manifest.json sw.js icon.svg README.md
   git commit -m "Kalkulator posisi risk 1%"
   git branch -M main
   git remote add origin https://github.com/<username>/kalkulator-posisi.git
   git push -u origin main
   ```

3. Di GitHub: **Settings → Pages → Source: Deploy from a branch → Branch: `main` / root → Save**.
4. Tunggu ±1 menit, lalu buka `https://<username>.github.io/kalkulator-posisi/`.

> Catatan: setiap kali mengubah `index.html`, naikkan versi cache di `sw.js`
> (`kalkulator-posisi-v1` → `-v2`, dst.) agar pengguna lama mendapat versi terbaru.

## Jalankan lokal

Cukup buka `index.html` di browser, atau:

```bash
python3 -m http.server 8000
# buka http://localhost:8000
```

## Parameter tetap

| Parameter | Nilai |
|---|---|
| Leverage | 5x |
| Mode margin | Isolated |
| Risk per trade | 1% dari balance |
| Taker fee | 0,05% per sisi |
| MMR (estimasi liq) | 0,5% |

⚠️ **Disclaimer:** alat bantu edukasi, bukan saran finansial. Estimasi liquidation adalah perkiraan — selalu verifikasi di exchange.

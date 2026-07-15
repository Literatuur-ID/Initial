# ⚡ Kalkulator Posisi — Risk 1%

Kalkulator position sizing untuk crypto futures (leverage 5x, isolated, risk 1% per trade).
Satu file HTML statis — tanpa build, tanpa dependency, semua kalkulasi berjalan offline di perangkat.

## Fitur

- 📋 **Paste sinyal** dari grup → auto-isi Pair, Arah, Entry, SL, TP
- 💰 Hitung risk amount, initial margin, position size, notional
- 📍 Estimasi harga liquidation + cek apakah SL masih aman
- 🎯 Take profit berlapis (TP1/TP2/TP3) dengan estimasi profit bersih setelah fee
- 💾 Input tersimpan otomatis di perangkat (localStorage)

## Parameter tetap

| Parameter | Nilai |
|---|---|
| Leverage | 5x |
| Mode margin | Isolated |
| Risk per trade | 1% dari balance |
| Taker fee | 0,05% per sisi |
| MMR (estimasi liq) | 0,5% |

⚠️ **Disclaimer:** alat bantu edukasi, bukan saran finansial. Estimasi liquidation adalah perkiraan — selalu verifikasi di exchange.

# SawitMonitor — Minyak Sawit

Dashboard monitoring **minyak sawit**: harga CPO, harga minyak goreng per provinsi, stok depot, ekspor, distribusi, produsen, dan jejak batch.

Demo: https://sawit-monitor.vercel.app

## Fitur

- **Dashboard** — KPI harga CPO (USD/ton), curah (Rp/kg), stok nasional, ekspor; grafik CPO 12 bulan; kondisi pasar; peringatan harga
- **Harga Minyak** — CPO vs curah (indeks), tabel curah / Minyakita / premium per provinsi vs HET
- **Stok & Depot** — Leaflet dark, marker depot (ukuran = stok, warna = status), filter defisit
- **Produksi & Ekspor** — CPO vs minyak goreng, tabel ekspor per negara tujuan
- **Distribusi** — truk tangki & kontainer, ETA, utilisasi refinery
- **Produsen** — refinery + merek kemasan + sertifikat ISPO, pencarian
- **Traceability** — batch CPO → refinery → kemasan → distributor sebagai blok hash

## Jalankan

Buka `index.html`. Tanpa build. Leaflet & font dari CDN.

## Kustomisasi

| Konstanta | Isi |
|---|---|
| `CPO`, `CURAH` | seri harga 12 bulan (USD/ton, Rp/kg) |
| `PROD_CPO`, `PROD_MG` | produksi bulanan (ribu ton) |
| `HARGA` | per provinsi: curah, Minyakita, premium, HET |
| `DEPOT` | depot: koordinat, stok, kapasitas, status |
| `EKSPOR`, `DIST`, `REFINERY`, `PRODUSEN`, `ALERT`, `LEDGER` | tabel operasional |

Semua data ilustratif.

## Deploy

Static site. `vercel --prod` atau push ke `main`.

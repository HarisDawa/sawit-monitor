# SawitMonitor

Dashboard monitoring kebun sawit: peta blok, produksi TBS, harga, armada, petani mitra, dan jejak panen (traceability).

Demo: https://sawit-monitor.vercel.app

## Fitur

- **Dashboard** — KPI luas kebun, produksi, harga, petani; grafik produksi 12 bulan; status blok; tugas panen
- **Peta Kebun** — Leaflet + tile gelap, marker per blok (warna = status), filter "siap panen"
- **Produksi** — tonase + rendemen CPO, tabel panen terbaru
- **Harga TBS** — tren 12 bulan, harga per provinsi vs plafon Disbun
- **Armada & PKS** — posisi truk, muatan, ETA, utilisasi pabrik
- **Petani Mitra** — pencarian nama/koperasi, luas lahan, status plasma/swadaya
- **Traceability** — blok hash per event panen, audit sampai kebun asal

## Jalankan

Buka `index.html` di browser. Tanpa build. Leaflet & font dari CDN.

## Kustomisasi

Semua data dummy di `<script>` bawah:

| Konstanta | Isi |
|---|---|
| `BLOK` | blok kebun: koordinat, luas, status, umur, produksi |
| `PRODUKSI`, `HARGA_TREN`, `RENDEMEN` | seri 12 bulan |
| `HARGA` | harga per provinsi + plafon |
| `PANEN`, `TUGAS`, `ARMADA`, `PKS`, `PETANI`, `LEDGER` | tabel-tabel operasional |

Ganti koordinat di `BLOK` → peta ikut menyesuaikan.

## Deploy

Static site. `vercel --prod` atau push ke `main` (auto-deploy).

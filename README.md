# UTS Data Acquisition & Management — Kelas F

## Akuisisi dan Penggabungan Data Kunjungan Wisatawan pada Daya Tarik Wisata di Kota Denpasar, Bali

### 1. Data Diri

- **Nama:** Mario Julio Rusbugowa Ndada
- **NIM:** 2501010227
- **Kelas:** F
- **Program Studi:** Informatika — INSTIKI

### 2. Sumber URL (Tabel)

| No | Metode Akuisisi | Nama Dataset/Sumber | URL Sumber | Format Mentah (`data/raw`) | Format Hasil (`Proses`) |
|---|---|---|---|---|---|
| 1 | Download | Perkembangan Kunjungan Wisatawan Nusantara ke Daya Tarik Wisata Kota Denpasar | [Satu Data Denpasar](https://satudata.denpasarkota.go.id/id/dataset/perkembangan-kunjungan-wisatawan-domestik-ke-daya-tarik-wisata-di-kota-denpasar) | `kunjungan_dtw_denpasar_raw.csv` | `kunjungan_dtw_denpasar_bersih.csv` |
| 2 | API | Open-Meteo Historical Weather API (Kota Denpasar) | [Open-Meteo](https://open-meteo.com/) | `cuaca_denpasar_raw.json` | `cuaca_denpasar_normalisasi.json` |
| 3 | Scraping | Jumlah Perjalanan Wisatawan Nusantara Menurut Kabupaten/Kota di Bali (BPS) | [BPS Bali](https://bali.bps.go.id/en/statistics-table/2/NDEzIzI%3D/jumlah-perjalanan-wisatawan-nusantara-menurut-kabupaten-kota-.html) | `perjalanan_wisnus_bali_raw.html` | `perjalanan_wisnus_bali_bersih.html` |

### 3. Goal (Tujuan)

Proyek ini bertujuan untuk mengumpulkan dan menggabungkan data kunjungan wisatawan pada daya tarik wisata di Kota Denpasar dengan data cuaca dan statistik perjalanan wisatawan. Proses akuisisi dilakukan melalui metode download, API, dan scraping.

Data yang diperoleh kemudian dibersihkan, dinormalisasi, dan digabungkan menggunakan Python dan Pandas. Proyek ini juga memperhatikan etika penggunaan data, sumber data, lisensi, provenance, serta pencatatan MD5. Hasil akhirnya berupa dataset yang lebih terstruktur untuk membantu melihat perkembangan kunjungan wisatawan dan hubungannya dengan kondisi cuaca di Kota Denpasar.

### 4. Struktur Folder dan File

```text
uts_data_acquisition_management/
│
├── data/
│   └── raw/
│       ├── download/
│       │   └── kunjungan_dtw_denpasar_raw.csv
│       │
│       ├── api/
│       │   └── cuaca_denpasar_raw.json
│       │
│       └── scraping/
│           └── perjalanan_wisnus_bali_raw.html
│
├── Proses/
│   ├── kunjungan_dtw_denpasar_bersih.csv
│   ├── cuaca_denpasar_normalisasi.json
│   ├── perjalanan_wisnus_bali_bersih.html
│   └── gabungan_kunjungan_cuaca_denpasar.csv
│
├── catatan_provenance.csv
└── data_ethics_checklist.csv
```

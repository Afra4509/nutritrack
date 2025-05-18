# NutriTrack: Aplikasi Pencegahan Stunting

NutriTrack adalah aplikasi dashboard berbasis Shiny yang dirancang untuk membantu dalam pemantauan dan pencegahan stunting pada balita. Aplikasi ini menyediakan visualisasi data pertumbuhan, rekomendasi nutrisi, dan alat pelacakan perkembangan anak dengan memanfaatkan database standar WHO dan data stunting dari Indonesia.

## Fitur Utama

- **Dashboard Pemantauan**: Melacak pertumbuhan anak dengan visualisasi interaktif
- **Analisis Nutrisi**: Evaluasi kecukupan asupan nutrisi harian
- **Visualisasi Data Stunting**: Menyajikan data stunting di seluruh provinsi Indonesia
- **Grafik Pertumbuhan WHO**: Membandingkan pertumbuhan anak dengan standar WHO
- **Rekomendasi Menu**: Saran menu sehat sesuai kebutuhan nutrisi anak
- **Pelacakan Perkembangan**: Grafik pertumbuhan yang membandingkan dengan standar WHO
- **Edukasi Stunting**: Materi informasi tentang pencegahan stunting

## Dataset

Aplikasi ini menggunakan beberapa dataset utama:

1. **Data Standar Pertumbuhan WHO**: Standar median tinggi badan dan deviasi standar berdasarkan usia dan jenis kelamin.
2. **Data Stunting Indonesia**: Dataset yang berisi informasi jumlah balita, kasus stunting, kategori pendek dan sangat pendek, serta prevalensi stunting di 38 provinsi Indonesia pada tahun 2023.

## Link websitenya

https://afra1502.shinyapps.io/masyaniw/

## Instalasi

### Prasyarat

Pastikan Anda telah menginstal:
- R (versi 4.0.0 atau lebih baru)
- RStudio (disarankan untuk pengembangan)

### Cara Install

1. Clone repositori ini:
   ```
   git clone https://github.com/Afra4509/nutritrack.git
   ```

2. Buka R atau RStudio dan install paket yang diperlukan:
   ```R
   install.packages(c("shiny", "ggplot2", "dplyr", "shinydashboard", "plotly", "shinyWidgets", "shinycssloaders"))
   ```

3. Buka file `app.R` dan jalankan aplikasi:
   ```R
   shiny::runApp()
   ```

## Cara Penggunaan

1. Masukkan data anak (nama, usia, jenis kelamin, berat badan, dan tinggi badan)
2. Lihat visualisasi status gizi dan pertumbuhan
3. Dapatkan rekomendasi nutrisi harian
4. Pantau perkembangan anak dari waktu ke waktu

## Struktur Aplikasi

```
nutritrack/
│
├── app.R                # Aplikasi utama
├── R/                   # Fungsi-fungsi pendukung
│   ├── modules.R        # Modul Shiny 
│   ├── utils.R          # Fungsi utilitas
│   └── data_processing.R # Pemrosesan data
│
├── data/                # Data statis 
│   ├── food_database.csv # Database makanan dan nutrisi
│   └── who_standards.csv # Standar pertumbuhan WHO
│
├── www/                 # Aset web
│   ├── styles.css       # CSS kustom
│   └── images/          # Gambar dan ikon
│
└── tests/               # Unit tests
```

## Kontribusi

Kontribusi pada proyek ini sangat dihargai! Berikut cara Anda dapat berkontribusi:

1. Fork repositori
2. Buat branch fitur (`git checkout -b feature/AmazingFeature`)
3. Commit perubahan Anda (`git commit -m 'Add some AmazingFeature'`)
4. Push ke branch (`git push origin feature/AmazingFeature`)
5. Buka Pull Request


## Link proyek

Link Proyek: [https://github.com/Afra4509/nutritrack](https://github.com/Afra4509/nutritrack)

## Ucapan Terima Kasih

- [Kementerian Kesehatan RI](https://www.kemkes.go.id/)
- [WHO](https://www.who.int/)
- [Shiny](https://shiny.rstudio.com/)

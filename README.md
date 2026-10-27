# Tugas Besar Strategi Algoritma

Notebook Jupyter untuk sistem rekomendasi jalur evakuasi tercepat bagi desa rawan banjir. Sistem mencari titik evakuasi terdekat dari sebuah desa berdasarkan jarak tempuh melalui jaringan jalan, bukan jarak garis lurus. Proyek ini merupakan tugas besar mata kuliah Strategi Algoritma, dengan wilayah studi Kabupaten Cilacap.

Seluruh proses ada di berkas `Percobaan1.ipynb`.

## Fitur

- Memuat data desa rawan banjir dan data tempat evakuasi dari berkas CSV.
- Membersihkan data koordinat, termasuk konversi ke numerik dan pembuangan data di luar wilayah Cilacap.
- Memetakan titik banjir dan titik evakuasi dalam peta interaktif Folium.
- Mengunduh jaringan jalan Kabupaten Cilacap dari OpenStreetMap memakai OSMnx.
- Menempelkan titik desa dan titik evakuasi ke node jalan terdekat (snapping).
- Menghitung rute jalan terpendek ke titik evakuasi terdekat dengan algoritma pencarian jalur terpendek pada graf.
- Menampilkan rute hasil perhitungan di peta, beserta gambar struktur jaringan jalan untuk bahan presentasi.

## Teknologi

- Python 3 dan Jupyter Notebook
- Pandas untuk pengolahan data
- OSMnx dan NetworkX untuk jaringan jalan dan perhitungan rute
- Folium untuk peta interaktif
- Matplotlib dan Seaborn untuk visualisasi tambahan

## Cara Instalasi

Prasyarat: Python 3 dan Jupyter Notebook atau JupyterLab. Notebook ini awalnya dibuat di Google Colab, jadi cara termudah menjalankannya adalah membuka berkas `Percobaan1.ipynb` di Colab melalui badge Open in Colab pada sel pertama.

Untuk menjalankan lokal, pasang dependensi berikut:

```bash
pip install pandas folium osmnx networkx matplotlib seaborn
```

Data tidak disertakan di repositori ini. Notebook membaca dua berkas dari Google Drive:

- `data_desa_rawan_clean.csv` berisi data desa rawan banjir.
- `tempat_evakuasi_clean.csv` berisi data tempat evakuasi.

Sesuaikan path pada sel pemuatan data dengan lokasi kedua berkas tersebut di lingkungan Anda.

## Cara Menjalankan

1. Buka `Percobaan1.ipynb` di Jupyter atau Google Colab.
2. Jalankan sel secara berurutan dari atas ke bawah.
3. Sel awal memasang paket, memuat data, dan membersihkannya.
4. Sel berikutnya menggambar peta titik banjir dan evakuasi.
5. Sel lanjutan mengunduh jaringan jalan Cilacap, melakukan snapping titik, lalu menghitung dan menampilkan rute evakuasi terdekat untuk desa sampel.

Koneksi internet dibutuhkan karena jaringan jalan diunduh dari OpenStreetMap pada saat notebook dijalankan.

## Lisensi

Proyek ini memakai lisensi MIT. Lihat berkas [LICENSE](LICENSE) untuk teks lengkapnya.

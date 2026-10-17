# Analisis What-if dan SWIFRA — Deck Kuliah

Deck presentasi akademik tentang analisis **"what-if"** dan **Structured What-if
Risk Assessment (SWIFRA)**, disusun dari bab 7 buku *Risk Assessment: A
Practical Guide to Assessing Operational Risks* (Lyon & Popov, 2022) dengan
studi kasus ledakan tangki limbah pestisida Bayer CropScience, Institute,
Virginia Barat, 2008.

Mata kuliah: Proses Industri dan Manajemen Risiko — modul lanjutan.
Program Studi Kesehatan Masyarakat Program Sarjana.
Pemateri: Team Teaching MK.

## Isi berkas

| Berkas | Keterangan |
|---|---|
| `index.html` | Deck lengkap, 49 slide, satu berkas mandiri (reveal.js dari CDN) |
| `deck.pdf` | Ekspor PDF, 49 halaman, 960 × 540 pt (16:9), teks dapat dicari |
| `figures/` | 11 gambar, semuanya diekstrak dari PDF sumber |

## Cara memakai

Presentasi — buka `index.html` di peramban:

- `F` layar penuh, `S` tampilan penyaji (catatan penyaji + pewaktu), `Esc` ikhtisar
- `→` `←` navigasi, `B` mengosongkan layar, `?` bantuan
- Setiap slide punya catatan penyaji yang memuat isi yang diucapkan, bukan yang tertulis
- Lima slide memakai pemunculan bertahap (lihat di bawah) — `→` menampilkan satu bagian sekaligus

### Lapisan gerak (motion)

Deck ini beranimasi, dan animasinya dipakai untuk mengatur tempo mengajar — bukan
sebagai hiasan. Yang ada di dalamnya:

| Bagian | Perilaku |
|---|---|
| Masuk slide | Judul, blok isi, kolom, dan baris tabel muncul berjenjang dalam urutan baca |
| Angka pemisah bagian | Tumbuh masuk dengan sedikit penskalaan |
| Perpindahan antar slide | Geser (`slide`), bukan sekadar pudar |
| Lima slide terpilih | Pemunculan bertahap pada bagian yang tidak boleh dibaca lebih dulu |

Slide dengan pemunculan bertahap sengaja dipilih karena membocorkan jawabannya
akan merusak latihannya:

- **slide 19** — kelemahan terbesar what-if tradisional, lalu akibatnya
- **slide 39** — apa yang dilakukan tim dangkal, lalu akibatnya
- **slide 40** — empat pertanyaan berantai kasus, satu per satu, supaya eskalasinya terasa
- **slide 46** — tiga pembeda analisis dangkal dan analisis berguna
- **slide 49** — pertanyaan penutup dari sumber

Yang penting untuk pemeliharaan:

- **Isi tidak pernah disembunyikan oleh gaya dasar.** Animasi hanya menambahkan
  gerak. Bila animasi gagal atau JavaScript mati, yang hilang hanyalah geraknya,
  bukan isi slide.
- **`prefers-reduced-motion` mematikan seluruh lapisan gerak** bagi pengguna yang
  memintanya di sistem operasinya.
- **PDF sama sekali tidak terpengaruh.** Semua animasi dimatikan di `@media print`,
  dan pemunculan bertahap dicetak dalam keadaan akhir. Ekspor ulang menghasilkan
  halaman yang identik dengan `deck.pdf`; sudah diperiksa halaman per halaman.

Ekspor PDF ulang (butuh Edge atau Chrome):

```bash
python <skills>/academic-html-deck/scripts/export_pdf.py index.html -o deck.pdf
```

Pemeriksaan mutu otomatis:

```bash
python <skills>/academic-html-deck/scripts/check_slides.py index.html
```

## Alur deck

| Bagian | Slide | Isi |
|---|---|---|
| Pembuka | 1–3 | Sampul, tujuan pembelajaran, pertanyaan pembuka |
| 01 | 4–9 | Asal usul metode dan kedudukan normatifnya |
| 02 | 10–14 | Proses sepuluh langkah dan peran tim |
| 03 | 15–19 | Lembar what-if tradisional, manfaat, dan kelemahannya |
| 04 | 20–29 | SWIFRA, lembar kerjanya, dan matriks risikonya |
| 05 | 30–45 | Studi kasus: rekaman sumber, perbandingan kedua metode |
| Penutup | 46–49 | Sintesis dan referensi |

Slide 31 membuka studi kasus dengan cuplikan sub-bab 7.8 buku sumber, sehingga
pernyataan ringkas peristiwa itu ada di depan mata mahasiswa sebelum rincian
dilaporkan satu per satu. Deck ini tidak memuat latihan kelompok tertanam;
kegiatan kelas diarahkan melalui catatan penyaji.

Tesis deck ini: analisis what-if mudah dipakai, dan justru karena itu paling
sering dipakai secara dangkal. Kelemahan mendasarnya adalah ia sebuah *analisis
bahaya*, bukan *penilaian risiko* — ia tidak memuat penaksiran risiko, sehingga
semua bahaya terlihat setara dan sukar diprioritaskan. SWIFRA menambahkan
taksiran risiko dan dua pertanyaan lanjutan (*bagaimana* dan *mengapa*), lalu
studi kasus memperlihatkan selisih kesimpulan yang dihasilkan.

## Sumber gambar — mohon dibaca sebelum dipublikasikan

Kesebelas gambar diekstrak dari PDF sumber dengan PyMuPDF pada 300 DPI; tabel
yang digambar sebagai vektor (matriks risiko, lembar kerja) dirender sebagai
potongan halaman, sedangkan foto diambil sebagai citra tertanam. Tiga foto
dikonversi ke JPEG agar ukuran PDF turun dari 12,6 MB ke 2,3 MB.

Satu berkas lagi, `figures/csb-summary-excerpt.png` (340 DPI), adalah potongan
halaman buku: judul sub-bab 7.8 &ldquo;CSB Investigation Summary&rdquo; beserta paragraf
pertamanya, yang menguraikan peristiwa secara ringkas. Kupasan dilakukan
berdasarkan koordinat lapisan teks sehingga potongan berhenti tepat di batas
paragraf dan tidak menyertakan cap unduhan Wiley. Ia dipakai pada slide 31
sebagai dokumen sumber yang dapat diverifikasi mahasiswa.

Perhatikan status hak cipta:

- **Gambar 7.1, 7.2, 7.3, 7.4, 7.7, 7.8, Tabel 7.2, dan potongan sub-bab 7.8**
  berasal dari buku Lyon & Popov (2022), © 2022 John Wiley & Sons. Dipakai di
  sini untuk pembelajaran, dengan atribusi lengkap pada setiap keterangan.
- **Gambar 7.5, 7.6 dan 7.9** berasal dari laporan akhir investigasi CSB (2011),
  sebuah dokumen publik pemerintah Amerika Serikat.

Mengunggah gambar berhak cipta Wiley ke repositori publik adalah redistribusi,
bukan pemakaian kelas. Bila deck ini akan dipublikasikan, pertimbangkan salah
satu dari: menjadikan repositori privat, mengeluarkan `figures/` dari riwayat
(gitignore) dan menyediakan skrip ekstraksi, atau menggambar ulang diagramnya.

Untuk menggambar ulang matriks risiko dan lembar kerja, cukup pakai tabel HTML
biasa — deck ini sudah memuat versi teks dari isi matriks pada slide 26–29,
sehingga gambar matriks dapat dilepas tanpa kehilangan isi.

## Rujukan utama

Lyon, B. K., & Popov, G. (2022). Chapter 7: "What-if" analysis methods. Dalam
G. Popov, B. K. Lyon, & B. Hollcroft, *Risk Assessment: A Practical Guide to
Assessing Operational Risks* (edisi ke-2). Hoboken, NJ: John Wiley & Sons.
doi:10.1002/9781119798323.ch7

U.S. Chemical Safety Board. (2011). *Bayer CropScience Pesticide Waste Tank
Explosion*. Laporan akhir, 20 Januari 2011.

Daftar lengkap ada pada slide 47–48.

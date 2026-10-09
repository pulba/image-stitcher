# Image Stitcher

Aplikasi web ringan untuk menggabungkan beberapa gambar menjadi satu gambar panjang secara vertikal. Cukup buka satu file HTML di browser, lalu tempel atau unggah gambar, atur urutannya, dan ekspor hasilnya sebagai PNG atau PDF.

## Fitur

- **Paste gambar langsung** dengan `Ctrl + V`.
- **Upload banyak gambar** sekaligus melalui pemilih file.
- **Drag-and-drop** gambar dari komputer ke area input.
- **Urutan otomatis**, gambar terbaru ditambahkan ke bagian paling atas.
- **Atur urutan gambar** dengan menyeret gambar atau menggunakan tombol naik dan turun.
- **Kelola daftar gambar**, termasuk menghapus gambar tertentu atau menghapus semua gambar.
- **Atur kanvas**, termasuk lebar, skala gambar, perataan, margin, jarak antar-gambar, dan warna latar.
- **Pratinjau langsung** dengan kontrol zoom dan fitur Fit.
- **Copy Image**, menyalin seluruh hasil gabungan sebagai satu gambar PNG ke clipboard.
- **Download PNG** untuk menyimpan gambar gabungan.
- **Export PDF** dalam mode satu halaman panjang atau beberapa halaman.
- **Pemrosesan lokal**, gambar tidak diunggah ke server.

## Mulai Menggunakan

1. Unduh `image-stitcher.html`.
2. Buka file tersebut menggunakan browser modern seperti Google Chrome atau Microsoft Edge.
3. Salin gambar dari browser, aplikasi, atau sumber lain.
4. Kembali ke Image Stitcher dan tekan `Ctrl + V`.
5. Ulangi untuk menambahkan gambar lainnya. Gambar terbaru akan muncul di bagian paling atas.
6. Atur urutan gambar dan pengaturan kanvas sesuai kebutuhan.
7. Pilih salah satu tindakan ekspor:
   - **Copy Image** untuk menyalin hasil gabungan.
   - **Download PNG** untuk menyimpan hasil sebagai gambar.
   - **Export PDF** untuk membuat dokumen PDF.

## Mengubah Urutan Gambar

- Seret gambar ke posisi yang diinginkan menggunakan pegangan di sebelah kiri.
- Gunakan tombol `↑` untuk memindahkan gambar ke atas.
- Gunakan tombol `↓` untuk memindahkan gambar ke bawah.
- Gunakan tombol `×` untuk menghapus gambar dari daftar.

Urutan dalam daftar menentukan urutan gambar pada hasil akhir, dari atas ke bawah.

## Pengaturan Kanvas

| Pengaturan | Fungsi |
|---|---|
| Lebar kanvas | Mengikuti gambar terlebar atau menggunakan lebar khusus. |
| Skala gambar | Menyesuaikan gambar dengan lebar kanvas atau mempertahankan ukuran asli. |
| Perataan | Menempatkan gambar di kiri, tengah, atau kanan. |
| Margin luar | Mengatur ruang di tepi kanvas. |
| Jarak antar-gambar | Mengatur jarak vertikal antar-gambar. |
| Warna latar | Menentukan warna ruang kosong pada kanvas. |
| Latar pratinjau | Mengubah tampilan area pratinjau tanpa mengubah hasil ekspor. |

## Ekspor PNG dan PDF

### PNG

File PNG mempertahankan susunan gambar, margin, jarak, perataan, dan warna latar sesuai pengaturan kanvas. Gunakan opsi ini jika kamu membutuhkan satu gambar utuh.

### PDF

Tersedia dua mode PDF:

- **Satu halaman panjang** untuk menyimpan hasil gabungan sebagai satu halaman.
- **Beberapa halaman** untuk membagi hasil menjadi halaman yang lebih mudah dicetak atau dibaca.

Ukuran halaman yang tersedia adalah A4, A3, dan Letter. Orientasi halaman dapat diatur menjadi portrait atau landscape, dengan margin halaman yang dapat disesuaikan.

## Kebutuhan

- Browser modern yang mendukung HTML5, Canvas, File API, dan JavaScript.
- Koneksi internet diperlukan untuk memuat library PDF dari CDN saat menggunakan fitur Export PDF.
- Fitur Copy Image bergantung pada dukungan clipboard gambar dan izin browser. Jika tidak tersedia, gunakan Download PNG.

Tidak perlu Node.js, npm, backend, database, atau proses build.

## Privasi

Gambar diproses di browser pada perangkat pengguna. Aplikasi tidak menyediakan fungsi untuk mengunggah gambar ke server. Data gambar disimpan sementara selama halaman terbuka dan dapat hilang ketika halaman ditutup atau dimuat ulang.

## Batasan

- Browser memiliki batas memori dan dimensi kanvas. Gabungan gambar yang sangat besar dapat gagal ditampilkan atau diekspor.
- Dukungan clipboard gambar dapat berbeda menurut browser dan cara file HTML dibuka.
- Export PDF memerlukan akses internet untuk memuat library eksternal.
- Aplikasi ini berjalan secara lokal dan tidak menyinkronkan daftar gambar antarperangkat.

## Struktur Proyek

```text
image-stitcher/
└── image-stitcher.html
```

HTML, CSS, dan JavaScript utama berada dalam satu file agar mudah dijalankan dan dipindahkan.

## Pemecahan Masalah

**Gambar tidak masuk setelah menekan `Ctrl + V`**
Pastikan sumber benar-benar menyalin gambar ke clipboard, bukan hanya menyalin alamat gambar. Klik area paste, lalu coba lagi.

**Copy Image gagal**
Periksa izin clipboard browser. Coba jalankan file melalui localhost atau HTTPS, atau gunakan Download PNG.

**PDF tidak bisa dibuat**
Pastikan koneksi internet aktif agar library PDF dapat dimuat. Muat ulang halaman lalu coba kembali.

**Hasil terlalu besar**
Kurangi lebar kanvas, jumlah gambar, margin, atau jarak antar-gambar. Untuk PDF, gunakan mode beberapa halaman.

**Gambar tampil dengan urutan yang salah**
Periksa urutan pada daftar gambar. Gambar yang berada paling atas akan muncul paling awal pada hasil gabungan.

## Lisensi

Gunakan dan modifikasi file ini sesuai kebutuhan pribadi atau proyekmu. Jika mendistribusikannya kembali, pastikan penggunaan library eksternal tetap mengikuti ketentuan lisensinya.

## Catatan Minggu 04 : Polymorphism

## Yang Saya Kerjakan
Di Tugas Minggu 4 ini aku mengerjakan Polymorphism di proyek Aset-Pinjam. Aku meng-override method hitungDenda di Ruang, Laptop, dan AlatLab supaya tiap jenis aset punya perhitungan denda sendiri, lalu membuat dua method cari di KatalogAset dengan parameter berbeda (kata saja, dan kata plus jenis aset). Dari sini aku paham bahwa overriding itu subclass menulis ulang method parent dengan signature sama, sedangkan overloading itu nama method sama tapi parameternya beda.

## Keputusan Desain
Keputusan desain saya, validasi hari negatif dan hitungan denda saya taruh di tiap subclass (Ruang, Laptop, AlatLab). Dendanya hari terlambat × multiplier jenis × tarif dari Varian.aktif().dendaPerHari. Saya pilih cara ini karena lebih simpel untuk tugas minggu ini, walaupun validasinya jadi tertulis di tiga tempat. Sebenarnya bisa juga ditaruh di Aset supaya tidak diulang-ulang. Untuk cari, cari(kata, jenis) saya buat memanggil cari(kata) dulu lalu disaring berdasarkan jenis, jadi logika pencocokan namanya tidak ditulis dua kali.

## Kendala
Kendala yang saya alami minggu ini ada dua. Pertama, saat pertama kali menjalankan tes dengan .\scripts\uji.ps1, hasilnya Tests run: 0 karena skrip itu ternyata menjalankan modul yang salah, sehingga saya belum tahu kode saya benar atau tidak. Setelah menambahkan parameter -Minggu 4, tesnya baru berjalan dengan benar. Kedua, saya sempat bingung mencari class Varian karena yang saya temukan awalnya hanya varian.md. Dari bagian import di file tes, saya baru tahu class itu ada di package config, sehingga saya bisa mengimpornya di Laptop, Ruang, dan AlatLab. Setelah dua hal itu teratasi dan method cari selesai diisi, semua 27 tes lulus.

## Penggunaan AI
- Alat yang dipakai : Claude
- Bagian yang dibantu AI : Saya menggunakan AI (Claude) untuk tiga hal utama memahami soal beserta perbedaan overriding dan overloading, menyusun kerangka kode hitungDenda dan cari, serta membantu membaca hasil tes saat tes awalnya tidak berjalan. Kode saya tulis, simpan, dan jalankan sendiri, lalu saya verifikasi lewat tes sampai semua lulus.
- Promp utama :
    a. Bantu aku paham soal minggu 4, beda overriding sama overloading.
    b. Cara bikin dua method cari di KatalogAset itu gimana, terutama yang pakai jenis aset?
    c. Kok hasil tesnya Tests run: 0? Gimana biar tesnya beneran jalan?
- Yang saya ubah atau tolak dari saran AI : Tidak ada
- Satu hal yang saya pahami lebih baik sekarang:Satu hal yang saya pahami lebih baik sekarang adalah perbedaan overriding dan overloading. Overriding adalah subclass menulis ulang method parent dengan nama dan parameter yang sama, seperti hitungDenda di Ruang, Laptop, dan AlatLab, sedangkan overloading adalah nama method sama dengan parameter berbeda, seperti cari(kata) dan cari(kata, jenis) di KatalogAset.
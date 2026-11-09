## Catatan Minggu 03 : Inheritance

## Yang Saya Kerjakan
Di tugas Minggu 3, saya memperbaiki error pada class Ruang, Laptop, dan AlatLab. Penyebab utamanya adalah baris throw new UnsupportedOperationException("TODO...") dari template yang belum dihapus, ditambah kurung kurawal yang salah dan method yang tertulis dua kali. Saya juga memasang Maven agar tes bisa dijalankan lewat terminal. Sisa satu error di AlatLab.java, yang tinggal diganti isinya, disimpan, lalu dites ulang sampai BUILD SUCCESS.

## Keputusan Desain
Saya membuat Ruang, Laptop, dan AlatLab sebagai turunan dari Aset supaya atribut dasar seperti kode dan nama tidak saya tulis berulang. Pengecekan data saya taruh di constructor dan akan melempar IllegalArgumentException kalau datanya tidak valid, jadi objek yang terbentuk selalu berisi data yang benar. Semua field saya buat private final supaya tidak bisa diubah setelah objek dibuat. Setiap kelas juga saya override method getJenis() agar semua jenis aset bisa disimpan dalam satu daftar Aset.

## Kendala
Awalnya muncul puluhan error merah karena baris throw new UnsupportedOperationException("TODO...") dari template belum saya hapus, ditambah kurung kurawal yang salah dan method yang tertulis dua kali. Saat menjalankan tes, PowerShell menolak script dan Maven belum dikenali, jadi saya mengubah execution policy dan mengatur PATH Maven. Saya juga sempat bingung karena error tidak berubah, ternyata file belum disimpan, sehingga sekarang saya selalu menyimpan dulu dan memakai mvn clean sebelum tes.

## Pengguna AI
- Alat yang digunakan : Claude
- Bagian yang dibantu AI : Saya meminta ai untuk menjelaskan apa yang saya kerjakan pada minggu 3, dan juga ai membantu saya membuat code dan juga membenarkan code.
- Prompt Utama : 
    a. Ini kenapa merah ya
    b. Kenapa ada garis merah?
    c. Cara ngecek error ini di mana ya
    d. Tolong bantu perbaiki yang error, pelan-pelan dan yang jelas.
- Yang saya ubah atau tolak dari saran AI, dan alasannya: Tidak ada yang saya tolak
- Di tugas Minggu 3, saya memperbaiki class Ruang, Laptop, dan AlatLab yang penuh error karena baris throw placeholder dari template belum dihapus, ditambah kurung kurawal yang salah. Saya juga memasang Maven agar tes bisa dijalankan. Sisa satu error di AlatLab.java yang tinggal diganti, disimpan, lalu dites ulang sampai BUILD SUCCESS.

                
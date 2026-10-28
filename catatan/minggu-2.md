# Catatan Minggu 02 (Struktur OOP: Class, Object, Encapsulation)

## Yang Saya Kerjakan
Minggu ini saya membuat cllas Aset pada file Aset.java,meliputi pembuatan field private(kode,nama,status,kondisi),konstruktor dengan validasi kode dan nama yang tidak boleh null atau kosong.Pengisian nilai awal status Tersedia dan Kondisi Baik,getter untuk seluruh field,serta setNama,setStatus,dan setKondisi supaya dapat di cek dengan tepat.

## Keputusan Desain
Keputusan yang diambil pada class Aset:seluruh field dibuat private agar data hanya diakses lewat getter dan setter.Kode dibuat final tanpa setter karena merupakan identitas yang tidak boleh berubah. 
konstruktor dan setter divalidasi dengann IllegalArgumentException agar objek selalu valid; status TERSEDIA dan kondisi BAIK diisi otomatis di konstruktor; serta kode tidak dinormalisasi dan disimpan apa adanya, yang dicatat sebagai asumsi.

## Kendala
Pada saat akan mengecek kode banyak sekali terjadi kekeliruan dan salah kode sehingga terjadi eror.Sehingga harus mengecek dan meneliti setiap baris di kodenya.

## Pengguna AI
- Alat yang digunakan : Claude
- Bagian yang dibantu AI : Saat memahami dan bedah soal untuk pemahaman dan Diskusi perancangan kelas aset baik status maupun kondisi.
- Promp Utama :
    a. bantu aku bedah pemahaman dari soal ini
    b. pada saat memperbaiki kode yang masih eror dan merah
    c.saat membantu mengecek dan memperbaiki kode tersebut.
- Yang saya ubah atau tolak dari saran AI, dan alasannya: (Tidak ada).
- Satu hal yang saya pahami sekarang : Dari tugas ini aku belajar bahwa class adalah cetakan dan object adalah hasil cetakannya. Data di dalam object sebaiknya dijaga dengan cara dibuat private, lalu diakses lewat getter dan setter yang punya pengecekan, supaya data yang salah tidak bisa masuk. 
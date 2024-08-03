# Minggu ke 3: Tulis kode lebih banyak lagi

## Selasa
- Slides: https://docs.google.com/presentation/d/1ZlNgZiPT2dHqUsdpQh2CdbbGvYmEeG8Br5SDIp371lY/edit?usp=sharing
- Kita akan mempelajari kode yang ditulis minggu lalu dan melihat berbagai cara untuk menyelesaikan masalah yang sama
- Anda akan bekerja dengan pod Anda untuk menerapkan perubahan spesifik yang dibahas di kelas
- FlexBox sangat mudah dipahami  - https://twitter.com/snowinglater/status/1615787738468610050
- Di mana kami memulai pada akhir hari Selasa - https://codepen.io/btopro/pen/OJqjoLb 
### Masalah: Saya memiliki gambar di halaman
- Saya perlu menambahkan tombol yang menambahkan gambar baru di sebelahnya saat saya menekan tombol tersebut
- Luangkan waktu 2 menit dan ketik jawaban berikut ke dalam Teams untuk menjawab tebakan Anda:
- Apa langkah pertama?
- Bagaimana cara membuat tombolnya?
- Kita hanya punya 1 gambar, bagaimana caranya kita bisa mendapatkan gambar lain di sana?
- https://cdn.pixabay.com/photo/2015/11/03/08/56/question-mark-1019820_1280.jpg

## Remediation
- Tukar codepens / audit codepen pod Anda. Cari yang berikut ini dan hal lain yang tidak Anda pahami
- Bersihkan CSS kartu Anda saat ini sehingga **kueri media berfungsi** - ini adalah hal umum yang tidak ada di PR 2.
- **Gunakan border dan background-color untuk membuat kartu Anda tampak seperti kartu secara visual** - kartu tersebut tidak boleh hanya berupa ruang kosong berwarna putih. Kartu tersebut harus tampak secara visual sebagai satu kartu, meskipun terdapat beberapa hal di dalamnya
buat pembungkus div di sekitar seluruh desain Anda, lalu yang lain sehingga Anda dapat meletakkan semua kartu di dalamnya sebagai wadah
```
<div class="wrapper">
..... your stuff to be a card
..... your stuff to be another card
</div>
```
- untuk membuat benda-benda "berada berdampingan" cari tahu cara menggunakan atribut displaydi CSS. Ini default untuk blockfor divdan sebagian besar tag tetapi mengubahnya menjadi flexberarti "membuat benda-benda lentur berdampingan di dalam tubuh saya"
- class="benda" BUKAN class = "benda"
- Hilangkan penggunaan id=”apapun” kecuali untuk kartu atau tombol
- Penggunaan padding dan margin yang berbasis 8 atau berbasis 16
- Hapus `<br> <center> <b> <body> <head>` dan tag lain yang dibahas yang tidak memiliki tujuan paralel lainnya
- Ganti semua gaya sebaris dengan kelas / pemilih CSS
- Ganti semua pemilih CSS khusus tag dengan kelas
- Buat “kartu” lain sehingga 2 hidup di layar berdampingan, lalu yang lain sehingga 3 hidup di layar.

## Rabu - mulai mengerjakan pekerjaan rumah sejauh menonton video dan menanggapi hal-hal di hax.psu

## Kamis

### Code by Numbers
Cara kerja kegiatan ini:
- Saya akan memberikan serangkaian langkah yang diperlukan
- Saya akan mulai melakukan aktivitas ini secara langsung di kelas dengan Anda mengikuti
- Saya akan mengajukan pertanyaan, terkadang berpura-pura bodoh, terkadang sah-sah saja sejauh menyangkut bagaimana kita menginginkan sesuatu bekerja
- Semakin cepat kita menyelesaikan tugas-tugas ini, semakin banyak tugas yang sudah kamu selesaikan. Oleh karena itu, semakin banyak tanggapan yang saya dapatkan terhadap pertanyaan, semakin besar kemungkinan kita akan menyelesaikan lebih banyak aktivitas.
- Saya akan berhenti saat saya melanjutkan melalui kode dengan angka dan berhenti untuk memberi Anda kesempatan untuk mengunyahnya
- Kami akan melakukan hal-hal yang dimaksud pada fork, clone, contoh, dll. **yang mencerminkan apa yang harus Anda lakukan pada kode proyek Anda sendiri**
- **Misalnya, jika di kelas kita mulai dengan repo kartu dan memasang tombol, setelah aktivitas langsung Anda akan memasang tombol itu di repo kartu ANDA**
- Di kelas berikutnya saya akan menggunakan contoh-contoh yang dihasilkan orang lain sebagai dasar untuk apa yang akan kita ulas bersama
- Siklus umpan balik ini akan terus berulang, biasanya setiap siklus mengakhiri siklusnya dengan tugas tambahan yang harus Anda lakukan di luar kelas + blog tentang topik tertentu

#### Kode Berdasarkan Angka - Aktivitas Bersama
- Kita akan mulai dari pena ini tentang profesor yang luar biasa: https://codepen.io/btopro/pen/PoLJXVj
- Rekaman dari kelas hari itu: https://www.youtube.com/watch?v=LGZHodz7dLo
- Garpukan pena dan ikuti / jawab pertanyaan dalam aktivitas di sepanjang jalan
- Mari tambahkan tombol yang ketika kita menekannya, akan menghasilkan salinan baru kartu kita
- Mari tambahkan tombol yang ketika kita menekannya, judul kartu akan berubah
- Mari kita tambahkan tombol yang ketika kita menekannya, gambar akan berubah menjadi gambar lain
- Mari tambahkan tombol yang ketika kita menekannya, warna latar belakang kartu berubah **melalui Kelas css**
- Mari tambahkan tombol yang jika kita menekannya, KARTU TERAKHIR akan terhapus. Logika tambahan untuk ditambahkan:
- Mari kita pastikan bahwa ketika kita akan menghapus kartu, kita tidak menghapus satu-satunya kartu kita
- Pastikan saat kita menambahkan kartu, kita tidak menambahkan lebih dari 10
- Mari kita pastikan ketika kita mengubah warna latar belakang, kita dapat mengaktifkan dan menonaktifkannya **untuk semua kartu di layar**

## Pekerjaan rumah
- Beberapa contoh yang dapat membantu Anda menerapkannya pada kartu Anda
  - https://codepen.io/btopro/pen/OJqjoLb  (pen from Tues)
  - https://codepen.io/btopro/pen/PoLJXVj (the pen from Thurs)
  - https://codepen.io/btopro/pen/QWzdMav (example of class toggling)
- Tambahkan hal-hal yang bertuliskan "Kode Berdasarkan Angka" di atas

## Simak berikut ini
- **LiveCode: New Idea and awesome Code Highlighting** https://www.youtube.com/watch?v=cM9KTKQ_4H0 -- lihat dari mana ide-ide baru muncul, tetapi juga banyak langkah melalui logika antara akses HTML dan JS / modifikasi status
- **Auto-pausing video with the visibilitychange document Event** https://www.youtube.com/watch?v=yORXfAb2Gvo -- pengantar singkat tentang umpan balik umum dalam mencari jenis peristiwa di MDN dan kemudian mengujinya

## Jawablah pertanyaan berikut ini
### Rekaman Video 1:
- Apa yang membuat ide itu layak?
- Apa masalah awal dengan penyorot kode Lit?
- Strategi apa yang dapat Anda lakukan untuk melakukan refaktor menuju kode yang lebih baik? Strategi apa/berapa kali iterasi yang saya lalui untuk mendapatkan "kode yang lebih baik"? - Apa yang membuat kode ini lebih baik?
### Video 2:
- Peristiwa aneh apa yang saya terapkan untuk memecahkan masalah UX?
- Apa perbedaan antara dokumen dan jendela dalam javascript? Apa itu _globalThis_? Temukan keduanya di halaman Mozilla Developer Network untuk mengetahui apa saja keduanya dan apa yang dapat Anda lakukan dengannya.
- Temukan 5 peristiwa yang dapat dihasilkan melalui MDN Web Docs melalui input pengguna. Tautan ke contoh

## Penyerahan Pekerjaan Rumah
- Buat postingan blog HAX.PSU yang berisi jawaban untuk pertanyaan di atas setelah menonton videonya
- Selesaikan pekerjaan "kode berdasarkan angka" yang dimulai di kelas bersama-sama **tetapi diterapkan pada kartu yang Anda buat sebelumnya** dan berikan tautan di posting blog Anda
- jatuhkan tautan ke postingan Anda ke kanvas HW3

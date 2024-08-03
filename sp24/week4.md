# Minggu ke 4 - Yang memiliki perkembangan nyata
This week we'll start looking at how our code fits (or doesn't) into the modern JS ecosystem. What we've made so far is old school, vanilla, simple. Now we'll start looking into how moderen JS is shipped and worked with as well as provide review and revision to the work that's been done.

## Selasa
## CATATAN KEBIJAKAN
- Asisten memberikan umpan balik tentang benar dan salahnya
- Jika Anda kehilangan poin, biasanya karena kekurangan hal yang diminta / memenuhi semua persyaratan
- Jam kantor yang diberi insentif: jam kantor pada hari Senin dan jika seorang siswa menyerahkan tugasnya tepat waktu dan datang ke jam kantor pada hari Senin karena mereka merasa tugasnya kurang dan menyerahkannya lagi setelah bertemu dengan salah satu dari kami, kami tidak akan mengurangi poin keterlambatan.

## Kode kritik dari PR 3 - 30 menit
- Periksa suasana hati; buka Teams dan saluran Umum. Bagaimana perasaan Anda tentang Minggu ke-3 dan di bagian mana Anda merasa paling cocok dengan emoji ini?
- Wa Group
- melihat beberapa contoh yang diajukan untuk dikritik:
  - https://codepen.io/Alan-Manuel-the-sasster/pen/rNRwKwW
  - https://codepen.io/emirahanna/pen/rNRpygq
  - https://codepen.io/RileySpitznas/pen/NWJgbKm
  - https://codepen.io/Kermitopalis/pen/qBvpRjX
  - https://codepen.io/ssambender/pen/eYXRKPW

## Perbaikan dan peningkatan yang perlu diperhatikan
- Berikut ini beberapa hal umum yang dapat diterapkan selama kegiatan pertama
1. pastikan hal seperti `class="whatever"` is NOT `class = "whatever"` sspasi pada atribut tidak diperbolehkan
2. jika Anda menguji untuk "status" gaya seperti misalnya `if (thing.style.display == "block") { } ` ubah ini untuk menguji apakah ada kelas ATAU atribut. Jika kelas tersebut ada `if (thing.classList.contains('namedclass')) {` maka aktifkan dan nonaktifkan kelas tersebut.
3. Pastikan Anda mengomentari fungsi Anda untuk memahami apa fungsinya. Umumnya saya mengomentari komentar saya sendiri yang terdapat pada setiap blok kode "baru"; seperti hal yang harus saya pikirkan/pahami atau yang mungkin tampak aneh dari konvensi umum saya (karena Anda masih di awal, ini seharusnya sering terjadi sebagai hasilnya)
4. PASTIKAN SEMUA TAG YANG TERBUKA, TERTUTUP DI TEMPAT YANG ANDA HARAPKAN
5. hilangkan ketergantungan pada `id="whatever"` dan kemudian `querySelector("#whatever")` tetapi TERUTAMA `document.getElementById('whatever')` . Refaktor ini menjadi `.whatever` and `class="whatever"` and `querySelector('.whatever')` atau menanggung amarah arsitektur komponen (dan a11y, dan ejekan) yang terus berlanjut!!
6. Saat menggunakan `@media` queries, verifikasi bahwa Anda menggunakan pemilih yang sama seperti yang Anda gunakan di bagian dokumen lainnya

## Slide deck untuk hari ini

- Ekosistem/lanskap JS:: https://docs.google.com/presentation/d/1XC6OuYVe3fOdGmpZ_Q9aGXOPJKjj5VbfR3vMvCUJBdk/edit?usp=sharing

### Mari kita pahami dan intip bagaimana sesuatu dibangun
- https://hax.psu.edu/ - Open it up and let's look around a modern repo structure
- https://github.com/elmsln/hax-psu
  - Aktivitas; lakukan semua hal berikut, ikuti petunjuk saya saat mengerjakannya. Jika Anda mengalami kendala, tanyakan kepada orang di sebelah Anda/di sekitar Anda. Jika mereka tidak tahu, tanyakan kepada asisten/saya.
  - Fork kode ini di website github
  - Gunakan github desktop / commandline untuk menarik salinan kode secara lokal
  - Saya cenderung menyimpan SEMUA pekerjaan pengembangan di sistem file saya seperti
    -  `~/Documents/git/{USERNAME}/{REPONAME}` - tidak peduli struktur apa yang Anda gunakan, tetapi buatlah logis / suatu tempat yang Anda tahu di mana mengaksesnya
    - Buka VS Code; Menu File -> Buka Folder.. dan pilih repo yang Anda tarik ke bawah
    - Mari kita dapatkan beberapa plugin: Klik Ekstensi (blok penyusun pada menu sebelah kiri) lalu cari `lit-html` and `lit-plugin` and `HTML CSS Support`
    - Open a terminal (VS Code -> Terminal menu -> New terminal)
      - Secara pribadi saya biasanya membuka terminal di luar VSCode, tetapi biasanya ini lebih merupakan preferensi daripada keharusan. Beberapa lingkungan Windows bisa jadi aneh dan mengharuskan ini, oleh karena itu saya sebutkan di sini
  - ketik `pwd` ini akan mencantumkan dimana Anda saat ini berada di sistem file
  - ketik `node -v` untuk memverifikasi bahwa ia memiliki akses ke node (seharusnya demikian jika Anda menginstalnya sebelumnya dari minggu ke-1)
  - ketik `ls -las` ini akan mencantumkan semua yang ada di folder ( dirini adalah tampilan sederhana dari info ini)
  - type `npm install` selama Anda melihat package.jsondi langkah sebelumnya - **Ini adalah cara Anda berinteraksi dengan SEMUA REPO KODE JAVASCRIPT MODERN**
  - type `npm run` yang akan mencantumkan perintah yang dapat Anda jalankan. _Hampir setiap proyek_ merespons `npm start` or `npm run start`
  - Ini akan membuka jendela browser. Atur tampilan Anda sehingga keduanya berdampingan
- Mari kita mulai menggali kodenya
- Saya akan menelusuri kode dan apa yang telah saya bangun baru-baru ini, menerapkan konsep dari kelas tetapi pada skala yang lebih tinggi
- Ada bug di ponsel, mari kita atur lingkungan yang optimal untuk mendiagnosis dan mengatasinya: https://github.com/elmsln/issues/issues/1903
- Jika Anda menguasai hal-hal kecil, sintaksis, struktur kecil, meminimalkan CSS, HTML, dan JS yang ditulis untuk menyelesaikan tugas, maka berpikir dalam struktur yang lebih besar dan lebih besar akan lebih alami. Ini adalah pola yang besar.
- 
### Bantuan tambahan
Jika Anda memerlukan bantuan tambahan setelah menontonnya, berikut beberapa langkah selanjutnya
- Pelajari dasar-dasar JS di sini https://www.w3schools.com/js/default.asp
- CSS fundamentals here https://www.w3schools.com/css/default.asp
- Dasar-dasar HTML di sini  https://www.w3schools.com/html/default.asp
- Datanglah ke kantor TA pada jam kerja, banyak sekali jam kerjanya, itulah tugas mereka!
- DM saya atau TA dengan pertanyaan spesifik yang Anda miliki tentang cara melakukan hal-hal tertentu dan kami dengan senang hati membantu

# Kamis (kita lihat saja bagaimana Selasa berjalan dan menyesuaikannya dari sana)
Sekarang setelah kita memiliki beberapa alur kerja dan proses, mari kita mulai melihat komponen web dan membangunnya dari nol. Ringkasan: Apa itu komponen web? [Slide Komponen Web](https://docs.google.com/presentation/d/18XW95fe_-mvOibTUvcCXh8OlH6xELCewAKlt4SJNc7g/edit?usp=sharing)
## Kode dengan angka
- Ambil template kartu ini: [Polaris Chip](https://github.com/btopro/polaris-chip) templat untuk Anda sendiri
- dapatkan kode ini dikloning ke komputer Anda
- ikuti di kelas

### Aktivitas Diskusi 10 menit
- Properti apa yang dapat kita tambahkan untuk mendukung tautan ini?
- Tipe data apa ini?
- Apa saja langkah yang diperlukan untuk melakukan ini? Apa saja yang perlu diperhitungkan/diubah dalam kode?
- Kalau kita ingin membuat status 'aktif' yang dimaksudkan untuk 'melayang', fokus dan menarik perhatian secara default, bagaimana kita melakukannya?
- Posting di Discord properti apa saja yang Anda hasilkan?

### Activity 10 min
- Aktivitas Pod. Lihatlah kartu-kartu Anda di Pod. Properti apa yang dapat Anda tambahkan untuk membuat kartu Anda fleksibel?
- Apakah kartu Anda memiliki kemampuan 'aktif' atau 'status' visual?
- Apakah ada area yang sifatnya dapat berupa HTML?

## Pekerjaan rumah

Now it's your turn:

- Terapkan CSS / HTML kartu Anda ke elemen my-card
- Abaikan JS yang mengubah kartu untuk saat ini; kami hanya mencoba untuk menampilkan kartu kami secara visual di sana
- Cobalah untuk menambahkan properti Anda ke dalam elemen sehingga Anda dapat mengubah variabel untuk membuat contoh kartu Anda
- Anda harus memiliki setidaknya 2-4 properti yang dapat saya pikirkan sekilas
- Buat 5 implementasi ini di area demo / index.html (artinya 5 implementasi berbeda dalam `<my-card>` penggunaan atribut)
- Jalankan tutorial lit - https://lit.dev/tutorials/intro-to-lit/ untuk membantu MEMASTIKANNYA MENGGUNAKAN JS DAN BUKAN TS

### Bonus 1pt
Melompat ke depan seminggu atau lebih, cobalah untuk menghubungkan JS Anda sehingga Anda dapat mengubah hal-hal pada kartu melalui tombol Anda. Petunjuk: tombol dan js ada dalam demo. Anda perlu mengubah cakupan panggilan dan beberapa aspek lainnya untuk mengubah data, menambahkan, menghitung jumlahnya, dll.

## Penyerahan
- Posting HAX.psu yang tertaut ke repo github yang Anda buat
- Saat mengerjakan tutorial, kendala apa yang Anda hadapi?
  - Saat membaca dek / tutorial / googling, apa yang tidak masuk akal?
  - Sama, tetapi apa yang MEMANG masuk akal? Apakah ini pendekatan yang lebih baik untuk pengkodean dalam 'lingkup global' ala **codepen**, atau apakah cakupan ini membuatnya lebih rumit?
    - Jika lebih rumit, apa yang membuatnya lebih sulit?
    - Jika pendekatannya unggul, mengapa Anda merasa ini lebih mudah daripada cara global berbasis **codepen**?
- Idealnya dipublikasikan di vercel; kalau kita sampai di kelas/akun kamu berfungsi di sana, keren; kalau tidak, tidak apa-apa

# Week 3: Code pen some moe

## Tuesday
- Slides: https://docs.google.com/presentation/d/1ZlNgZiPT2dHqUsdpQh2CdbbGvYmEeG8Br5SDIp371lY/edit?usp=sharing
- Kita akan mempelajari kode yang ditulis minggu lalu dan melihat berbagai cara untuk menyelesaikan masalah yang sama
- Anda akan bekerja dengan pod Anda untuk menerapkan perubahan spesifik yang dibahas di kelas
- FlexBox really easy to understand - https://twitter.com/snowinglater/status/1615787738468610050
- Where we got started on end of day Tues - https://codepen.io/btopro/pen/OJqjoLb 
Issue: I have an image on the page
- I need to add a button that adds a new image next to it when I hit the button
- Take 2 minutes and type up the following answers into Teams as to your guess:
- What’s the first step?
- How do I make the button?
- Kita cuma punya 1 gambar, bagaimana caranya kita bisa mendapatkan gambar lain di sana?
- https://cdn.pixabay.com/photo/2015/11/03/08/56/question-mark-1019820_1280.jpg

## Remediation
- Swap codepens / audit the codepen of your pod. Look for the following and anything else you don’t understand
- Clean up your current card CSS so that **media queries work** - this was a common thing that was missing in HW2.
- **Use border and background-color to visually make your card look like a card** - it shouldn't just be a blank white space. It should visually appear as a single card, even if it has multiple things inside of it
- create a wrapper div around your entire design, then another so you can put all the cards in it as a container
```
<div class="wrapper">
..... your stuff to be a card
..... your stuff to be another card
</div>
```
- in order to get things "to sit next to each other" look up how to use the `display` attribute in `CSS`. This defaults to `block` for `div` and most tags but changing it to `flex` means "make things flex side by side inside of me"
- class="tihng" NOT class   =   "thing"
- Drop usage of id=”whatever” unless for card or button
- Usage of padding and margin that’s either base 8 or base 16
- Remove `<br> <center> <b> <body> <head>` and any other tags discussed that have no purpose of other parallels
- Replace all inline styles with CSS class / selector
- Replace all tag specific CSS selectors with classes
- Make another “card” so that 2 live on the screen side by side, then another so that 3 do

## Wed - start into the homework as far as watching videos and responding to things on hax.psu

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

## Homework
- Some examples that can help you apply to your card
  - https://codepen.io/btopro/pen/OJqjoLb  (pen from Tues)
  - https://codepen.io/btopro/pen/PoLJXVj (the pen from Thurs)
  - https://codepen.io/btopro/pen/QWzdMav (example of class toggling)
- Add things to yours that say "Code By The Numbers" above

## Watch the following
- https://www.youtube.com/watch?v=cM9KTKQ_4H0 -- see where new ideas come from, but also lots of stepping through logic between HTML and JS accessing / state modification
- https://www.youtube.com/watch?v=yORXfAb2Gvo -- a short primer on the general feedback loop of searching for a type of event on MDN and then testing it

## Answer these questions
### Rekaman Video 1:
- Apa yang membuat ide itu layak?
- Apa masalah awal dengan penyorot kode Lit?
- Strategi apa yang dapat Anda lakukan untuk melakukan refaktor menuju kode yang lebih baik? Strategi apa/berapa kali iterasi yang saya lalui untuk mendapatkan "kode yang lebih baik"? - Apa yang membuat kode ini lebih baik?
### Video 2:
- Peristiwa aneh apa yang saya terapkan untuk memecahkan masalah UX?
- Apa perbedaan antara dokumen dan jendela dalam javascript? Apa itu globalThis? Temukan keduanya di halaman Mozilla Developer Network untuk mengetahui apa saja keduanya dan apa yang dapat Anda lakukan dengannya.
- Temukan 5 peristiwa yang dapat dihasilkan melalui MDN Web Docs melalui input pengguna. Tautan ke contoh

## Penyerahan Pekerjaan Rumah
- Buat postingan blog HAX.PSU yang berisi jawaban untuk pertanyaan di atas setelah menonton videonya
- Selesaikan pekerjaan "kode berdasarkan angka" yang dimulai di kelas bersama-sama **tetapi diterapkan pada kartu yang Anda buat sebelumnya** dan berikan tautan di posting blog Anda
- jatuhkan tautan ke postingan Anda ke kanvas HW3

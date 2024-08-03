# Masalah umum

Ini adalah daftar masalah umum dan solusi umum. Sebelum mengangkat tangan atau mengatakan Anda buntu, pastikan Anda telah membaca daftar ini karena kemungkinan besar saya akan meminta Anda untuk membahasnya.

## Saya melakukan X dan itu tidak berhasil

### Terminal / command line
- cari sebelum perintah yang Anda ketik, google kesalahannya. biasanya berwarna merah, atau semacam "apa pun yang tidak terdefinisi"
- perintah terminal tidak dimulai dengan a $dan Anda mungkin telah menyalin dan menempel dengan salah
- pastikan Anda berada di direktori yang benar saat menjalankan perintah

#### Ini mengatakan "apapun" bukanlah sebuah perintah
setiap repo yang memilikinya `package.json` perlu diinstal. Umpan baliknya SELALU:
1. git clone / unduh benda itu
2. buka proyek di jendela terminal dan jalankan npm install untuk menginstal dependensi
3. membaca package.json Anda dapat melihat perintah yang tersedia di bawah scripts meskipun `npm start` cukup umum diikuti oleh `npm run dev`
4. ANDA HARUS BERADA DI DIREKTORI YANG SAMA DENGAN FILE `package.json` ITU UNTUK MENJALANKAN PERINTAH

#### Common commands
- `cd` ubah direktori `cd whatever` pindah ke directori `whatever` 
- `cd ../..` pindah kembali 2 folder `cd ..` back one
- `ls -las` lists things in a well printed way in the current directory
- `pwd` menunjukkan jalur ke direktori kerja saat ini
- `git pull origin master` (atau git pull origin main) akan mendapatkan komit dan kode yang diperbarui dari repo git

### Browser / kode Anda yang sedang berjalan

Kosong / gagal / tidak melakukan apa yang Anda harapkan
- Lihat terminal, apakah ada kesalahan/peringatan?
- Lihat di VS Code, apakah ada yang berwarna merah di tepi kanan? Jika ada, gulir untuk melihat kode tersebut dan arahkan kursor untuk petunjuk tentang sintaksis atau dependensi yang salah.
- Buka browser, klik kanan dan tekan _Inspect_. Di tab yang terbuka, lihat untuk _Console_ melihat apakah ada pesan kesalahan

### Kesalahan umum HTML
- atribut HARUS seperti ini  `<p class="whatever">`. beberapa sistem (seperti codepen) akan mengizinkan  `<p CLASS = "STUFF">` or `<P class=stuff>` tetapi ini tidak benar dan dapat menyebabkan masalah.
- Nama tag selalu `<`  dalam huruf kecil, spasi, nama atribut, =", lalu nilai dan kemudian ". Tag harus selalu diakhiri dengan `>` dan untuk menjadi lengkap akan memiliki pencocokan `</tagname>`atau `</p>`.
- VSCode terkadang akan mengidentifikasi tag terbuka tanpa tag penutup
- 
### Kesalahan umum CSS
- `#thing` akan menargetkan `<p id="thing">`
- `.thing` akan menargetkan `<p class="thing">`
- `.thing .nesting .here` is `<p class="thing"><div class="nesting"><a class="here">`
- `.thing.nesting.here` without spaces, implies `<p class="thing nesting here">` because you can stack classes / selectors together
- ALL css attributes MUST have `;` at the end of them. JS is forgiving at times but CSS is not. for example `p.orange { color: orange }` will break
- `<p class="orange">` with a `p.orange { color: orange;}` will work
- Try to target class names and not tag names (generally)
- Try to avoid using `id="whatever"`. While not "wrong", over-use of this approach can cause accessibility errors in certain situations and `<section class="whatever">` is just as specific if you never use "whatever" elsewhere
- you can sorta "make up" selectors when we get into web components via attributes. This allows you to somewhat abuse the specification of HTML for CSS purposes and is a good thing but you won't see it a lot outside of web components
  - example: `<my-tag cool>` could have a selector internally of `:host([cool]) { background-color: green;}`
  - more universal / vanillaJS / any context example: `<div data-cool="data-cool">` w/ a global selector of `div[data-cool] { background-color: green; }`
- CSS scoping when we get into web components, is that CSS does not cascade when you see "shadow-root" in the browser inspector. This is a feature, not a bug, but frustrating at first for sure!

### JS Common mistakes
- Kita akan menggunakan javascript modular, yang berarti "perkakas" atau perkakas pengembangan lokal, benar-benar membangun dan membuat kode berfungsi saat Anda memeriksanya.
- Akibatnya ketika Anda mereferensikan kode lain, kode tersebut seharusnya seperti `import "@whatever/library/thing.js";` and NOT `import "../../../../node_modules/@whatever/library/thing.js"` loop umpan balik JS saat menggunakan NPM
- temukan aset di npm
- `npm install --save @what/ever`
- `npm run start` (restart / reload your development environment)
- import the code into your code like `import "@what/ever/thing.js"`
- now, if it's another webcomponent then you'll be able to use the `<what-ever>` tag

# Biasakan melakukan hal ini setiap waktu.
Ini secara harfiah merupakan siklus umpan balik dari pekerjaan dan cara untuk menyelesaikan 99% masalah. Jika Anda membenci ini, Anda mungkin akan membenci pengembangan. Jika ini masuk akal, mudah-mudahan Anda baru saja menemukan gairah Anda.

# Video of how to get started / OS level explainer
- https://www.youtube.com/watch?v=cwTswuFkMH4

# Lit life cycle activity
- https://lit.dev/tutorials/ make sure you do all the tutorials

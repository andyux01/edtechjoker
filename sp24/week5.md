# Minggu ke-5 - Lebih banyak dengan komponen Web
Seperti yang diharapkan, hasil dari pekerjaan rumah sangat beragam. Ini bukan subjek yang mudah, dan terkadang kita harus sedikit mengembangkan sesuatu untuk melihat apa yang dapat kita ingat. Minggu ini kita mulai berpikir seperti penulis spesifikasi HTML. Ini adalah pekerjaan pemikiran yang mendalam dan kita beruntung dapat membangun di atas abstraksi, tetapi mari kita mulai proses yang mereka lalui untuk memikirkan atribut dan pertimbangan desain tag primitif HTML (p, img, a, table, dll.) dan menggunakan proses itu untuk membangun kartu kita sendiri sehingga dapat digunakan kembali seperti tag asli tetapi lebih tangguh!

## Selasa
- Mari kita tinjau masalah yang dialami orang saat melakukan hal itu
- Kritisi:
  - https://github.com/ssambender/polaris-chip
  - https://github.com/emirahanna/polaris-chip
  - https://github.com/infodigger33/polaris-chip - Yang ini mari kita fork / klon dan gali bersama

### Aktivitas: Bicaralah dengan orang-orang di pod Anda 20 menit
- Apakah ada yang berhasil membuat kartunya berfungsi? Jika ada, biarkan orang tersebut menjelaskan bagaimana cara mereka membuat kartunya berfungsi.
- Jika ada yang benar-benar hilang dan kartunya tidak berfungsi, debug. Apa yang salah? Di mana mereka terjebak?
- Saya melihat banyak komponen, tetapi tidak semuanya dapat digunakan kembali. Temukan 5 masalah (di antara pod Anda, total 5, tidak sama terus-menerus) yang Anda lihat saat meninjau kode satu sama lain.
- Apa yang TIDAK dapat digunakan kembali menurut definisi berikut:
> Seseorang secara acak menelusuri internet untuk sebuah Kartu yang berisi detail Anda. Apakah mereka dapat mengunduhnya dan menulis `<my-card title="Fresh Prince" fancy source="https://encrypted-tbn1.gstatic.com/images?q=tbn:ANd9GcRPgSRgEYJ3lY8Ky8wNqfoJqWe2U2VMe-RIKbO_0HSXGj5sHA-_"></my-card>` serta memperoleh kartu yang terlihat 'mewah' dengan judul pangeran segar tertulis di atasnya dan gambar saat-saat yang lebih baik?

Jika seseorang mendapatkan kartu Anda dan tidak dapat mengganti judul/gambar di dalamnya dengan miliknya sendiri, kartu tersebut tidak dapat digunakan kembali. Bekerjasamalah dengan kelompok Anda agar kartu milik semua orang dapat digunakan kembali. Tambahkan kartu ini ke demo Anda untuk memastikan bahwa Anda memiliki dukungan untuk gambar berukuran besar!

Bila Anda merasa yakin bahwa setiap orang dalam pod Anda mempunyai kartu yang berfungsi dan dapat digunakan kembali, posting tautannya di saluran tim.Jika seseorang mendapatkan kartu Anda dan tidak dapat mengganti judul/gambar di dalamnya dengan miliknya sendiri, kartu tersebut tidak dapat digunakan kembali. Bekerjasamalah dengan kelompok Anda agar kartu milik semua orang dapat digunakan kembali. Tambahkan kartu ini ke demo Anda untuk memastikan bahwa Anda memiliki dukungan untuk gambar berukuran besar!

Bila Anda merasa yakin bahwa setiap orang dalam pod Anda mempunyai kartu yang berfungsi dan dapat digunakan kembali, posting tautannya di saluran tim.

## Rabu
- Jika kartu Anda tidak berfungsi/Anda mengalami masalah, bicaralah dengan LA/cari bantuan
- Untuk hari Kamis, bersihkan kartu Anda dan coba terapkan tombol berbasis JS yang telah diubah cakupannya untuk menghubungkan fungsionalitas pada contoh yang kita lihat di kelas.
- Ini akan menjadi pekerjaan rumah selain apa yang kita lakukan pada hari Kamis.

## Kamis
- Demo langsung / ikuti dengan menambahkan hal-hal di bawah ini
- Rekaman kelas di bawah ini: https://www.youtube.com/watch?v=hLDrFa45wJQ

## Let's get fancy with CSS selectors
- Adding a 'reflected' variable to our element. Reflected variables allow you to change the properties of your card and have the CSS change as a result
- live code demo adding a reflected variable in CSS so that `:host([fancy]) { background-color: golden; }` works
- `fancy: { type: Boolean, reflect: true }`
- Follow along and add support for `fancy` so that we can add fancy which changes the background color / borders / drop shadow of our card
- https://developer.mozilla.org/en-US/docs/Web/CSS/box-shadow
```js

constructor() {
  super();
  this.fancy = false;
}

static get properties() {
  return {
    fancy: { type: Boolean, reflect: true }
  }
}
```

```css
:host([fancy]) {
display: block;
  background-color: pink;
  border: 2px solid fuchsia;
  box-shadow: 10px 5px 5px red;
}
```

## Let's support flexible HTML areas in web components
- Some of you had properties that were "description" or really long blobs of text to put on the card.
- Let's try an experiment. In either your title or 'description' property try to make some of the text bold
- What happens? Why did this happen? Throw a screen shot in Teams of what happens when you tried to apply this
- `<slot>` to the rescue, but let's put it in 2 new tags that can work together `<details>` and `<summary>`
  - https://developer.mozilla.org/en-US/docs/Web/HTML/Element/details - allows you to collapse an area
  - https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Slot (the docs on slot are confusing but including just so you see them)
 
```html
<details ?open="${this.fancy}">
  <summary>Description</summary>
  <div>
    <slot>${this.description}</slot>
  </div>
</details>
```

## Let's make it so when fancy changes, our details area opens as well
- A few of you have asked "Is this just a design element? Where does the JS go?" or some version of "Should I add methods to my card?"
- This is an example of when it makes sense to do something like that -- responding to events and actions in the element itself
- Let's add a method called `openChanged(e)` This will flip `fancy` between `true` and `false` based on the Details area opening and closing
- https://developer.mozilla.org/en-US/docs/Web/HTML/Element/details#events -- details has a `toggle` event
- **Question**: If the user is clicking this to open and close it, why are we not listening for the "click" event?

```html
<!-- put this in your render method where you had details -->
  <details ?open="${this.fancy}" @toggle="${this.openChanged}">
```
Note that the `@` is somethign lit specific. You won't be able to do this in `index.html` and is a good example of "syntactical sugar", meaning something that is NOT vanilla.
Here is the equivallent to what this is doing in case you were wondering
```js
this.shadowRoot.querySelector('details').addEventListener('toggle', this.openChanged.bind(this));
```
We won't do it that way but so you are aware; think of it like the jquery `$("details")` selector syntax but JUST for events to make it easier to read.

This is the JS method I'll be adding to my `class`
```js
// put this anywhere on the MyCard class; just above render() is probably good
  openChanged(e) {
    console.log(e.newState);
    if (e.newState === "open") {
      this.fancy = true;
    }
    else {
      this.fancy = false;
    }
  }
```

# IF THIS DOESNT WORK FOR YOU TRY THIS ONE
Welcome to browser differences. If you use safair the 1st one will never work. If you use the latest version of Chrome it will work, if you use the previous version of chrome it won't. I had no intention of creating htis problem and yet here we are... learning exactly the issue w/ an evolving spec.
```js
// put this anywhere on the MyCard class; just above render() is probably good
openChanged(e) {
  console.log(e);
  if (e.target.getAttribute('open') !== null) {
    this.fancy = true;
  }
  else {
    this.fancy = false;
  }
}
```

## Additional Design considerations
- Get your card to have height / sizing requirements so that long title don't bork the design
- Same thing but with images -- https://developer.mozilla.org/en-US/docs/Web/CSS/aspect-ratio helpful article / attribute for this
- Same thing but with the description area

```css
 details summary {
    text-align: left;
    font-size: 20px;
    padding: 8px 0;
  }

  details[open] summary {
    font-weight: bold;
  }
  
  details div {
    border: 2px solid black;
    text-align: left;
    padding: 8px;
    height: 70px;
    overflow: auto;
  }
```

## Homework
- Get your card to have a `fancy` attribute like from class that changes the styling
- Add the details and summary so that when you toggle details it also toggle fancy
- Ensure that when you change fancy (or set it ahead of time) that it ensures we collapse or expand to match
- Add support for `<slot>` and get your description to load that way instead of via property (unless you want to support both like in the example)
- Get you images / titles allowing for the cards to look relatively uniform
- Get the JS working for the buttons in `index.html` so that the operations work
- Turn into Canvas a link to your github repo where this code is located

## Note
This largely ends our work with the `card`. We will publish them to NPM and use them in a new repo to complete the end to end workflow of a developer in this space.

After that we will work on a new element. Each time we work on a new project there will be less training wheels but this feedback loop is the same over and over again in the industry:
- Get requirements
- Make a design (step we are skipping a bit to learn)
- Make a new element / boilerplate repo
- Start to translate the design to the element
- push up to github
- Deploy demo to a URL (vercel for us / many others exist)
- automated testing (skipping this to learn)
- publish to npm / leverage in the production project


# Belajar Docsify

Website: [https://docsify.js.org](https://docsify.js.org)
Github: [Github](https://github.com/docsifyjs/docsify)

---

## Sebelum Belajar

> Saya asumsikan bahwa kamu sudah tau tentang:
>
> - [x] Terminal untuk pengguna linux/mac
> - [x] Command Prompt bagi pengguna windows
> - [x] HTML minimal tentang h1, h2 ..

---

# Getting Started

---

## Cara Install Global

```
npm i docsify-cli -g
```

## Membuat Project

```
docsify init ./nama-project
docsify init ./blog
```

docsify akan membuatkan sebuah folder yang bernama `blog` yang berisi 3 file:

- `index.html`
- `README.md`
- `.nojekyll`

**index.html\***

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Document</title>
    <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" />
    <meta name="description" content="Description" />
    <meta
      name="viewport"
      content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0"
    />
    <link
      rel="stylesheet"
      href="//cdn.jsdelivr.net/npm/docsify/lib/themes/vue.css"
    />
  </head>
  <body>
    <div id="app"></div>
    <script>
      window.$docsify = {
        name: "",
        repo: "",
      };
    </script>
    <script src="//cdn.jsdelivr.net/npm/docsify/lib/docsify.min.js"></script>
  </body>
</html>
```

**README.md**

Secara default file `README.md` adalah tempat untuk menulis kontent dan secara otomatis docsify akan membuatkan daftar di sidebarnya (sebelah kiri) sesuai dengan tanda `#`.

- `#` berarti h1 di html.
- `##` mirip h2 dan seterusnya.

**.nojekyll**
.nojekyll adalah file kosong secara defaultnya.

## Menjalankan Project

```
docsify serve blog
```

?> Pastikan mengetikkan perintah di atas pada di luar folder `blog`, karena saya membuat projectnya bernama `blog`.

Ilustrasinya:

```
--jalankan docsify serve blog
--blog
      --index.html
      --README.md
      --.nojekyll
```

---

# Customization

## Mengganti Default Kontent

?> Konten yang saya maksud di sini adalah tulisan yang berada di sebelah kanan (bukan sidebar).

Secara default docsify akan menampilkan konten dari `README.md`.
Lalu bagaimana caranya mengubahnya?
kita hanya perlu mengedit file index.html di bagian window.\$docsify

```js
window.$docsify = {
  // Change to /home.md
  homepage: "home.md",
  // Or use the readme in your repo
  homepage:
    "https://raw.githubusercontent.com/docsifyjs/docsify/master/README.md",
};
```

Ada 2 cara untuk mengganti `README.md` sebagai nilai default kontentnya:

1. Mengganti dengan file `home.md`.
2. Mengganti dengan file `.md` yang berada di github kamu.

## Custom Sidebar

> Goals:
>
> - [x] Membuat Daftar Isi sendiri di sebelah kiri (Sidebar).

Ketika kamu ingin membuat daftar isi yang ada di sebalah kiri (sidebar), caranya cukup mudah dengan:

- Mengganti `README.md` default dengan `_sidebar` yang berisi daftar isi kamu.

Langkah 1: Membuat custom sidebar

- Buat file `_sidebar.md`
- letakan di folder utama sejajar dengan file index.html

misal: `_sidebar.md`

Langkah 2: Membuat daftar isinya

Jika ingin membuat judul tanpa link

```markdown
- Judul 1
  - Sub Judul 1
- Judul 2
  - Sub Judul 2
```

Jika ingin membuat daftar isi dan link

```markdown
- [Judul 1](/)
  - [Sub Judul ](/judul/judul1.md)
- [Judul 2](/judul/judul2.md)
```

- `Judul 1` saya arahkan linknya ke home `/`
- kemudian `Subjudul 2` saya arahkan linknya ke alamat `/judul/subjudul1.md` di mana file `subjudul1.md` berada.

Hasilnya:

```
Judul 1
  - Sub Judul 1
Judul 2
  - Sub Judul 2
```

---

# Fitur

## Warning

Cara Membuatnya

```
!> Peringatan
```

Hasilnya

!> Peringatan

## Marked

Cara Membuatnya

```
?> Catatan ini penting
```

Hasilnya

?> Catatan ini penting

# Advanced

## Loading Dialog

```html
..
<body>
  <div data-app id="main">Please wait...</div>
  <script>
    window.$docsify = {
      el: "#main",
    };
  </script>
</body>
```

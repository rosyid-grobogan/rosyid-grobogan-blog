# Belajar Docsify

Website: [https://docsify.js.org](https://docsify.js.org)
Github: [Github](https://github.com/docsifyjs/docsify)

# Getting Started

## Cara Install Global

```
npm i docsify-cli -g
```

## Membuat Project

```
docsify init ./nama-project
```

maka akan dibuatkan 3 file:

- `index.html`
- `README.md`
- `.nojekyll`

**README.md**

Secara default file README.md adalah tempat buat nulis dokumentasi dan secara otomatis akan dibuatkan daftar ininya sesuai dengan tanda `#`

- `#` berarti judul (mirip h1)
- `##` mirip h2 dan seterusnya

## Menjalankan Project

```
docsify serve docs
```

# Customization

## Custom Sidebar

Membuat custom sidebar

- Buat file `_sidebar.md`
- letakan di folder utama sejajar dengan file index.html

misal: `_sidebar.md`

Membuat daftar isi tanpa link

```markdown
- Introduction - Quick start
```

Membuat daftar isi dan link

```markdown
- [Introduction](/) - [Quick start](/introduction/quick-start.md)
```

- introduction link ke home `/`
- quick start link ke artikel yang berada di folder `/introduction/quick-start.md`

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

# Element Functions

* [English Version](./element-en.md)

## Pendahuluan

Modul ini menyediakan kumpulan fungsi JavaScript untuk mempermudah manipulasi DOM, penanganan event, dan pengelolaan konten dinamis.

## Instalasi

Cukup sertakan file JavaScript dalam proyek Anda atau impor fungsi-fungsinya sebagai modul ES:

```javascript
import { onClick, onClicks, onChange, onChanges, onInput, onInputs, container, setValue, getValue, renderHTML, addJS, addCSS } from 'https://cdn.jsdelivr.net/gh/jscroot/lib@0.2.6/element.js';
```

## Fungsi dan Penggunaan

### Pemilihan Elemen DOM

#### `container(id)`

Mengambil elemen berdasarkan ID.

```javascript
const element = container('myElement');
```

### Penanganan Event

#### `onClick(id, actionFunction)`

Menambahkan event klik ke elemen berdasarkan ID.

**Contoh tanpa argumen:**

```javascript
function handleClick() {
    console.log("Tombol diklik!");
}

onClick('myButton', handleClick);
```

**Contoh dengan argumen:**

```javascript
function handleClickWithArgs(target) {
    console.log("Tombol diklik!", target.id);
}

onClick('myButton', handleClickWithArgs);
```

#### `onClicks(className, actionFunction)`

Menambahkan event klik ke semua elemen dengan class tertentu.

**Contoh tanpa argumen:**

```javascript
function handleMultipleClicks() {
    console.log("Sebuah elemen diklik!");
}

onClicks('myClass', handleMultipleClicks);
```

**Contoh dengan argumen:**

```javascript
function handleMultipleClicksWithArgs(element) {
    console.log("Elemen yang diklik:", element.className);
}

onClicks('myClass', handleMultipleClicksWithArgs);
```

#### `onChange(id, actionFunction)`

Menambahkan event perubahan nilai ke elemen berdasarkan ID.

```javascript
function handleChange(element) {
    console.log("Input berubah:", element.value);
}

onChange('myInput', handleChange);
```

#### `onChanges(className, actionFunction)`

Menambahkan event perubahan nilai ke semua elemen dengan class tertentu.

```javascript
function handleMultipleChanges(element) {
    console.log("Input diubah:", element.value);
}

onChanges('myClass', handleMultipleChanges);
```

#### `onInput(id, actionFunction)`

Menambahkan event input ke elemen berdasarkan ID.

```javascript
function handleInput(element) {
    console.log("Nilai input:", element.value);
}

onInput('myInput', handleInput);
```

#### `onInputs(className, actionFunction)`

Menambahkan event input ke semua elemen dengan class tertentu.

```javascript
function handleMultipleInputs(element) {
    console.log("Input berubah secara real-time:", element.value);
}

onInputs('myClass', handleMultipleInputs);
```

### Manipulasi DOM

#### `setValue(id, valueContent)`

Mengatur nilai dari input field.

```javascript
setValue('myInput', 'Nilai Baru');
```

#### `getValue(id)`

Mengambil nilai dari input field.

```javascript
const value = getValue('myInput');
console.log(value);
```

#### `setInner(id, content)`

Mengatur inner HTML dari elemen.

```javascript
setInner('myDiv', '<p>Halo Dunia</p>');
```

#### `setInnerText(id, content)`

Mengatur inner text dari elemen.

```javascript
setInnerText('myDiv', 'Halo Dunia');
```

### Visibilitas dan Gaya

#### `show(id)`

Menampilkan elemen dengan mengatur `display: block`.

```javascript
show('myDiv');
```

#### `hide(id)`

Menyembunyikan elemen dengan mengatur `display: none`.

```javascript
hide('myDiv');
```

### Pemuatan Konten Dinamis

#### `renderHTML(id, urlHTML, callback = null)`

Memuat konten HTML eksternal ke dalam elemen.

```javascript
function afterContentLoad() {
    console.log('Konten berhasil dimuat');
}

renderHTML('content', 'content/home.html', afterContentLoad);
```

#### replaceTag

Fungsi `replaceTag` digunakan untuk menggantikan elemen dengan ID tertentu di dalam dokumen dengan elemen dari file HTML eksternal.


```javascript
replaceTag('myElement', 'component.html', () => {
    console.log('Elemen berhasil diganti!');
});
```

Parameter

- `id` (**String**) - ID dari elemen yang akan diganti.
- `urlHTML` (**String**) - URL dari file HTML yang akan digunakan sebagai pengganti.
- `callback` (**Function**, opsional) - Fungsi yang akan dijalankan setelah elemen berhasil diganti.

Contoh Penggunaan

```html
<div id="content">Ini akan diganti</div>
<script>
    replaceTag('content', 'newContent.html', () => {
        console.log('Penggantian berhasil!');
    });
</script>
```

Fungsi replaceTag untuk menggantikan elemen dengan ID yang diberikan dengan elemen dari file HTML eksternal

### Pengelolaan Script dan CSS

#### `addJSInHead(src)`

Menambahkan file JavaScript secara dinamis ke dalam dokumen.

```javascript
await addJSInHead('https://example.com/script.js');
```

#### `addCSSInHead(href)`

Menambahkan file CSS secara dinamis ke dalam dokumen.

```javascript
await addCSSInHead('https://example.com/styles.css');
```

#### `isCSSLoaded(href)`

Memeriksa apakah file CSS sudah dimuat.

```javascript
if (isCSSLoaded('styles.css')) {
    console.log('CSS sudah dimuat');
}
```

#### `isJSLoaded(src)`

Memeriksa apakah file JavaScript sudah dimuat.

```javascript
if (isJSLoaded('script.js')) {
    console.log('JS sudah dimuat');
}
```

#### `addJS(src)`

Menambahkan file JavaScript ke dalam dokumen hanya jika belum dimuat sebelumnya.

```javascript
await addJS('https://example.com/script.js');
```

#### `addCSS(href)`

Menambahkan file CSS ke dalam dokumen hanya jika belum dimuat sebelumnya.

```javascript
await addCSS('https://example.com/styles.css');
```

## Kesimpulan

Modul utilitas ini menyederhanakan interaksi dengan DOM dan penanganan event, sehingga mempermudah pengelolaan aplikasi web dinamis. Gunakan fungsi-fungsi ini untuk merapikan kode JavaScript Anda!


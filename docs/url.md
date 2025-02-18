# Manual Penggunaan Fungsi url

## Pendahuluan
File ini berisi kumpulan fungsi JavaScript yang digunakan untuk mengambil dan mengelola informasi URL di dalam browser. Fungsi-fungsi ini dapat digunakan untuk mendapatkan informasi seperti protokol, host, path, query string, hash, serta mengatur atau mengubah elemen-elemen tersebut.

---

## Fungsi dan Cara Penggunaannya

### 1. `getProtocol()`
**Deskripsi:**
Mengembalikan protokol dari URL saat ini (contoh: `http` atau `https`).

**Cara penggunaan:**
```javascript
let protocol = getProtocol();
console.log(protocol); // Output: "https" atau "http"
```

---

### 2. `getHost()`
**Deskripsi:**
Mengembalikan host dari URL saat ini (contoh: `example.com:8080`).

**Cara penggunaan:**
```javascript
let host = getHost();
console.log(host); // Output: "example.com:8080"
```

---

### 3. `fullPath()`
**Deskripsi:**
Mengembalikan pathname lengkap dari URL saat ini.

**Cara penggunaan:**
```javascript
let path = fullPath();
console.log(path); // Output: "/folder/subfolder/page.html"
```

---

### 4. `folderPath()`
**Deskripsi:**
Mengembalikan path direktori dari URL tanpa nama file dan ekstensi.

**Cara penggunaan:**
```javascript
let folder = folderPath();
console.log(folder); // Output: "/folder/subfolder/"
```

---

### 5. `getPath()`
**Deskripsi:**
Mengembalikan pathname tanpa tanda `/` di awal.

**Cara penggunaan:**
```javascript
let path = getPath();
console.log(path); // Output: "folder/page.html"
```

---

### 6. `getQueryString()`
**Deskripsi:**
Mengembalikan query string dalam bentuk objek yang dapat diakses dengan properti.

**Cara penggunaan:**
```javascript
let query = getQueryString();
console.log(query.key); // Output: Nilai dari parameter "key" jika ada
```

---

### 7. `setQueryString(key, value)`
**Deskripsi:**
Menambahkan atau mengubah parameter dalam query string URL.

**Cara penggunaan:**
```javascript
setQueryString("page", "2"); // URL berubah menjadi ?page=2
```

---

### 8. `getHash()`
**Deskripsi:**
Mengembalikan hash (fragmen) dari URL tanpa simbol `#`.

**Cara penggunaan:**
```javascript
let hash = getHash();
console.log(hash); // Output: "section1"
```

---

### 9. `setHash(hashvalue)`
**Deskripsi:**
Mengatur nilai hash dalam URL.

**Cara penggunaan:**
```javascript
setHash("contact"); // URL berubah menjadi #contact
```

---

### 10. `redirect(URL)`
**Deskripsi:**
Mengalihkan pengguna ke URL yang diberikan.

**Cara penggunaan:**
```javascript
redirect("https://example.com"); // Browser akan diarahkan ke "https://example.com"
```

---

### 11. `onHashChange(runFunctionEvent)`
**Deskripsi:**
Menjalankan fungsi tertentu saat hash di URL berubah.

**Cara penggunaan:**
```javascript
onHashChange((event) => {
    console.log("Hash berubah: ", window.location.hash);
});
```

---

## Penutup
Fungsi-fungsi ini sangat berguna untuk mengelola URL dan navigasi halaman berbasis hash. Pastikan untuk menggunakannya dengan benar agar aplikasi dapat bekerja secara optimal.


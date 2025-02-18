# Dokumentasi Fungsi Cookie

## 1. setCookieWithExpireDay
### Deskripsi
Fungsi ini digunakan untuk menyimpan cookie dengan batas waktu kedaluwarsa dalam satuan hari.

### Parameter
- `cname` (string): Nama cookie.
- `cvalue` (string): Nilai cookie.
- `exdays` (number): Jumlah hari sebelum cookie kedaluwarsa.

### Contoh Penggunaan
```javascript
setCookieWithExpireDay("username", "JohnDoe", 7);
```

---

## 2. setCookieWithExpireHour
### Deskripsi
Fungsi ini digunakan untuk menyimpan cookie dengan batas waktu kedaluwarsa dalam satuan jam.

### Parameter
- `cname` (string): Nama cookie.
- `cvalue` (string): Nilai cookie.
- `exhour` (number): Jumlah jam sebelum cookie kedaluwarsa.

### Contoh Penggunaan
```javascript
setCookieWithExpireHour("sessionID", "abc123", 3);
```

---

## 3. setCookieWithExpireSecond
### Deskripsi
Fungsi ini digunakan untuk menyimpan cookie dengan batas waktu kedaluwarsa dalam satuan detik.

### Parameter
- `cname` (string): Nama cookie.
- `cvalue` (string): Nilai cookie.
- `exsecs` (number): Jumlah detik sebelum cookie kedaluwarsa.

### Contoh Penggunaan
```javascript
setCookieWithExpireSecond("tempData", "xyz789", 30);
```

---

## 4. deleteCookie
### Deskripsi
Fungsi ini digunakan untuk menghapus cookie dengan cara mengatur waktu kedaluwarsa ke masa lalu.

### Parameter
- `cname` (string): Nama cookie yang akan dihapus.

### Contoh Penggunaan
```javascript
deleteCookie("username");
```

---

## 5. getCookie
### Deskripsi
Fungsi ini digunakan untuk mendapatkan nilai cookie berdasarkan nama.

### Parameter
- `cname` (string): Nama cookie yang akan diambil nilainya.

### Return
- Mengembalikan nilai cookie jika ditemukan.
- Mengembalikan string kosong (`""`) jika cookie tidak ditemukan.

### Contoh Penggunaan
```javascript
let username = getCookie("username");
console.log(username);
```

---

## Catatan
- Cookie hanya akan tersedia pada domain dan path yang sama tempat cookie tersebut disimpan.
- Pastikan nilai cookie tidak mengandung karakter khusus tanpa encoding yang sesuai.
- Gunakan `encodeURIComponent` dan `decodeURIComponent` untuk memastikan nilai cookie aman untuk disimpan dan dibaca.


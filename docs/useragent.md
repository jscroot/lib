# isMobile()

## Deskripsi
Fungsi `isMobile()` digunakan untuk mendeteksi apakah pengguna sedang mengakses aplikasi atau situs web dari perangkat mobile.

## Instalasi
Fungsi ini dapat digunakan langsung dalam proyek JavaScript Anda. Cukup impor dan gunakan sesuai kebutuhan.

```javascript
import { isMobile } from './nama_file';
```

## Penggunaan
Panggil fungsi `isMobile()` untuk mendapatkan nilai boolean yang menunjukkan apakah pengguna menggunakan perangkat mobile atau tidak.

```javascript
if (isMobile()) {
    console.log("Pengguna menggunakan perangkat mobile.");
} else {
    console.log("Pengguna menggunakan perangkat desktop.");
}
```

## Cara Kerja
Fungsi ini memeriksa `navigator.userAgent` untuk menentukan apakah string agen pengguna cocok dengan daftar perangkat mobile yang umum, seperti:
- Android
- iPhone
- iPad
- iPod
- BlackBerry
- IEMobile
- Opera Mini

Jika ada kecocokan, fungsi mengembalikan `true`, menandakan bahwa perangkat tersebut adalah perangkat mobile. Jika tidak, fungsi mengembalikan `false`.

## Catatan
- Deteksi berbasis `userAgent` tidak selalu akurat karena beberapa perangkat atau browser dapat memanipulasi nilai `userAgent`.
- Untuk pendekatan yang lebih andal, bisa menggunakan fitur pendeteksian media query CSS atau API lain seperti `window.matchMedia`.

## Lisensi
Fungsi ini dapat digunakan dan dimodifikasi sesuai kebutuhan tanpa batasan lisensi.


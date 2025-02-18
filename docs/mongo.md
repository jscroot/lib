# README

## Tata Cara Penggunaan Fungsi Mongo

### 1. **getDateFromObjectId**
#### Deskripsi
Fungsi `getDateFromObjectId` digunakan untuk mendapatkan tanggal dan waktu dari sebuah ObjectId yang dihasilkan dalam format MongoDB.

#### Parameter
- `stringID` (String): ObjectId dalam format string.

#### Cara Kerja
- Fungsi ini mengambil 8 karakter pertama dari ObjectId, yang merupakan representasi heksadesimal dari timestamp Unix.
- Konversi nilai heksadesimal tersebut ke bilangan desimal.
- Kalikan dengan 1000 untuk mendapatkan nilai dalam milidetik.
- Kembalikan sebagai objek `Date` JavaScript.

#### Contoh Penggunaan
```javascript
import { getDateFromObjectId } from 'https://cdn.jsdelivr.net/gh/jscroot/lib@0.2.2/mongo.js';

const objectId = "65d9a3f8b7e8d6c3a4f9e0d1";
const date = getDateFromObjectId(objectId);
console.log(date); // Output: Tanggal dan waktu dari ObjectId
```

### 2. **generateObjectId**
#### Deskripsi
Fungsi `generateObjectId` digunakan untuk membuat ObjectId baru yang menyerupai format yang digunakan dalam MongoDB.

#### Cara Kerja
- Mendapatkan timestamp Unix dalam detik, dikonversi ke format heksadesimal.
- Menghasilkan 16 karakter acak dalam format heksadesimal.
- Menggabungkan timestamp dan angka acak untuk membentuk ObjectId.

#### Contoh Penggunaan
```javascript
import { generateObjectId } from 'https://cdn.jsdelivr.net/gh/jscroot/lib@0.2.2/mongo.js';

const newObjectId = generateObjectId();
console.log(newObjectId); // Output: String ObjectId baru
```

### Catatan
- Fungsi `generateObjectId` tidak menjamin keunikan 100% seperti yang dihasilkan oleh MongoDB karena bagian acaknya tidak menggunakan identifier khusus seperti hostname atau process ID.
- Pastikan bahwa ObjectId yang digunakan sesuai dengan kebutuhan sistem Anda.


# **Penggunaan Fungsi Validasi dan Format Input**  

Dokumen ini menjelaskan bagaimana cara menggunakan empat fungsi JavaScript berikut:  

1. **validateUserName** → Memproses input username agar hanya mengandung huruf kecil, angka, underscore (_), dan tanda hubung (-).  
2. **validatePhoneNumber** → Memastikan nomor telepon hanya mengandung angka dan diawali dengan kode negara Indonesia (62).  
3. **formatRupiah** → Memformat angka menjadi tampilan mata uang Rupiah (Rp).  
4. **onInput** → Menambahkan event `oninput` secara dinamis pada elemen input.  

---

## **1. Validasi Username (`validateUserName`)**  

### **Deskripsi:**  
- Mengonversi input menjadi huruf kecil.  
- Menghapus spasi dalam input.  
- Hanya mengizinkan huruf, angka, underscore (_), dan tanda hubung (-).  

### **Cara Penggunaan Langsung di HTML:**  
```html
<input type="text" id="username" placeholder="Masukkan username" oninput="validateUserName(this)">
```
Atau menggunakan JavaScript:  
```js
document.getElementById('username').addEventListener('input', function() {
    validateUserName(this);
});
```
Menggunakan `onInput`:  
```js
onInput('username', validateUserName);
```

### **Contoh Input & Output:**  
| **Input**      | **Output**  |  
|---------------|------------|  
| `User Name!@#` | `username` |  
| `Test_ 123`   | `test_123`  |  

---

## **2. Validasi Nomor Telepon (`validatePhoneNumber`)**  

### **Deskripsi:**  
- Hanya mengizinkan angka dalam input.  
- Jika angka pertama adalah `0`, akan diganti dengan `62` (kode negara Indonesia).  

### **Cara Penggunaan Langsung di HTML:**  
```html
<input type="text" id="phone" placeholder="Masukkan nomor telepon" oninput="validatePhoneNumber(this)">
```
Menggunakan JavaScript:  
```js
document.getElementById('phone').addEventListener('input', function() {
    validatePhoneNumber(this);
});
```
Menggunakan `onInput`:  
```js
onInput('phone', validatePhoneNumber);
```

### **Contoh Input & Output:**  
| **Input**      | **Output**  |  
|---------------|------------|  
| `08123456789` | `628123456789` |  
| `+62 812-3456` | `628123456` |  

---

## **3. Format Rupiah (`formatRupiah`)**  

### **Deskripsi:**  
- Memastikan input hanya berupa angka dan tanda koma untuk desimal.  
- Memformat angka menjadi mata uang Rupiah (`Rp`).  
- Menyimpan nilai asli tanpa format di atribut `data-value`.  

### **Cara Penggunaan Langsung di HTML:**  
```html
<input type="text" id="harga" placeholder="Masukkan harga" oninput="formatRupiah(this)">
```
Menggunakan JavaScript:  
```js
document.getElementById('harga').addEventListener('input', function() {
    formatRupiah(this);
});
```
Menggunakan `onInput`:  
```js
onInput('harga', formatRupiah);
```

### **Contoh Input & Output:**  
| **Input**      | **Output (Ditampilkan)** | **Data-Value (Tersembunyi)** |  
|---------------|-----------------|-----------------|  
| `1000000`     | `Rp. 1.000.000` | `1000000` |  
| `25000,50`    | `Rp. 25.000,50` | `25000,50` |  

---

## **4. Menambahkan Event Secara Dinamis (`onInput`)**  

### **Deskripsi:**  
- Fungsi ini memungkinkan kita untuk menetapkan fungsi validasi secara dinamis ke elemen input berdasarkan `id`.  
- Mengurangi penulisan kode secara manual di HTML.  

### **Cara Penggunaan:**  
```js
onInput('username', validateUserName);
onInput('phone', validatePhoneNumber);
onInput('harga', formatRupiah);
```
Kode di atas akan secara otomatis menambahkan event `oninput` ke elemen dengan ID yang disebutkan.  

---

Dengan menggunakan fungsi `onInput`, kita dapat menulis kode yang lebih ringkas dan fleksibel dalam menangani validasi input pengguna. 🚀
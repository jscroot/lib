# API

## getJSON

Anda bisa langsung memanggilnya seperti ini tanpa harus menyertakan parameter `tokenkey` dan `tokenvalue` jika tidak diperlukan:

```javascript
// URL yang ingin diambil datanya
const url = 'https://api.example.com/data';

// Fungsi yang akan menangani respons dari server
function handleResponse(response) {
    console.log('Status:', response.status);
    console.log('Data:', response.data);
}

// Menggunakan fungsi getJSON tanpa token
getJSON(url, handleResponse);
```

Jika Anda perlu menambahkan token, cukup berikan `tokenkey` dan `tokenvalue` seperti ini:

```javascript
const tokenKey = 'Authorization';
const tokenValue = 'Bearer your-token-here';
getJSON(url, handleResponse, tokenKey, tokenValue);
```
## postJSON

Anda dapat memanggil fungsi `postJSON` seperti ini:

### Tanpa Token:
```javascript
const url = 'https://api.example.com/data';
const data = { key1: 'value1', key2: 'value2' };

// Fungsi untuk menangani respons
function handleResponse(response) {
    console.log('Status:', response.status);
    console.log('Data:', response.data);
}

// Menggunakan fungsi postJSON tanpa token
postJSON(url, data, handleResponse);
```

### Dengan Token:
```javascript
const tokenKey = 'Authorization';
const tokenValue = 'Bearer your-token-here';
postJSON(url, data, handleResponse, tokenKey, tokenValue);
```

parameter `tokenkey` dan `tokenvalue` menjadi opsional, dan Anda bisa memanggil fungsi `postJSON` lebih sederhana jika tidak membutuhkan token.

## deleteJSON

### Tanpa Token:
```javascript
const url = 'https://api.example.com/data';
const data = { key1: 'value1', key2: 'value2' };

// Fungsi untuk menangani respons
function handleResponse(response) {
    console.log('Status:', response.status);
    console.log('Data:', response.data);
}

// Menggunakan fungsi deleteJSON tanpa token
deleteJSON(url, data, handleResponse);
```

### Dengan Token:
```javascript
const tokenKey = 'Authorization';
const tokenValue = 'Bearer your-token-here';
deleteJSON(url, data, handleResponse, tokenKey, tokenValue);
```

Anda dapat menggunakan `deleteJSON` lebih fleksibel tanpa harus selalu menyertakan token, jika tidak diperlukan.

## putJSON

### Tanpa Token:
```javascript
const url = 'https://api.example.com/data';
const data = { key1: 'value1', key2: 'value2' };

// Fungsi untuk menangani respons
function handleResponse(response) {
    console.log('Status:', response.status);
    console.log('Data:', response.data);
}

// Menggunakan fungsi putJSON tanpa token
putJSON(url, data, handleResponse);
```

### Dengan Token:
```javascript
const tokenKey = 'Authorization';
const tokenValue = 'Bearer your-token-here';
putJSON(url, data, handleResponse, tokenKey, tokenValue);
```

fungsi `putJSON` bisa digunakan dengan atau tanpa token, menjadikannya lebih fleksibel sesuai dengan kebutuhan.
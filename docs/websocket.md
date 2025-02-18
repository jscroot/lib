# WebSocket Functions

## Pendahuluan
Dokumen ini menjelaskan penggunaan fungsi-fungsi yang terkait dengan WebSocket yang telah dibuat dalam file JavaScript. Fungsi ini memungkinkan komunikasi real-time antara client dan server menggunakan WebSocket.

## Daftar Fungsi

### 1. `openWebSocketSetId(id, url_ws)`
Fungsi ini digunakan untuk membuka koneksi WebSocket dan mengatur ID pengguna.

**Parameter:**
- `id` (string) - ID pengguna yang akan dikirim ke server setelah koneksi dibuka.
- `url_ws` (string, base64-encoded) - URL WebSocket dalam format base64 yang akan digunakan untuk membuat koneksi.

**Return:**
- Mengembalikan objek WebSocket jika koneksi berhasil.

**Cara Penggunaan:**
```javascript
let wsocket = openWebSocketSetId("user123", "d3M6Ly8xMjcuMC4wLjE6ODA=");
```

### 2. `connectws(id, url_ws)`
Fungsi ini digunakan untuk membuat koneksi WebSocket dengan server dan mengatur ID pengguna setelah koneksi berhasil.

**Parameter:**
- `id` (string) - ID pengguna yang dikirim ke server setelah koneksi berhasil.
- `url_ws` (string, base64-encoded) - URL WebSocket dalam format base64.

**Return:**
- Mengembalikan `Promise` yang akan menyelesaikan koneksi WebSocket jika berhasil atau menolak jika terjadi error.

**Cara Penggunaan:**
```javascript
connectws("user123", "d3M6Ly8xMjcuMC4wLjE6ODA=").then(ws => {
  console.log("WebSocket berhasil terkoneksi");
}).catch(err => {
  console.log("Gagal koneksi WebSocket", err);
});
```

### 3. `closeWebSocket(wsocket)`
Fungsi ini digunakan untuk menutup koneksi WebSocket yang sedang aktif.

**Parameter:**
- `wsocket` (WebSocket) - Objek WebSocket yang ingin ditutup.

**Cara Penggunaan:**
```javascript
closeWebSocket(wsocket);
```

### 4. `sendMessagetoWebSocket(msg, wsocket)`
Fungsi ini digunakan untuk mengirim pesan ke server melalui WebSocket yang telah terbuka.

**Parameter:**
- `msg` (string) - Pesan yang akan dikirim ke server.
- `wsocket` (WebSocket) - Objek WebSocket yang digunakan untuk mengirim pesan.

**Cara Penggunaan:**
```javascript
sendMessagetoWebSocket("Hello, Server!", wsocket);
```

## Catatan Tambahan
- Pastikan browser yang digunakan mendukung WebSocket.
- URL WebSocket harus dalam format base64 sebelum dikirim ke fungsi.
- Pastikan WebSocket dalam keadaan terbuka (`wsocket.readyState === WebSocket.OPEN`) sebelum mengirim pesan untuk menghindari error.
- Gunakan `catcher(messages);` dalam fungsi `onmessage` untuk menangani pesan yang diterima dari server.


---
redirect_to: https://croot.js.org/lib/
---

# JSCroot lib sekarang CrootJS

Library ini sudah berganti nama menjadi **CrootJS**: [`crootjs/lib`](https://github.com/crootjs/lib), dokumentasi di [croot.js.org/docs](https://croot.js.org/docs/). Repo ini tidak diperbarui lagi. Versi lama (`v0.2.8` dan sebelumnya) tetap tersedia di jsDelivr, jadi aplikasi yang sudah memakainya tidak rusak.

Untuk pindah, ganti alamat import, lalu cek perbedaan fungsi di dokumentasi CrootJS (misalnya `api.js` kini juga mengembalikan Promise dan memberi `status: 0` saat jaringan gagal):

```js
// dulu
import { getCookie } from "https://cdn.jsdelivr.net/gh/jscroot/lib@0.2.8/cookie.js";
// sekarang
import { getCookie } from "https://cdn.jsdelivr.net/gh/crootjs/lib@0.0.30/cookie.js";
```

---

# JSCRoot Library

Start with calling ES Module Javascript from html file
```html
<script type="module" src="croot.js"></script>
```
Begin javascript with import JSCroot Component [Here](https://www.jsdelivr.com/package/gh/jscroot/lib?tab=files)
```js
import {getCookie} from "https://cdn.jsdelivr.net/gh/jscroot/lib@0.2.8/cookie.js";
import {redirect} from "https://cdn.jsdelivr.net/gh/jscroot/lib@0.2.8/url.js";

if (getCookie("login")===""){
    redirect("/");
}
```

## Docs

* [element.js](./docs/element.md)
* [api.js](./docs/api.md)
* [cookie.js](./docs/cookie.md)
* [url.js](./docs/url.md)
* [validate.js](./docs/validate.md)
* [mongo.js](./docs/mongo.md)
* [useragent.js](./docs/useragent.md)
* [websocket.js](./docs/websocket.md)

---

## Release Tag
```sh
git tag                                 #check current version
git tag v0.2.8                          #set tag version
git push origin --tags                  #push tag version to repo
```
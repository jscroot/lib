# JSCRoot Library

Start with calling ES Module Javascript from html file
```html
<script type="module" src="index.js"></script>
```
Begin javascript with import JSCroot Component
```js
import {getCookie} from "https://cdn.jsdelivr.net/gh/jscroot/lib@0.2.0/cookie.js";
import {redirect} from "https://cdn.jsdelivr.net/gh/jscroot/lib@0.2.0/url.js";

if (getCookie("login")===""){
    redirect("/");
}
```

## Docs

* [api.js](./docs/api.md)

### getCookie(cname)
```js
if (getCookie("login")===""){
    redirect("/");
}
```

## validate.js

Fungsi validasi inputan user

###  formatRupiah(input)
Untuk mendapatkan format harga dalam rupiah pada inputan
```js
onInput('harga', formatRupiah);//element objek harga ikut jadi argumen fungsi formatrupiah
const harga=getAttributeValue('id','data-value');
```

## Quick Start with ChatGPT

Using JSCroot assisted by chatGPT:
1. Download source code from [release page](https://github.com/jscroot/lib/releases)
2. Extract, choose js file and upload it into ChatGPT Prompt, for example : api.js
3. Input this text:
   ```txt
   I want to use JSCroot as ES modules to build my website, this is my library file from:
   https://cdn.jsdelivr.net/gh/jscroot/lib@0.2.0/api.js
   ```
4. Other option: if you cant upload file, just paste the code inside api.js after cdn url with several new line
   ```txt
   I want to use JSCroot as ES modules to build my website, this is my library file from:
   https://cdn.jsdelivr.net/gh/jscroot/lib@0.2.0/api.js

   ...content inside api.js file...
   ```

## Release Tag
```sh
git tag                                 #check current version
git tag v0.2.1                          #set tag version
git push origin --tags                  #push tag version to repo
```
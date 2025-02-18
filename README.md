# JSCRoot Library

Start with calling ES Module Javascript from html file
```html
<script type="module" src="index.js"></script>
```
Begin javascript with import JSCroot Component [Here](https://www.jsdelivr.com/package/gh/jscroot/lib?tab=files)
```js
import {getCookie} from "https://cdn.jsdelivr.net/gh/jscroot/lib@0.2.2/cookie.js";
import {redirect} from "https://cdn.jsdelivr.net/gh/jscroot/lib@0.2.2/url.js";

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
git tag v0.2.3                          #set tag version
git push origin --tags                  #push tag version to repo
```
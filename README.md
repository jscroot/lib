# JSCRoot Library

## Quick Start with ChatGPT

Using JSCroot assisted by chatGPT:
1. Download source code from [release page](https://github.com/jscroot/lib/releases)
2. Extract, choose js file and upload it into ChatGPT Prompt, for example : api.js
3. Input this text:
   ```txt
   I want to use JSCroot as ES modules to build my website, this is my library file from:
   https://cdn.jsdelivr.net/gh/jscroot/lib@0.0.9/api.js
   ```
4. Other option: if you cant upload file, just paste the code inside api.js after cdn url with several new line
   ```txt
   I want to use JSCroot as ES modules to build my website, this is my library file from:
   https://cdn.jsdelivr.net/gh/jscroot/lib@0.0.9/api.js

   ...content inside api.js file...
   ```

## CDN List
```txt
https://cdn.jsdelivr.net/gh/jscroot/lib@0.0.9/api.js
https://cdn.jsdelivr.net/gh/jscroot/lib@0.0.9/cookie.js
https://cdn.jsdelivr.net/gh/jscroot/lib@0.0.9/element.js
https://cdn.jsdelivr.net/gh/jscroot/lib@0.0.9/image.js
https://cdn.jsdelivr.net/gh/jscroot/lib@0.0.9/loading.js
https://cdn.jsdelivr.net/gh/jscroot/lib@0.0.9/mongo.js
https://cdn.jsdelivr.net/gh/jscroot/lib@0.0.9/url.js
https://cdn.jsdelivr.net/gh/jscroot/lib@0.0.9/useragent.js
https://cdn.jsdelivr.net/gh/jscroot/lib@0.0.9/websocket.js
```
## Release Tag
```sh
git tag                                 #check current version
git tag v0.0.9                          #set tag version
git push origin --tags                  #push tag version to repo
```
# XMLHttpRequest Deno Polyfill

A polyfill of XMLHttpRequest for Deno (and other browser and browser-like environments) by browserifying [@driverdan/node-XMLHttpRequest](https://github.com/driverdan/node-XMLHttpRequest).

```js
import XMLHttpRequest from ""https://deno.land/x/xmlhttprequest_deno@v0.0.1/mod.js";

let xhr = new XMLHttpRequest();
xhr.onreadystatechange = function() {
  if(this.readyState == 4 && this.status == 200) {
    console.log(this.responseText);
  }
};

xhr.open("GET", "https://example.com", true);
xhr.send();
```

**Note:** @kitsonk (a core Deno dev) has published a TypeScript `XMLHttpRequest` polyfill that may or may not suit your purposes better: https://github.com/kitsonk/xhr It is ~actively maintained, unlike this repo, and you could strip types from it fairly easily if you need a pure JS module.

---

# XMLHttpRequest Deno Polyfill

A **buggy** polyfill of XMLHttpRequest for Deno (and other browser and browser-like environments) by browserifying [@driverdan/node-XMLHttpRequest](https://github.com/driverdan/node-XMLHttpRequest).

```js
import XMLHttpRequest from "https://deno.land/x/xmlhttprequest_deno@v0.0.2/mod.js";

let xhr = new XMLHttpRequest();
xhr.onreadystatechange = function() {
  if(this.readyState == 4 && this.status == 200) {
    console.log(this.responseText);
  }
};

xhr.open("GET", "https://example.com", true);
xhr.send();
```

# TODO

* Fix the major bugs mentioned here:
  * https://github.com/driverdan/node-XMLHttpRequest/issues
  * https://github.com/driverdan/node-XMLHttpRequest/pulls

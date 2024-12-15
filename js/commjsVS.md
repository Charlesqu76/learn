### CommonJS VS ES Module


#### CommonJs
> CommonJS is a  _**synchronous**_  module system, This means that when a module is imported, the code execution is blocked until the module is loaded.The module system uses the require function to import modules and the module.exports object to export modules.

```
// export module
module.exports = { test: 1 };

// import module
const test = require("./test");
console.log(test); // { test: 1 }
```


#### ES module

> ES Modules represents a more modern approach to JavaScript module management, using an  _**asynchronous**_  model for loading modules

```
// export module
export const a = { a: 1 };
const b = { b: 2 };
export default b;

// import module
import b, { a } from "./test.mjs";
console.log(a); // { a: 1 }
console.log(b); // { b: 2 }
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTc4ODA1OTM4Nl19
-->
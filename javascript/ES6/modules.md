# Modules

Prior to ES6, we used libraries such as Browserify to create modules on the client-side, and require in Node.js. With ES6, we can now directly use modules of all types (AMD and CommonJS).

## Exporting in CommonJS

```
module.exports = 1;
module.exports = { foo: 'bar' };
module.exports = ['foo', 'bar'];
module.exports = function bar () {};
```

## Exporting in ES6

With ES6, we have various flavors of exporting. We can perform Named Exports:

```
export let name = 'David';
export let age  = 25;​​
```

As well as exporting a list of objects:
```
function sumTwo(a, b) {
    return a + b;
}

function sumThree(a, b, c) {
    return a + b + c;
}

export { sumTwo, sumThree };
```

```
// lib/math.js
export function sum(x, y) {
  return x + y;
}
export var pi = 3.141593;
```

```
// app.js
import * as math from "lib/math";
alert("2π = " + math.sum(math.pi, math.pi));
```

```
// otherApp.js
import {sum, pi} from "lib/math";
alert("2π = " + sum(pi, pi));
```

[Source](https://github.com/DrkSephy/es6-cheatsheet#modules)
[Source](https://github.com/lukehoban/es6features#modules)

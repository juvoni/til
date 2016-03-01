# Maps

- A replacement to the common pattern of creating a hash-map using plain JavaScript objects
    - Avoids security issues with user-provided keys
    - Allows keys to be arbitrary values, you can even use DOM elements or functions as the key to an entry

Use ``map.set(key, value)`` to add entries
Use ``map.get(key)`` to get an entry

Check for a key using ``map.has(key)``
Remove entries with ``map.delete(key)``

The most amazing part of Maps is that we are no longer limited to just using strings. We can now use any type as a key, and it will not be type-cast to a string.

```
let map = new Map([
    ['name', 'david'],
    [true, 'false'],
    [1, 'one'],
    [{}, 'object'],
    [function () {}, 'function']
]);

for (let key of map.keys()) {
    console.log(typeof key);
    // > string, boolean, number, object, function
}
```

> Note: Using non-primitive values such as functions or objects won't work when testing equality using methods such as map.get(). As such, stick to primitive values such as Strings, Booleans and Numbers.

We can also iterate over maps using ``.entries()``:

```
for (let [key, value] of map.entries()) {
    console.log(key, value);
}
```

[Source](https://github.com/bevacqua/es6#maps)
[Source](https://github.com/DrkSephy/es6-cheatsheet#symbols)


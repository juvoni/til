# Strings

With ES6, the standard library has grown immensely. Along with these changes are new methods which can be used on strings, such as ``.includes()`` and .``repeat()``.

## includes( )

```
var string = 'food';
var substring = 'foo';

console.log(string.indexOf(substring) > -1);
```

Instead of checking for a return value > -1 to denote string containment, we can simply use .includes() which will return a boolean:

```
const string = 'food';
const substring = 'foo';

console.log(string.includes(substring)); // true
```


## .repeat( )

```
function repeat(string, count) {
    var strings = [];
    while(strings.length < count) {
        strings.push(string);
    }
    return strings.join('');
}
```

In ES6, we now have access to a terser implementation:
```
// String.repeat(numberOfRepetitions)
'meow'.repeat(3); // 'meowmeowmeow'
```

Also added

``String.prototype.startsWith`` -- whether the string starts with value
``String.prototype.endsWith`` -- whether the string ends in value

[Source](https://github.com/DrkSephy/es6-cheatsheet#strings)
[Source](https://github.com/bevacqua/es6#strings-and-unicode)


#Arrow Functions

One common solution to this problem is to store the context of this using a variable:

```
function Person(name) {
    this.name = name;
}

Person.prototype.prefixName = function (arr) {
    var that = this; // Store the context of this
    return arr.map(function (character) {
        return that.name + character;
    });
};
```


> Best Practice: Use Arrow Functions whenever you need to preserve the lexical value of this.

Using Arrow Functions, the lexical value of this isn't shadowed and we can re-write the above as shown:

```
function Person(name) {
    this.name = name;
}

Person.prototype.prefixName = function (arr) {
    return arr.map(character => this.name + character);
};
```


> Best Practice: Use Arrow Functions in place of function expressions when possible.

Arrow Functions are also more concise when used in function expressions which simply return a value:

Terse way to declare a function like param => returnValue

```
var squares = arr.map(function (x) { return x * x }); // Function Expression
```

```
const arr = [1, 2, 3, 4, 5];
const squares = arr.map(x => x * x); // Arrow Function for terser implementation
```


- To return an object implicitly, wrap it in parenthesis () => ({ foo: 'bar' }) or you'll get an error
- Parenthesis are demanded when you have zero, two, or more parameters, () => expr or (p1, p2) => expr
- When using a code block, there's no implicit return, you'll have to provide it -- () => { return 'foo' }


[Source](https://github.com/DrkSephy/es6-cheatsheet#arrow-functions)



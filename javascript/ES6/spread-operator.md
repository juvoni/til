# Spread Operator

In ES5, we could find the max of values in an array by using the apply method on Math.max like this:

```
Math.max.apply(null, [-1, 100, 9001, -32]); // 9001
```

In ES6, we can now use the spread operator to pass an array of values to be used as parameters to a function:

```
Math.max(...[-1, 100, 9001, -32]); // 9001
```

We can concat array literals easily with this intuitive syntax:

```
let cities = ['San Francisco', 'Los Angeles'];
let places = ['Miami', ...cities, 'Chicago']; // ['Miami', 'San Francisco', 'Los Angeles', 'Chicago']
```

[Source](https://github.com/DrkSephy/es6-cheatsheet#strings)

- Rest parameters is a better `arguments`
  - You declare it in the method signature like `function foo (...everything) {}`
  - `everything` is an array with all parameters passed to `foo`
  - You can name a few parameters before `...everything`, like `function foo (bar, ...rest) {}`
  - Named parameters are excluded from `...rest`
  - `...rest` must be the last parameter in the list
- Spread operator is better than magic, also denoted with `...` syntax
  - Avoids `.apply` when calling methods, `fn(...[1, 2, 3])` is equivalent to `fn(1, 2, 3)`
  - Easier concatenation `[1, 2, ...[3, 4, 5], 6, 7]`
  - Casts array-likes or iterables into an array, e.g `[...document.querySelectorAll('img')]`
  - Useful when [destructuring](#assignment-destructuring) too, `[a, , ...rest] = [1, 2, 3, 4, 5]` yields `a: 1` and `rest: [3, 4, 5]`
  - Makes `new` + `.apply` effortless, `new Date(...[2015, 31, 8])`

[Source](https://github.com/bevacqua/es6#spread-operator-and-rest-parameters)

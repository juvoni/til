#Assignment Destructuring

Destructuring allows us to extract values from arrays and objects (even deeply nested) and store them in variables with a more convenient syntax.

###Destructuring Arrays

```
var {foo} = pony is equivalent to var foo = pony.foo
```

You can provide default values, 

```
var {foo='bar'} = baz yields foo: 'bar' if baz.foo is undefined
```

Properties that aren't found yield undefined as usual, e.g: 

```
var {foo} = {}
```

*ES5*

```
var arr = [1, 2, 3, 4];
var a = arr[0];
var b = arr[1];
var c = arr[2];
var d = arr[3];
```

*ES6*

```
let [a, b, c, d] = [1, 2, 3, 4];
```

###Destructuring Objects

*ES5*

```
var luke = { occupation: 'jedi', father: 'anakin' };
var occupation = luke.occupation; // 'jedi'
var father = luke.father; // 'anakin'
```

*ES6*

```
let luke = { occupation: 'jedi', father: 'anakin' };
let {occupation, father} = luke;
```

[Source](https://github.com/bevacqua/es6)
[Source](https://github.com/DrkSephy/es6-cheatsheet#destructuring)

# Classes

- Not "traditional" classes, syntax sugar on top of prototypal inheritance
- Syntax similar to declaring objects, ```class Foo {}```
- Prototypal inheritance with a simple syntax ```class PonyFoo extends Foo {}```
- Constructor method ```class Foo { constructor () { /* initialize instance */ } }```

```
class Person {
    constructor(name, age, gender) {
        this.name   = name;
        this.age    = age;
        this.gender = gender;
    }

    incrementAge() {
      this.age += 1;
    }
}
```


And extend them using the ```extends``` keyword:

```
class Personal extends Person {
    constructor(name, age, gender, occupation, hobby) {
        super(name, age, gender);
        this.occupation = occupation;
        this.hobby = hobby;
    }

    incrementAge() {
        super.incrementAge();
        this.age += 20;
        console.log(this.age);
    }
}
```

>Best Practice: While the syntax for creating classes in ES6 obscures how implementation and prototypes work under the hood, it is a good feature for beginners and allows us to write cleaner code.

[Source](https://github.com/bevacqua/es6#classes)
[Source](https://github.com/DrkSephy/es6-cheatsheet#classes)




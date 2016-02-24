# Generators

Generator functions are a special kind of iterator that can be declared using the ```function* generator () {}``` syntax

Generator functions use yield to emit an element sequence

```
function* sillyGenerator() {
    yield 1;
    yield 2;
    yield 3;
    yield 4;
}

var generator = sillyGenerator();
> console.log(generator.next()); // { value: 1, done: false }
> console.log(generator.next()); // { value: 2, done: false }
> console.log(generator.next()); // { value: 3, done: false }
> console.log(generator.next()); // { value: 4, done: false }
```

- Generator functions return a generator object that's adheres to both the iterable and iterator protocols
    + Given g = generator(), g adheres to the iterable protocol because g[Symbol.iterator] is a method
    + Given g = generator(), g adheres to the iterator protocol because g.next is a method
    + The iterator for a generator object g is the generator itself: g[Symbol.iterator]() === g

- Generator function execution is suspended, remembering the last position, in four different cases
    + A yield expression returning the next value in the sequence
    + A return statement returning the last value in the sequence
    + A throw statement halts execution in the generator entirely
    + Reaching the end of the generator function signals { done: true }

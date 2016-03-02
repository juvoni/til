# Promises

Promises behave like a tree. Add branches with p.then(handler) and p.catch(handler)

Promises allow us to turn our horizontal code (callback hell):

```
func1(function (value1) {
    func2(value1, function (value2) {
        func3(value2, function (value3) {
            func4(value3, function (value4) {
                func5(value4, function (value5) {
                    // Do something with value 5
                });
            });
        });
    });
});
```

Into vertical code:
```
func1(value1)
    .then(func2)
    .then(func3)
    .then(func4)
    .then(func5, value5 => {
        // Do something with value 5
    });
```

Prior to ES6, we used bluebird or Q. Now we have Promises natively:

```
new Promise((resolve, reject) =>
    reject(new Error('Failed to fulfill Promise')))
        .catch(reason => console.log(reason));
```

- Create new `p` promises with `new Promise((resolve, reject) => { /* resolver */ })`
    - The resolve(value) callback will fulfill the promise with the provided value
    - The reject(reason) callback will reject p with a reason error
    - You can call those methods asynchronously, blocking deeper branches of the promise tree

> Benefits of Promises: Error Handling using a bunch of nested callbacks can get chaotic. Using Promises, we have a clear path to bubbling errors up and handling them appropriately. Moreover, the value of a Promise after it has been resolved/rejected is immutable - it will never change.

[Source](https://github.com/DrkSephy/es6-cheatsheet#promises)
[Source](https://github.com/bevacqua/es6#promises)


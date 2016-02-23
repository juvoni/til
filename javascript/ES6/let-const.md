# Let + Const

Block-scoped binding constructs. let is the new var. const is single-assignment. Static restrictions prevent use before assignment.

```
function f() {
  {
    let x;
    {
      // okay, block scoped name
      const x = "sneaky";
      // error, const
      x = "foo";
    }
    // error, already declared in block
    let x = "inner";
  }
}
```

> Note: let and const are block scoped. Therefore, referencing block-scoped identifiers before they are defined will produce a ReferenceError.

> Best Practice: Leave var declarations inside of legacy code to denote that it needs to be carefully refactored. When working on a new codebase, use let for variables that will change their value over time, and const for variables which cannot be reassigned.

- let is hoisted to the top of the block, while var declarations are hoisted to top of the function
- const variables must be declared using an initializer, ```const foo = 'bar'```

const variables don’t make the assigned value immutable

```const foo = { bar: 'baz' }``` means foo will always reference the right-hand side object
``const foo = { bar: 'baz' };`` ``foo.bar = 'boo'`` won't throw error. foo.bar will be 'boo'



[Source](https://github.com/lukehoban/es6features#let--const)
[Source](https://github.com/DrkSephy/es6-cheatsheet#var-versus-let--const)
[Source](https://github.com/bevacqua/es6#let-and-const)

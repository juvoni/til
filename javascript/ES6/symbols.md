# Symbols

- A new primitive type in ES6
- You can create your own symbols using var symbol = Symbol()
- You can add a description for debugging purposes, like Symbol('ponyfoo')
- Symbols are immutable and unique. Symbol(), Symbol(), Symbol('foo') and Symbol('foo') are all different
- Symbols are of type symbol, thus: typeof Symbol() === 'symbol'

## Symbol( )

Calling Symbol() or Symbol(description) will create a unique symbol that cannot be looked up globally. A Use case for Symbol() is to patch objects or namespaces from third parties with your own logic, but be confident that you won't collide with updates to that library. 

## Symbol.for(key)

Symbol.for(key) will create a Symbol that is still immutable and unique, but can be looked up globally. Two identical calls to Symbol.for(key) will return the same Symbol instance. NOTE: This is not true for Symbol(description):

```
Symbol('foo') === Symbol('foo') // false
Symbol.for('foo') === Symbol('foo') // false
Symbol.for('foo') === Symbol.for('foo') // true
```

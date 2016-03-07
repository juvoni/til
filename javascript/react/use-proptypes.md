# Always set propTypes for validation and self-documentation

> From  John Cobb - An opinionated guide to React.js best practices and conventions

I always use propTypes to provide validation for each prop the component will receive. Furthermore, this also provides a self-documenting reference for how the component should be used, and what props it needs to be passed.

```
propTypes: {
        arrayProp: React.PropTypes.array,
        boolProp: React.PropTypes.bool,
        funcProp: React.PropTypes.func,
        numProp: React.PropTypes.number,
        objProp: React.PropTypes.object,
        stringProp: React.PropTypes.string,
    }
```

[Source](https://web-design-weekly.com/2015/01/29/opinionated-guide-react-js-best-practices-conventions/)

# Check if Object is Empty

ECMA 5+:

```
Object.keys({}).length; // 0
```

Pre-ECMA 5:

```
function isEmpty(obj) {
    for(var prop in obj) {
        if(obj.hasOwnProperty(prop))
            return false;
    }

    return true;
}
```

jQuery:

```
jQuery.isEmptyObject({}); // true
```

lodash:

```
_.isEmpty({}); // true
```

Underscore:

```
_.isEmpty({}); // true
```

[Source](http://stackoverflow.com/questions/679915/how-do-i-test-for-an-empty-javascript-object)

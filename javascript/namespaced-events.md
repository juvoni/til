#Namespaced Events Jquery

How do you unbind that one in a safe way that won't accidentally unbind other click handlers? Namespaced events!

Instead of just click as the name of the event, you can use click.namespace.
```
$("#element")
  .on("click.myNamespace", function() { 
     console.log("doSomething");
   });
```
Now you can use .off() with that exact event name to unbind just it.
```
$("#element").off("click.myNamespace");
```

[Source](https://css-tricks.com/namespaced-events-jquery/)

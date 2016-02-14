#Measure Function Performance

The Performance.now() method returns a DOMHighResTimeStamp, measured in milliseconds, accurate to one thousandth of a millisecond.

##Example
```
var t0 = performance.now();
doSomething();
var t1 = performance.now();
console.log("Call to doSomething took " + (t1 - t0) + " milliseconds.")
```

Unlike other timing data available to JavaScript (for example Date.now), the timestamps returned by Performance.now() are not limited to one-millisecond resolution. Instead, they represent times as floating-point numbers with up to microsecond precision.

Also unlike Date.now, the values returned by Performance.now() always increase at a constant rate, independent of the system clock (which might be adjusted manually or skewed by software like NTP).

[Source](https://developer.mozilla.org/en-US/docs/Web/API/Performance/now)

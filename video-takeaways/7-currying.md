## Function currying

> Currying is the process of taking a function that accepts some number of arguments, then creating a new version of that function that can accept an "incomplete" argument list. When given too few arguments, the curried function returns a new function that accepts the remaining arguments

```javascript
function addCurried(a, b) {
  if (typeof b !== "undefined") return a + b;
  else
    return function(c) {
      return a + c;
    };
}
```

## Reference

- [Currying Functions in JavaScript](https://codepen.io/Universalist/post/currying-functions-in-javascript)

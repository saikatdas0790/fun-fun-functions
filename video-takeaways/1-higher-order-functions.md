## Functions are values

```javascript

let someFunction = function(someParameter) {
    // Do work
    return someValue;
}

```

## The Filter method - Array.prototype.filter()

> Creates a new array with all elements that pass the test implemented by the provided function

```javascript

let words = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];

const result = words.filter(word => word.length > 6);

```

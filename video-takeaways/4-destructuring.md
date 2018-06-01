## Destructuring assignment

> The destructuring assignment syntax is a JavaScript expression that makes it possible to unpack values from arrays, or properties from objects, into distinct variables.

### Array Destructuring

```javascript

let foo = ['one', 'two', 'three'];

let [one, two, three] = foo;

```

### Object Destructuring

```javascript

let o = {p: 42, q: true};
let {p, q} = o;

```

### Default Values

> A variable can be assigned a default, in the case that the value unpacked from the object is undefined.

```javascript

var {a = 10, b = 5} = {a: 3};

```
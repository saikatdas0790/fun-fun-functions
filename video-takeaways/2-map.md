## Arrow Functions

> Define the entire body of a method inline. Pass in the parameters and get the return value.

```javascript

let someFunction = (x => x/2);

```

## Array Map function - Array.prototype.map()

```javascript

let materials = [
  'Hydrogen',
  'Helium',
  'Lithium',
  'Beryllium'
];

console.log(materials.map(material => material.length));

```
## ES6 Importing Styles

ECMAScript 6 provides several styles of importing:

### Default import

```javascript
import localName from "src/my_lib";
```

### Namespace import

> imports the module as an object (with one property per named export).

```javascript
import * as my_lib from "src/my_lib";
```

### Named imports

```javascript
import { name1, name2 } from "src/my_lib";
```

> You can rename named imports:

```javascript
// Renaming: import `name1` as `localName1`
import { name1 as localName1, name2 } from "src/my_lib";

// Renaming: import the default export as `foo`
import { default as foo } from "src/my_lib";
```

### Empty import

> only loads the module, doesn’t import anything. The first such import in a program executes the body of the module.

```javascript
import "src/my_lib";
```

There are only two ways to combine these styles and the order in which they appear is fixed; the default export always comes first.

### Combining a default import with a namespace import

```javascript
import theDefault, * as my_lib from "src/my_lib";
```

### Combining a default import with named imports

```javascript
import theDefault, { name1, name2 } from "src/my_lib";
```

## Named exporting styles: inline versus clause

There are two ways in which you can export named things inside modules.

> On one hand, you can mark declarations with the keyword export.

```javascript
export var myVar1 = ···;
export let myVar2 = ···;
export const MY_CONST = ···;

export function myFunc() {
    ···
}
export function* myGeneratorFunc() {
    ···
}
export class MyClass {
    ···
}
```

> On the other hand, you can list everything you want to export at the end of the module (which is similar in style to the revealing module pattern).

```javascript
const MY_CONST = ···;
function myFunc() {
    ···
}

export { MY_CONST, myFunc };
```

> You can also export things under different names:

```javascript
export { MY_CONST as FOO, myFunc };
```

### Reference

* [Modules basics](http://exploringjs.com/es6/ch_modules.html#sec_basics-of-es6-modules)
* [Importing and Exporting in Detail](http://exploringjs.com/es6/ch_modules.html#sec_importing-exporting-details)
* [JavaScript Modules: A Beginner’s Guide](https://medium.freecodecamp.org/javascript-modules-a-beginner-s-guide-783f7d7a5fcc)

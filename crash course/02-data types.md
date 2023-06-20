<h1 align="center"> Data Types </h1>

we got String, Numbers, BigInt, Boolean, null, undefined.

```js
const name = 'cheng xiaoshi'; // String
const age = 30; // numbers
const grade = 92.5; // there are no float or double in javascript so its just numbers
const bigNumber = 12345678901234567890n;  // BigInt, can append the 'n' suffix to an integer literal
const anotherBigNumber = BigInt('98765432109876543210'); // or use 'BigInt()'
const isLibir = true; // boolean (true or false)
const x = null; // basically empty, something but nothing in it
const y = undefined; // defining undefined, funny
let z; // this gonna be undefined as well

// well how can you check what variable has which data types
// we use

console.log(typeof name); // typeof will give you information about the data types
```

oh, then you tried to do 

```js
const x = null;

console.log(typeof x); // output: object
```

in javascript, when you use the **'typeof'** operator with **'null'**, it incorrectly returns **'object'**. This is because in the early days of JavaScript, **'null'** was implemented as a 32-bit value representing a null pointer to an object. Due to a limitation in the language design, the **'typeof'** operator for **'null'** was defined to return **'object'**. However, **'null'** is not actually an object.

to check if a value is **'null'** you can use an equality comparison,

```js
const x = null;

console.log(x === null); // output: true
```

in this case we can compare the value to **'null'** to determine if it is indeed **'null'**.


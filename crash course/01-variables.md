<h1 align="center"> Variables </h1>

there are var, let and const

```js
var age = 16; // number
let message = 'libir'; // string
const = true; // boolean
```

## var
**'var'** has global scopes, can be accessed from anywhere, but can lead to conflicts if another variable with the same name is declared elsewhere, so avoid using this.

## let
**'let'** has block scopes, can only be accessed within the block of code where they are defined. unlike 'var' and 'const', you can reassign the value

```js
let age = 14;
age = 15;

console.log(age);
```

## const
**'const'** also has block scopes, like **'let'**, but they cannot be reassigned once a value is assigned to them. **'const'** is useful for declaring constant or values that are not intended to change.

then that begs the questions, when should you use **'let'** and **'const'**?
always use **'const'** unless you know you're gonna reassign the value, this makes your code more robust.(i learn this word when watching some video about rust(not joking))
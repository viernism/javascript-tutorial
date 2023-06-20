<h1 align="center"> Functions </h1>

reusable blocks of code, u can use it to perform a similiar action

it is the fundamental building block of js, allows you to organize and modularize your code

```js
function add(a, b) {
  return a + b;
}

// invoking the function and storing the result
const sum = add(2, 3);
console.log(sum); // output: 5
```

what if we remove the stuff inside paranthesis

```js
function add(a, b) {
  return a + b;
}

// invoking the function and storing the result
const sum = add();
console.log(sum); // output: NaN
```

what this mean is Not a Number(NaN)

you can set default values on the parameter

```js
function add(a = 3, b = 3) {
  return a + b;
}

console.log(add()); // output: 6
```

you can also just console.log inside the function but its better to use return

we can also turn this into an arrow function, instead of **'function'** we can use **'variables'** instead

```js
const add = (a = 3, b = 3) => a + b;

console.log(add()); // Output: 6
```

what's nice about this is that if its just one expression, we dont have any variables being assigned or any other lines hapenning, we dont need to use curly braces, we dont even need the return we can just **'console.log'**. 

if you only had 1 parameter, you dont even need the paranthesis

```js
const add = num1 => num1 + 5;

console.log(add(5)); // you can just pass 1 value here!
```

its great to use arrow functions with foreach not only because of the readibility but also concise syntax compared to traditional function expressions

```js
const numbers = [1, 2, 3, 4];

// using a regular function
numbers.forEach(function (number) {
  console.log(number * 2);
});
// output: 2 4 6 8

// vs

// using an arrow function
numbers.forEach((number) => console.log(number * 2));
// output: 2 4 6 8
```

now isn't that pretty? now a little bit more complex use

```js
const users = [
  { name: 'Samuel', age: 30 },
  { name: 'Jasmine', age: 25 },
  { name: 'Nate', age: 35 }
];

// using a regular function
users.forEach(function (user) {
  if (user.age > 30) {
    console.log(`${user.name} is over 30 years old.`);
  } else {
    console.log(`${user.name} is 30 years old or younger.`);
  }
});
/* output:
Samuel is 30 years old or younger.
Jasmine is 30 years old or younger.
Nate is over 30 years old.
*/

// using an arrow function
users.forEach((user) => {
  if (user.age > 30) {
    console.log(`${user.name} is over 30 years old.`);
  } else {
    console.log(`${user.name} is 30 years old or younger.`);
  }
});
/* output:
Samuel is 30 years old or younger.
Jasmine is 30 years old or younger.
Nate is over 30 years old.
*/

```




<h1 align="center"> Strings and String methods </h1>


## concatenation

basically combining strings together, this is the old ways.

```js
const age = 15;

const message = 'I am ' + age + ' years old.';

console.log(message); // output: 'I am 15 years old.'
```

## template string

better way to concatenate string in javascript, enclosed in backticks instead of single or double quotes

```js
const firstName = 'John';
const lastName = 'Pork';

const fullName = `My Name is ${firstName} ${lastName}`;

console.log(fullName); // output: 'John Pork'
```

you also can get the number of characters from a string

```js
const name = 'John Pork';

console.log(name.length); // we dont need paranthesis () for property
```

if we want to change the case we can do

```js
const name = 'John Pork';

console.log(name.toUpperCase()); // change to uppercase
```

or lower case

```js
const name = 'John Pork';

console.log(name.toLowerCase()); // change to lower case
```

you can also do where you want to start your string using **'substring'**

```js
const name = 'John Pork';

console.log(name.substring(0, 4)); // output: 'John'
```

you can also use multple property

```js
const name = 'John Pork';

console.log(name.substring(0, 4).toUpperCase()); // output: 'JOHN'
```

we can also split each characters using **'split'**

```js
const name = 'John Pork';

console.log(name.substring(0, 4).split('')); // output: ["J", "o", "h", "n"]
```

will be really handy if you want to make an array

```js
const list = 'linux, arch, ubuntu, debian, nixos, templeos';

console.log(list.split(', ')); // output: ["linux", "arch", "ubuntu", "debian"...]
```


<h1 align="center"> Conditionals </h1>

your basic conditional statement, if, else if, and else

**'if'**

```js
const age = 18;

if (age >= 18) {
  console.log("ur an adult"); // if true execute btw its youre iknowitsjustforfunny
}

```

**'if'** with **'else'**

```js
const age = 18;

if (age >= 18) {
  console.log("ur an adult"); // if true execute
} else {
  console.log("minor"); // if false execute this instead
}
```

**'else if'** 

```js
const grade = 85;

if (grade >= 90) {
  console.log("A"); // executed if true
} else if (grade >= 80) {
  console.log("B"); // executed if first condition isnt true
} else if (grade >= 70) {
  console.log("C"); // executed if first twwo condition isnt true
} else {
  console.log("D"); // executed if all previous conditions are false 
}
```

**'&& (AND)'**

```js
const age = 25;
const hasLicense = true;

if (age >= 18 && hasLicense) {
  console.log("You are eligible to drive."); // executed if both true
} else {
  console.log("You are not eligible to drive."); // executed if any false
}
```

**'|| (OR)'**

```js
const isWeekend = true;
const isHoliday = false;

if (isWeekend || isHoliday) {
  console.log("It's time to relax!"); // executed if at least one condition is true
} else {
  console.log("Keep up the good work!"); // executed if any false
}
```

**'! (NOT)'**

```js
const isLoggedOut = true;

if (!isLoggedOut) {
  console.log("Welcome back!"); // executed if false
} else {
  console.log("Please log in to continue."); // executed if true
}
```

how does one looks with everything?

```js
const temperature = 28;
const isRaining = false;
const isWeekend = true;

if ((temperature > 25 && temperature < 30) || (isRaining && isWeekend)) {
  console.log("It's a good day to stay indoors."); // executed if any of the conditions are true
} else if ((temperature >= 30 && !isRaining) || (temperature >= 25 && isWeekend)) {
  console.log("It's a great day for outdoor activities."); // executed if any of the conditions are true and the previous conditions are false
} else {
  console.log("The weather is moderate."); // if all conditions false, execute
}
```

forgot to mention there are also ternary operators, basically a shorthand if statement, used a lot to assign variables based on a condition

```js
const isLoggedIn = true;
const greeting = isLoggedIn ? "Welcome back!" : "Please log in.";

console.log(greeting); // output: "Welcome back!"
```

you can even use switch to evaluate the condition

```js
const fruit = "apple";
let message;

switch (fruit) {
  case "apple":
    message = "It's a tasty apple!";
    break;
  case "banana":
    message = "It's a ripe banana!";
    break;
  default:
    message = "Unknown fruit!";
}

console.log(message);
```

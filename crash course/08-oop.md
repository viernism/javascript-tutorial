<h1 align="center"> OOP </h1>

so there are this things called construction function, that are used to create and initialize objects based on a blueprint or a class(using prototype or es6 class)

```js
// constructor function
function Person(name, age) {
  this.name = name;
  this.age = age;
}

// instantiate object || creating objects
const person1 = new Person("Cheng Xiaoshi", 21);
const person2 = new Person("Lu Guang", 17);

console.log(person1); // output: Person { name: 'Cheng Xiaoshi', age: 23 }

// if you want to output just the name you can do this
console.log(person2.name); // output: Person { name: 'Lu Guang'}
```

we can also use methods inside the constructor which is just another function

```js
function Person(name, age) {
  this.name = name;
  this.age = age;
  
  this.greet = function() {
    console.log(`Hello, my name is ${this.name} and I'm ${this.age} years     old.`);
  };

  this.changeName = function(newName) {
    this.name = newName;
  };

  this.changeAge = function(newAge) {
	this.age = newAge;
  };
}

// instantiate object || creating objects
const person = new Person("Cheng Xiaoshi", 21);
person.greet(); // output: "Hello, my name is Cheng Xiaoshi and I'm 21 years old."

person.changeName("Lu Guang");
person.changeAge(17);
person.greet(); // output: "Hello, my name is Lu Guang and I'm 17 years old."
```

what if you want to pass a date not as a string but to a date object?

```js
function Person(name, age, dob) {
  this.name = name;
  this.age = age;
  this.dob = new Date(dob);
  
  this.getBirthYear = function() {
    return this.dob.getFullYear();
  };

  this.getName = function(newName) {
    return `${this.name}`;
  };
}

// instantiate object || creating objects
const person1 = new Person('Cheng Xiaoshi', 21, '4-15-1980');
const person2 = new Person('Lu Guang', 17, '10-24-1974');

console.log(person1.getBirthYear()); // output: 1980
console.log(person1.getName()); // output: Cheng Xiaoshi
```

you can also use only the month and the day like this

```js
function Person(name, age, dob) {
  this.name = name;
  this.age = age;
  this.dob = new Date(dob);
  
  this.getBirthMonthAndDay = function() {
    const month = this.dob.toLocaleString('default', { month: 'long' });
    const day = this.dob.getDate();
    return `${month} ${day}`;
  };

  this.getName = function() {
    return `${this.name}`;
  };
}

// instantiate object || creating objects
const person1 = new Person('Cheng Xiaoshi', 21, '4-15-1980');
const person2 = new Person('Lu Guang', 17, '10-24-1974');

console.log(person1.getBirthMonthAndDay()); // output: "April 15"
console.log(person2.getBirthMonthAndDay()); // output: "October 24"
console.log(person1.getName()); // output: "Cheng Xiaoshi"
console.log(person2.getName()); // output: "Lu Guang"
```

so lets talk about prototype, because this way is not the efficient way to define methods for objects in javascripts

```js
function Person(name, age, dob) {
  this.name = name;
  this.age = age;
  this.dob = new Date(dob);
}

Person.prototype.getBirthMonthAndDay = function() {
  const month = this.dob.toLocaleString('default', { month: 'long' });
  const day = this.dob.getDate();
  return `${month} ${day}`;
};

Person.prototype.getName = function() {
  return this.name;
};

// instantiate object || creating objects
const person1 = new Person('Cheng Xiaoshi', 21, '4-15-1980');
const person2 = new Person('Lu Guang', 17, '10-24-1974');

console.log(person1.getBirthMonthAndDay()); // output: "April 3"
console.log(person2.getBirthMonthAndDay()); // output: "March 6"
console.log(person1.getName()); // output: "Cheng Xiaoshi"
```

so with es6 classes were added to js, with classes it does the exact same thing but just prettier so its called syntactic sugar

```js
class Person {
  constructor(name, age, dob) {
    this.name = name;
    this.age = age;
    this.dob = new Date(dob);
  }

  getBirthMonthAndDay() {
    const month = this.dob.toLocaleString('default', { month: 'long' });
    const day = this.dob.getDate();
    return `${month} ${day}`;
  }

  getName() {
    return this.name;
  }
}

// instantiate object || creating objects
const person1 = new Person('Cheng Xiaoshi', 23, '4-3-1980');
const person2 = new Person('Lu Guang', 17, '3-6-1974');

console.log(person1.getBirthMonthAndDay()); // output: "April 3"
console.log(person2.getBirthMonthAndDay()); // output: "March 6"
console.log(person1.getName()); // output: "Cheng Xiaoshi"
```

they added this(i think) so that other that come to learn this language wouldnt have to deal with prototypes(annoying)

i prefer classes tho, easier to read and more organized



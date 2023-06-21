<h1 align="center"> Object Literals </h1>

basically a collection of key-value pairs, each key is a unique identifier(property) that maps to a value, this allows you to define objects directly without the need for a specific object constructor

```js
const person = {
  firstName: 'John',
  lastName: 'Pork',
  age: 35,
  city: 'London'
};
```

you can access the properties of an object using dot notation or bracket notation

```js
const person = {
  firstName: 'John',
  lastName: 'Pork',
  age: 35,
  city: 'London'
};

console.log(person.firstName); // output: 'John'
console.log(person['lastName']); // output: 'Pork'
```

you can modify the values of object properties or add new properties dynamically

```js
const person = {
  firstName: 'John',
  lastName: 'Pork',
  age: 35,
  address: {
    street: '456 Elm St',
    city: 'London',
    state: 'England',
    postalCode: 'SW1A 1AA'
  },
};

console.log(person); // Output: { firstName: 'John', lastName: 'Pork', age: 35, city: 'London' }

person.age = 31; // modify the value of an existing property
person.gender = 'Pig Hybrid'; // add a new property

console.log(person); // Output: { firstName: 'John', lastName: 'Pork', age: 31, city: 'London', gender: 'Pig Hybrid' }
```

wait how can we access a single value only? we got you

```js
const person = {
  firstName: 'John',
  lastName: 'Pork',
  age: 35,
  hobbies: ['travels, instalive, post'],
  address: {
    street: '456 Elm St',
    city: 'London',
    state: 'England',
    postalCode: 'SW1A 1AA'
  },
};

console.log(person.firstName); // output: { firstName: 'John' }
console.log(person.address.city); // output: { city: 'London' }
```

we can also "PULL" the object with a variable

```js
const person = {
  firstName: 'John',
  lastName: 'Pork',
  age: 35,
  hobbies: ['travels, instalive, post'],
  address: {
    street: '456 Elm St',
    city: 'London',
    state: 'England',
    postalCode: 'SW1A 1AA'
  },
};

const { firstName, lastName, address: { city}} = person;

console.log(city); // output: { city: 'London'}
```

<h1 align="center"> Arrays of Objects </h1>

you're probably gonna deal a lot with arrays that has object literals inside like this:

```js
const books = [
  { 
    title: 'Lord of the Mysteries',
    author: 'Chen Dong',
    year: 2018
  },
  {
    title: "Omniscient Reader's Viewpoint",
    author: 'Sing Shong',
    year: 2015
  },
  {
    title: 'Shiguang Dailiren',
    author: 'Zi Chan Bao Zeng',
    year: 2020
  },
  {
    title: "Return of the Blossoming Blade",
    author: 'Sleepyslyfox',
    year: 2019
  },
];

console.log(books); // im too lazy to do an output just do it man
console.log(books[0].title); // output: 'Lord of the Mysteries'

// for each loop
books.forEach(book => {
  console.log(`Title: ${book.title}, Author: ${book.author}`);
}); // output: Title: Lord of the Mysteries, Author: Chen Dong
//             Title: Omniscient Reader's Viewpoint, Author: Sing Shong
//             Title: Shiguang Dailiren, Author: Zi Chan Bao Zeng
//             Title: Return of the Blossoming Blade, Author: Sleepyslyfox

for (let i = 0; i < books.length; i++) { // loop as many as books there are using length
  console.log(`Title: ${books[i].title}, Author: ${books[i].author}`);
} // output is the same as for each loop

// while loop
let i = 0;
while (i < books.length) { // loop as many as books there are using length
  console.log(`Title: ${books[i].title}, Author: ${books[i].author}`);
  i++;
} // output is the same as for loop

books[3].year = 2023; // modify the year of the fourth book
books[1].rating = 4.8; // add a new 'rating' property to the second book

console.log(books[2]); // output: { title: 'Shiguang Dailiren', author: 'Zi Chan Bao Zeng', year: 2021 }
console.log(books[1]); // output: { title: "Omniscient Reader's Viewpoint", author: 'Sing Shong', year: 2015, rating: 4.8 }
```

so JSON(data format) is used a lot in full stack development, and using API when you sending data to a server, so its very similiar to object literals like when you use laravel and returns a dd, its in json format very familiar

oh yeah we also have **high order array methods** like the for each, map, and filter.
of course there's more

```js
const books = [
  { 
    title: 'Lord of the Mysteries',
    author: 'Chen Dong',
    year: 2018
  },
  {
    title: "Omniscient Reader's Viewpoint",
    author: 'Sing Shong',
    year: 2015
  },
  {
    title: 'Shiguang Dailiren',
    author: 'Zi Chan Bao Zeng',
    year: 2020
  },
  {
    title: "Return of the Blossoming Blade",
    author: 'Sleepyslyfox',
    year: 2019
  },
];

// for each loop
books.forEach(book => {
  console.log(`Title: ${book.title}, Author: ${book.author}`);
}); // output: Title: Lord of the Mysteries, Author: Chen Dong
//             Title: Omniscient Reader's Viewpoint, Author: Sing Shong
//             Title: Shiguang Dailiren, Author: Zi Chan Bao Zeng
//             Title: Return of the Blossoming Blade, Author: Sleepyslyfox

// using map to create a new array of book titles
const bookTitles = books.map(book => book.title);
console.log(bookTitles); // output: ['Lord of the Mysteries', "Omniscient Reader's Viewpoint", 'Shiguang Dailiren', 'Return of the Blossoming Blade']

// using filter to find books published after 2017
const recentBooks = books.filter(book => book.year > 2017);
console.log(recentBooks); 
// Output: [{ title: 'Lord of the Mysteries', author: 'Chen Dong', year: 2018 }, { title: 'Shiguang Dailiren', author: 'Zi Chan Bao Zeng', year: 2020 }, { title: 'Return of the Blossoming Blade', author: 'Sleepyslyfox', year: 2019 }]
```

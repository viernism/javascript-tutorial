<h1 align="center"> Events </h1>

basically actions that happen in the browser, like moving the mouse, pressing a key, clicking a button

```html
<button id="myButton" class="btn">Please, do not the button</button>
```

if we want to add an event listener we do

```js
const button = document.getElementById('myButton');

button.addEventListener('click', function() {
  console.log('Button clicked!');
});
```

we can also prevent a default behavior

```js
const button = document.getElementById('myButton');

button.addEventListener('click', function(event) {
  event.preventDefault();
  console.log('Button clicked!');
});
```

we can also remove the function and just use an arrow function

```js
const button = document.getElementById('myButton');

button.addEventListener('click', (event) => {
  event.preventDefault();
  console.log('Button clicked!');
});
```

we can also access the target element that triggered the event in this case which is the button

```js
const button = document.getElementById('myButton');

button.addEventListener('click', (event) => {
  event.preventDefault();
  console.log(event.target.className); // to get class name
  console.log(event.target.id); // to get id
});
```

now lets do something kinda cool

```js
const button = document.getElementById('myButton');

// click event handler
button.addEventListener('click', function(event) {
  console.log('Button clicked!'); // log message to the console
  button.textContent = 'Clicked!'; // change button text content
  button.style.backgroundColor = 'red'; // change button background color
});

// mouse enter event handler
button.addEventListener('mouseenter', function(event) {
  console.log('Mouse entered button!'); // log message to the console
  button.style.fontSize = '20px'; // change button font size
});

// mouse leave event handler
button.addEventListener('mouseleave', function(event) {
  console.log('Mouse left button!'); // log message to the console
  button.style.fontSize = '16px'; // reset button font size
});

```

now if you're kinda confused on how to use multiple element each uniquely, remember we declare them as variable so if that isnt unique idk


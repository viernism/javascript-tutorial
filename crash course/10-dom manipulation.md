<h1 align="center"> DOM Manipulation </h1>

now about the methods, there is a lot of it i'm not gonna explain all of them but

okay so this is the general html we're gonna use

```html
<h1 id="myHeading">DOM Manipulation</h1> 
<button id="myButton">Please, do not the button</button> 
<ul id="myList"> 
	<li>Item 1</li> 
	<li>Item 2</li> 
	<li>Item 3</li> 
</ul>
```

if you want to remove all the list just do

```js
ul.remove();
```

if you want to choose which child property to be removed

```js
ul.firstElementChild.remove();
```

if you want to modify the text content do

```js
ul.lastElementChild.textContent = 'Item 2';
```

oh you want to choose the second one? its like a node list starts from 0

```js
ul.children[1].innerText = 'Item 1';
```

so.. whats the different between innerText and textContent?

well lets say you have something like this 

```html
<div id="myDiv" style="display: none;">
  Hello <span style="display: none;">world!</span>
</div>
```

so textContent will return the whole content even the nested one inside the span but innerText wouldnt

```js
const divElement = document.getElementById('myDiv');

console.log(divElement.textContent); // output: Hello world!
console.log(divElement.innerText);   // output: Hello
```

we also have innerHTML that deals with HTML markup

```html
<div id="myDiv">
  <h1>Title</h1>
  <p>Paragraph 1</p>
</div>
```

we can make a new h2 heading and a new p paragraph

```js
const divElement = document.getElementById('myDiv');

console.log(divElement.innerHTML);
// output: <h1>Title</h1><p>Paragraph 1</p>

divElement.innerHTML = '<h2>New Title</h2><p>New Paragraph</p>';
```

we can also modify the css in real time using js

```html
<div id="myDiv">Hello, World!</div>
```

why? you can use function to make this dynamically in real time using events

```js
const divElement = document.getElementById('myDiv');

divElement.style.color = 'red';
divElement.style.backgroundColor = 'yellow';
divElement.style.fontSize = '20px';
```
<h1 align="center"> DOM Selection </h1>

okay- there is not gonna be a lot of list because there is a lot of dom selection but i'll show you the most common one

### single element

single element means that even if you had like 1000 container, its only gonna select one

okay if you want to select the element with the specified id and assigns it to the **'element'** variable

```html
<container id="container">
```

you should use **'getElementById'**

```js
const element = document.getElementById('myElementId');

console.log(element);
```

if you want to selects all the elements that has a specified class name 

```html
<div class="header">
```

if you want to select a single element

```html
<h1>Hi</h1>
```

you should use **'querySelector'**

```js
const element = document.querySelector('h1');

console.log(element);
```

### multiple element

if you want to select more than one thing

you should use **'querySelectorAll'**

```html
<p>test 1</p>
<p>test 2</p>
<p>test 3</p>
```

to select all of it the output would be like a node list so you can run array methods in it

```js
const elements = document.querySelectorAll('p');

console.log(elements);

// output:
// NodeList(3) [p, p, p]0: p1: p2: plength: 3[[Prototype]]: NodeList
```

and theres this old ways the output is on HTMLCollection but you cannot run array methods in it, you have to convert it to array first

```html
<p class="item">test 1</p>
<p class="item">test 2</p>
<p class="item">test 3</p>
```

the old way is **'getElementbyClass'**

```js
const elements = document.getElementsByClassName('item');

console.log(elements);

// output:
// 1. HTMLCollection(3) [p.item, p.item, p.item]
// 0: p.item
// 1: p.item
// 2: p.item
// length: 3
// [[Prototype]]: HTMLCollection
```

if you want to do it by tag instead just change it to Tag

```js
const elements = document.getElementsByTagName('p');

console.log(elements);
```

so the most common one is **'querySelector'**, **'querySelectorAll'**, sometimes **'getElementById'**

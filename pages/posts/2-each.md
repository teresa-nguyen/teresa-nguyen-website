---
title: All the Different Ways to Go Through a List in JavaScript
date: 2022/4/09
description: Understanding all the different ways to go through a list in JavaScript.
tag: javascript
author: Teresa
---

# All the Different Ways to Go Through a List in JavaScript

There are many ways to go through an array list in JavaScript. I want to share some that I found while learning:

<ol>
  <li>
      The `for` loop is the first one that I learn. This loop allows the flexibility to set the starting point, the endpoint, and how much to move between each item. Read more about the `for` loop [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for).

```js
const array = [1, 2, 3]

for (let i = 0; i < array.length; i++) {
  console.log(array[i])
}

// expected output:
// 1
// 2
// 3
```

  </li>
  <li>
  The second way is the `forEach()` method on the array. Unlike the `for` loop, we do not need to set the starting position, the endpoint, or how much to move between each element. Because of this, we lose the flexibility of the `for` loop. The `forEach()` method will go through every item, moving up one index at a time. This is useful if this is the behavior that you want since you're writing less! Read more about the `forEach()` method [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach).

```js
const array = [1, 2, 3]

array.forEach((element) => console.log(element))

// expected output:
// 1
// 2
// 3
```

  </li>
  <li>
  The third way is to use a library like Underscore and Lodash. These popular libraries provide a useful method called `each()`, which acts similarly to `forEach()`. Read more about `each()` [here](https://underscorejs.org/#each) and [here](https://lodash.com/docs/#forEach).

```js
import _ from 'underscore'

const array = [1, 2, 3]

_.each(array, (element) => console.log(element))

// expected output:
// 1
// 2
// 3
```

  </li>
  <li>
  Lastly, I learned that ES6 provides a new way to go through an array, called the `for...of` loop. I haven't had a chance to use this much, but you can read more about it [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...of).

```js
const array1 = ['a', 'b', 'c']

for (const element of array1) {
  console.log(element)
}

// expected output:
// 1
// 2
// 3
```

  </li>
</ol>

There are many ways to go through an array. Use the one you like best for your situation!

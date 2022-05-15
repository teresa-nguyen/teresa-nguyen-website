---
title: How to Copy an Object in JavaScript
date: 2022/4/16
description: Learn the different ways to copy an object in JavaScript.
tag: javascript
author: Teresa
---

# How to Copy an Object in JavaScript

I recently found out that you can't simply assign an object to another variable to copy it. The two variables will end up pointing to the same object! Fortunately, there are many ways to create a new copy of an object in JavaScript. Here are the ways I found:

1. The first way I learned was the `Object.assign()` method. Learn more about it [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/assign).

```js
const object1 = { name: 'John' }

const object2 = Object.assign({}, object1)
object2.name = 'Scott'

console.log(object1.name) // John
console.log(object2.name) // Scott
```

2. The second way is similar to the first but uses the ES6 spread operator. Learn more about it [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax).

```js
const object1 = { name: 'John' }

const object2 = { ...object1 }
object2.name = 'Scott'

console.log(object1.name) // John
console.log(object2.name) // Scott
```

3. Lastly, you can use libraries like Underscore or Lodash for the clone method. Learn more about it [here](https://underscorejs.org/#clone)

```js
const object1 = { name: 'John' }

const object2 = _.clone(object1)
object2.name = 'Scott'

console.log(object1.name) // John
console.log(object2.name) // Scott
```

I hope these help you learn how to create newly copied objects without affecting your existing object.

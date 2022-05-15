---
title: Understanding Equality in JavaScript
date: 2022/4/23
description: Learn the difference between '==' and '===' in JavaScript.
tag: javascript
author: Teresa
---

# Understanding Equality in JavaScript

Understanding equality in JavaScript is complex! I recently learned that using `===` is the safest way to check equality in JavaScript; `==` has tripped me up so many times, but what is the difference between the two?

```js
1 === '1' // false
1 == '1' // true
```

`===`, also known as strict equality, checks the two values if they are the same or not. It's that simple. While `==`, also known as abstract equality, actually tries to convert the second value that it is comparing to be the same type as the first value before comparing the two.

In our above example, `===` checks the number `1` against the string `'1'`, which are not the same. Therefore, returning false.

While `==` tries to convert the second value. The string `'1'` will be converted to the number `1` before being compared against the first value (the number `1`). Once converted, the two values are now the number `1` when compared, which returns true.

I hope this explains the weird behavior of `==` and helps you avoid making mistakes!

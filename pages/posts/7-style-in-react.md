---
title: How to Style in React
date: 2022/5/14
description: Understanding the className and style properties in React.
tag: css,react
author: Teresa
---

# How to Style in React

When I first learned how to style in HTML, I used the `class` and `style` properties. In `React`, we use the same properties, but they are slightly different.

In React, we use the `className` property instead of the `class` property. This is done because `class` means something else in JavaScript, a blueprint for creating objects. Besides the name, they both behave the same. `className` takes in a string of CSS class names.

```html
<!-- html -->
<div class="myClass"></div>
```

```jxs
// jsx
<Component className="myClass"></Component>
```

The other property is `style`. In React, it is also called `style`, but it behaves a little differently. Instead of taking a string seperated by a `;`, it takes in an object instead, with the style name as the key and the value as strings or numbers. The key in the style object is also camelCase, so remember to convert the style name!

```html
<!-- html -->
<div style="padding-left: 12px; position: absolute"></div>
```

```jsx
// jsx
<Component style={{ paddingLeft: 12, position: 'absolute' }}></Component>
```

Because `React` uses `jsx`, we must understand these differences when working in `jsx` vs `html`.

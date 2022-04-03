---
title: Learning About Controlled Inputs in React
date: 2022/4/2
description: Understanding controlled inputs and why we should use them.
tag: react
author: Teresa
---

# Learning About Controlled Inputs in React

Form elements in HTML (`<input>`, `<textarea>`, and `<select>`) maintain their own state in the browser and will update based on user input. However, in React, state is kept in the state property within the component and are updated with setState(). The browser input state and the React state may not be the same value.

Controlled input solves this by making React act as our source of truth.

The value of the input will be set by the value of the React state, and any update on the input by the user will trigger setState to change the React state.

```jsx
import { useState } from 'react';

function MyInput() {
  const [value, setValue] = useState('');
  const onChange = (event) => {
    setValue(event.target.value);
  };

  return (
    <>
      <div>My input value: {value}</div>
      <input value={value} onChange={onChange} />
    </>
  );
}
```


An input form element whose value is controlled by React in this way is called a "controlled component".
# How to set up testing

## To set it up

### Create a __tests__ folder

### Install jest

```bash
npm install --save-dev jest @testing-library/react
```

### Install jest-dom

```bash
npm i @testing-library/jest-dom
```

Apparently theres a difference if you trigger `jest` or `react-scripts test`.

I'll use both for now.

## how to use it

### Import Dependencies

In your test files, start by bringing in what you need:

```js
import React from 'react';
import { render } from '@testing-library/react';
```

And don't forget the component you're testing:

```js
import Button from './Button';
```

### Write Test Cases

To test something, you use it() blocks. Here's an example:

```js
it('matches snapshot', () => {
  const {asFragment} = render(<Button>Click</Button>)  
  expect(asFragment()).toMatchSnapshot();
});
```

This test checks if the button looks like it's supposed to.

### Run Tests

When you run npm test, it'll check all your tests and tell you how they did. With these steps, you're ready to start testing your React components with Jest and React Testing Library!

# react-layout-effect

Tiny package dedicated to an isomorphic `useLayoutEffect`.

More info: https://github.com/reduxjs/react-redux/pull/1444

## Usage

```ts
import { useLayoutEffect } from 'react-layout-effect'

const MyComponent = () => {
  useLayoutEffect(() => {
    console.log('hi')
  })
}
```

The "hi" message is only logged when 1+ of these is true:
  - `window.document.createElement` exists
  - using a bundler that supports ".native.js" overrides

The warning message [thrown by React](https://github.com/facebook/react/issues/14927) is avoided in SSR environments.

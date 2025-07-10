# hooks

## Overview

This repository contains a collection of custom React hooks designed to simplify common tasks and enhance your development experience. These hooks are lightweight, efficient, and easy to integrate into your projects.

## Features

- **`useMobile`**: Detect if the user is on a mobile device.
- **`useMounted`**: Check if a component is mounted.
- **`useCallbackRef`**: Create a stable callback reference.
- **`useLazyRef`**: Lazily initialize a ref.
- **`useDebouncedCallback`**: Debounce a callback function.
- **`useMediaQuery`**: Match media queries.

## Installation

Install the package via npm:

```bash
npm install @snipplets/hooks
```

## Usage

Import and use the hooks in your React components:

```typescript
import { useMobile, useMounted, useCallbackRef, useLazyRef, useDebouncedCallback, useMediaQuery } from '@snipplets/hooks';

const MyComponent = () => {
  const isMobile = useMobile();
  const isMounted = useMounted();
  const callbackRef = useCallbackRef(() => console.log('Callback invoked'));
  const lazyRef = useLazyRef(() => ({ initialized: true }));
  const debouncedCallback = useDebouncedCallback(() => console.log('Debounced callback'), 300);
  const matchesMediaQuery = useMediaQuery('(max-width: 768px)');

  return (
    <div>
      {isMobile ? 'You are on a mobile device' : 'You are not on a mobile device'}
      {isMounted && <p>The component is mounted</p>}
      <button ref={callbackRef}>Click me</button>
      <p>{lazyRef.current.initialized ? 'Ref initialized' : 'Ref not initialized'}</p>
      <button onClick={debouncedCallback}>Debounced Button</button>
      <p>{matchesMediaQuery ? 'Media query matches' : 'Media query does not match'}</p>
    </div>
  );
};
```

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or features.

## License

This project is licensed under the MIT License.
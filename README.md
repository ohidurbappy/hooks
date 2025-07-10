# hooks

## Overview

This repository contains a collection of custom React hooks designed to simplify common tasks and enhance your development experience. These hooks are lightweight, efficient, and easy to integrate into your projects.

## Features

- **`useMobile`**: Detect if the user is on a mobile device.
- **`useMounted`**: Check if a component is mounted.

## Installation

Install the package via npm:

```bash
npm install @snipplets/hooks
```

## Usage

Import and use the hooks in your React components:

```typescript
import { useMobile, useMounted } from '@snipplets/hooks';

const MyComponent = () => {
  const isMobile = useMobile();
  const isMounted = useMounted();

  return (
    <div>
      {isMobile ? 'You are on a mobile device' : 'You are not on a mobile device'}
      {isMounted && <p>The component is mounted</p>}
    </div>
  );
};
```

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or features.

## License

This project is licensed under the MIT License.
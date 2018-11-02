# react-filecore

Adapter to connect React and FileCore.

## Setup

Typically you'll want to mount FileCore at the root of your application.

```typescript
import * as React from 'react'
import * as ReactDom from 'react-dom'
import { FileCoreProvider } from 'react-filecore'

import { App } from './App'
import { manager } from './filecore'

const appRoot = document.getElementById('app-root')

ReactDom.render(
  <FileCoreProvider manager={manager}>
    <App />
  </FileCoreProvider>,
  appRoot
)
```

## Usage

Simply wrap whatever needs FileCore

```typescript
import * as React from 'react'
import { FileCore } from 'react-filecore'

export const AwesomeForm = () => (
  <FileCore>
    {({ files, addFile }) => ({
      /* Form Stuff */
    })}
  </FileCore>
)
```

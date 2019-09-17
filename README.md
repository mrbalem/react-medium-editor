# react-medium-editor

React wrapper for [medium-editor](https://github.com/daviferreira/medium-editor)

### Demo

[http://wangzuo.github.io/react-medium-editor](http://wangzuo.github.io/react-medium-editor)

### Installation

```sh
npm install react-medium-editor --save
```

### Usage

```javascript
// load theme styles with webpack
import React, { useState } from 'react';
require('medium-editor/dist/css/medium-editor.css');
require('medium-editor/dist/css/themes/default.css');

// ES module
import Editor from 'react-medium-editor';

// CommonJS enviroment
// var Editor = require('react-medium-editor').default;

cons App = () => {

  const [InitialEstate, getInitialState] = useState("Fusce dapibus, tellus ac cursus commodo")

  const handleChange = text => {
        getInitialState(text);
  }
  
  return (
        <div>
            <h1>react-medium-editor</h1>
            <h3>Html content</h3>
            <div>{InitialEstate}</div>

            <h3>Editor #1 (&lt;pre&gt; tag)</h3>
            <Editor
                tag="pre"
                text={InitialEstate}
                onChange={getInitialState}
                options={{ toolbar: { buttons: ['bold', 'italic', 'underline'] } }}
            />

            <h3>Editor #2</h3>

            <Editor
                text={InitialEstate}
                onChange={handleChange}
            />
        </div>
    )

}

export default App;
```

### Import Component

    ```javascript
      
      import App from './App'
      
      //for use component
      <App></App>
    
    ```

### License

MIT

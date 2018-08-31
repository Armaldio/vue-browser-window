# vue-browser-window

> Control your window the Vue way!

# Usage

## Installation

### Using yarn

`yarn add vue-browser-window`

### Using npm

`npm i --save vue-browser-window`

## Usage

First import the component:
```js
import VueBrowserWindow from 'vue-browser-window';
```

Add it to you vue model
```js
export default {
    components: {
        BrowserWindow: VueBrowserWindow
    }
}
```

Finally, wrap you app with the component
```html
<template>
  <browser-window @wheel="event = 'wheel'" @resize="event = 'resize'">
    <div id="app"></div>
  </browser-window>
</template>
```

Summary:
```html
<template>
  <browser-window @wheel="event = 'wheel'" @resize="event = 'resize'">
    <div id="app">
      Last event: {{ event }}
    </div>
  </browser-window>
</template>

<script>
  import VueBrowserWindow from '../../';

  export default {
    name      : 'app',
    components: {
      BrowserWindow: VueBrowserWindow
    },
    data () {
      return {
        event: ''
      };
    },
  };
</script>
```
From: [demo/src/App.vue](demo/src/App.vue)

## Todo
- [x] Support all window events

> Do not hesitate to submit your request for a new feature or a change, or directly a PR! Help is greatly appreciated!

## License

This project is licensed under [MIT License](http://en.wikipedia.org/wiki/MIT_License)

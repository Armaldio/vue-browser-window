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

<style>
</style>

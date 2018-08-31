<template>
    <div>
        <slot></slot>
    </div>
</template>

<script>
  export default {
    name : 'vue-browser-window',
    props: {},

    data () {
      return {
        events: [
          'abort',
          'animationcancel',
          'animationend',
          'animationiteration',
          'auxclick',
          'blur',
          'change',
          'click',
          'close',
          'contextmenu',
          'dblclick',
          'error',
          'focus',
          'gotpointercapture',
          'input',
          'keydown',
          'keypress',
          'keyup',
          'load',
          'loadend',
          'loadstart',
          'lostpointercapture',
          'mousedown',
          'mousemove',
          'mouseout',
          'mouseover',
          'mouseup',
          'pointercancel',
          'pointerdown',
          'pointerenter',
          'pointerleave',
          'pointermove',
          'pointerout',
          'pointerover',
          'pointerup',
          'reset',
          'resize',
          'scroll',
          'select',
          'selectionchange',
          'selectstart',
          'submit',
          'touchcancel',
          'touchmove',
          'touchstart',
          'transitioncancel',
          'transitionend',
          'wheel',
        ]
      };
    },
    mounted () {
      for (let i = 0; i < this.events.length; i++) {
        let event     = this.events[i];
        window[`on${event}`] = () => this.$emit(event);
      }
    }
  };
</script>

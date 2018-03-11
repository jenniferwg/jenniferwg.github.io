<template>
  <div id="app">
    <Content/>
  </div>
</template>

<script>
import Content from './components/Content'

export default {
  name: 'App',
  components: {
    Content
  }
}
</script>

<style lang="scss">
  @import './assets/styles/_variables';

  #app {
    font-family: 'Work Sans', sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    margin-left: 12vw;
    margin-top: 30vh;
  }

  body {
    background-color: $pink; 
  }

  mark {
    background-color: $yellow;
    font-style: italic;
  }
</style>

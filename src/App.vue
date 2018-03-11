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

<style>
#app {
  font-family: 'Work Sans', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin-left: 12vw;
  margin-top: 30vh;
}
body {
  background-color: #ffefeb; 
}
mark {
  background-color: #ffe7b0;
  font-style: italic;
}
</style>

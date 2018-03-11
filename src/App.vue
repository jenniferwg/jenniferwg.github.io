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
  }

  html {
    font-size: calc(8px + (20 - 8)*(100vw - 375px)/ (1920 - 375));
  }

  body {
    background-size: 3.2rem 3.2rem;
    background-image: linear-gradient(to right, $pink 1px, transparent 1px), linear-gradient(to bottom, $pink 1px, transparent 1px);
  }

  mark {
    background-color: $yellow;
    font-style: italic;
    padding-right: 0.6rem;
  }

  a {
    color: $vivid-pink;
    text-decoration: none;
    position: relative;
  }

  a:hover {
    font-style: italic;
    cursor: text;
    transition: all 0.3s;
  }

  a:after {
    display: block;
    position: absolute;
    left: -1px;
    bottom: 0;
    width: 0;
    height: 110%;
    background-color: $yellow;
    content: '';
    transform-origin: left;
    transition: width 0.3s ease;
    z-index: -1;
  }

  a:hover:after {
    width: 120%;
  }
</style>

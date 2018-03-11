<template>
  <div class="hello">
    <h1>{{ title }}</h1>
    <h2 v-html="description"></h2>
    <ul>
      <li>Github</li>
      <li>Linkedin</li>
      <li>Contact</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      title: 'Hi, I\'m Jennifer Wang.',
      description: 'Lorem ipsum dolor sit amet, <mark>consectetur</mark> adipiscing elit. Sed sit amet elementum nisl, eget finibus nulla. Sed egestas libero a est viverra, <mark>quis laoreet erat</mark> lacinia. Aliquam in magna pulvinar, fringilla lectus et, dapibus orci.',
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import '../assets/styles/_variables';

  h1 {
    font-weight: normal;
    font-size: 3.2rem;
  }

  h2 {
    font-family: 'Lato', sans-serif;
    font-weight: 100;
    line-height: 2.2rem;
    font-size: 1.5rem;
    max-width: 60vw;
  }

  ul {
    position: absolute;
    bottom: 12vh;
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin-right: 6vw;
    cursor: crosshair;
    position: relative;
  }

  li:after {
    display: block;
    position: absolute;
    left: 0;
    bottom: -10px;
    width: 0;
    height: 10px;
    background-color: $dark-blue;
    content: "";
    -webkit-transition: all 0.3s;
    -moz-transition: all 0.3s;
    -o-transition: all 0.3s;
    transition: all 0.3s;
    height:2px;
  }

  li:hover:after {
    width: 100%;
    height:2px;
  }
</style>

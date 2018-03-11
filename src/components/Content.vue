<template>
  <div class="content">
    <div class="term">{{ term }}</div>
    <div class="term-tag">{{ tag }}</div>
    <ol class="definitions">
      <li v-for="(def, index) in definitions" :key="index">
        <div v-html="def"></div>
      </li>
    </ol>
    <ul class="links">
      <li v-for="link in links" :key="link.type">
        <a :href="link.url">{{ link.type }}</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Content',
  data () {
    return {
      term: 'Jennifer Wang',
      tag: '/ JE-ni-fer WANG / n.',
      definitions: [
        'A human passionate about <mark>connecting</mark> fellow humans through beautiful products.',
        'Full-stack software engineer at <a href="https://affinity.co/">Affinity</a>, with a background in <mark>user-focused</mark> marketing and design.',
        'East coast transplant newly based in <mark>San Francisco</mark> - exploring, learning and getting involved.'
      ],
      links: [
        { type: "Github", url: "https://github.com/jenniferwg"},
        { type: "LinkedIn", url: "https://www.linkedin.com/in/jenniferwg"},
        { type: "Contact", url: "mailto:jennifer@affinity.co" }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import '../assets/styles/_variables';

  .term {
    font-weight: 600;
    font-size: 3.2rem;
  }

  .term-tag {
    font-weight: normal;
    font-size: 1.8rem;
    margin-bottom: 1.6rem;
  }

  .definitions {
    margin-top: 0.8rem;
    margin-bottom: 6.5rem;
    font-family: 'Lato', sans-serif;
    font-weight: 100;
    line-height: 2rem;
    font-size: 1.4rem;
    max-width: 65vw;
  }

  .definitions > li {
    padding-left: 1rem;
    padding-bottom: 1rem;
  }

  .links {
    position: absolute;
    bottom: 6.4rem;
    list-style-type: none;
    padding: 0;
    font-size: 1.2rem;
  }

  .links > li {
    display: inline-block;
    margin-right: 6vw;
    position: relative;
  }
</style>

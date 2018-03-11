<template>
  <div class="content">
  <transition name="slide-in" appear>
    <div>
      <div class="term">{{ term }}</div>
      <div class="term-tag">{{ tag }}</div>
    </div>
  </transition>
  <transition name="fade-in" appear>
    <div>
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
  </transition>
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
        'A human passionate about <mark>connecting</mark> fellow humans through ' +
        'beautiful products.',
        'Full-stack software engineer at <a href="https://affinity.co/">Affinity</a>, ' +
        'with a background in <mark>user-focused</mark> marketing and design.',
        'East coast transplant engaging in the <mark>San Francisco</mark> community. '
      ],
      links: [
        { type: 'Github', url: 'https://github.com/jenniferwg' },
        { type: 'LinkedIn', url: 'https://www.linkedin.com/in/jenniferwg' },
        { type: 'Contact', url: 'mailto:jennifer@affinity.co' }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import '../assets/styles/_variables';

  .slide-in-enter-active {
    transition: all 1.2s cubic-bezier(0.3, 0.65, 0.7, 0.95);
  }

  .slide-in-enter {
    transform: translateX(-1rem);
    opacity: 0;
  }

  .fade-in-enter-active {
    transition: opacity 2s;
  }

  .fade-in-enter {
    opacity: 0;
  }

  .content {
    max-width: $media-lg;
    margin-left: 8%;
    margin-right: 8%;
    margin-top: 24vh;
  }

  .term {
    font-weight: 600;
    font-size: 3.2rem;
  }

  .term-tag {
    font-weight: normal;
    font-size: 1.4rem;
    margin-bottom: 1.6rem;
  }

  .definitions {
    font-family: 'Lato', sans-serif;
    line-height: 2.2rem;
    font-size: 1.4rem;
    padding-left: 3rem;

    @media only screen and (max-width: $media-md) {
      font-size: 1.6rem;
    }
  }

  .definitions > li {
    padding-left: 1rem;
    padding-bottom: 1rem;
  }

  .links {
    position: absolute;
    bottom: 10vh;
    list-style-type: none;
    padding: 0;
    font-size: 1.2rem;

    @media only screen and (max-width: $media-md) {
      bottom: 30vh;
      font-size: 1.4rem;
    }
  }

  .links > li {
    display: inline-block;
    margin-right: 6vw;
    position: relative;
  }
</style>

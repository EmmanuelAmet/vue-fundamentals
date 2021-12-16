<template>
  <!-- <Greet name="Manuel" hero-name="Walls"/>
  <Greet name="Diana" hero-name="Flash"/>
  <Greet :name="name" :hero-name="channel"/> -->
  <Article id="my-article" title="Title" :likes="38" :isPublished="true"/>

</template>

<script>

import Greet from './components/Greet.vue'
import Article from './components/Article.vue'

export default {
  name: 'App', 
  components: {
    Greet,
    Article,
  },
  data () {
    return {
      name: 'Manuel',
      channel: 'CodeVolution'
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}

</style>

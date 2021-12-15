<template>
  <Greet name="Manuel" hero-name="Walls"/>
  <Greet name="Diana" hero-name="Flash"/>
  <Greet :name="name" :hero-name="channel"/>
</template>

<script>

import Greet from './components/Greet.vue'

export default {
  name: 'App', 
  components: {
    Greet,
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

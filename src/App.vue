<template>
  <!-- <Greet name="Manuel" hero-name="Walls"/>
  <Greet name="Diana" hero-name="Flash"/>
  <Greet :name="name" :hero-name="channel"/> -->
  <!-- <Article id="my-article" title="Title" :likes="38" :isPublished="true"/> -->

  <!-- <h2>{{name}}</h2>
  <ComponentC/>
  <ComponentE />
  <ComponentF /> -->

  <button @click="showPopup = true">Show Popup</button>
  <Popup v-show="showPopup" @close="closePopup"/>
</template>

<script>

import Greet from './components/Greet.vue'
import Article from './components/Article.vue'
import ComponentC from './components/ComponentC.vue'
import ComponentE from './components/ComponentE.vue'
import ComponentF from './components/ComponentF.vue'
import Popup from './components/Popup.vue'

export default {
  name: 'App', 
  components: {
    Greet,
    Article,
    ComponentC,
    ComponentE,
    ComponentF,
    Popup,
  },
  data () {
    return {
      name: 'ManuelAmet',
      channel: 'CodeManuel',
      showPopup: false,
    }
  },
  methods: {
    closePopup(name){
      this.showPopup = false
      console.log('name', name)
    }
  },
  provide() {
    return {
      username: this.name}
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

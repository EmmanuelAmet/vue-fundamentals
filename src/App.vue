<template>
  <button @click="activeTab = 'TabA'">Tab A</button>
  <button @click="activeTab = 'TabB'">Tab B</button>
  <button @click="activeTab = 'TabC'">Tab C</button>

<keep-alive>
<component :is="activeTab" />
</keep-alive>
  <!-- <TabA v-if="activeTab === 'TabA'" />
  <TabB v-if="activeTab === 'TabB'" />
  <TabC v-if="activeTab === 'TabC'" /> -->
</template>

<script>
import ComponentC from './components/ComponentC.vue'
import TabA from './components/Tabs/TabA.vue'
import TabB from './components/Tabs/TabB.vue'
import TabC from './components/Tabs/TabC.vue'

export default {
  name: 'App', 
  components: {
    TabA,
    TabB,
    TabC,
    ComponentC,
  },
  data () {
    return {
      activeTab: 'TabA'
    }
  },
  methods: {}
}
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h4 {
  color: orange;
}
</style>

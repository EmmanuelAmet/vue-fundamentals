<template>
  <Card></Card>
  <Card>
    Card Content
  </Card>
  <Card>
    <h2>Card Content</h2>
  </Card>
  <Card> 
    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSZ0Bvcb06LNaFVCrVUi9uejRCbPDe1xDFafwZ2k-nQqKPsoiPodBce8YajqYgX3S-kEbg&usqp=CAU" alt="">
  </Card>

  <Card>
    <template v-slot:header>
      <h3>Herder</h3>
    </template>
    <template v-slot:default>
          <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSZ0Bvcb06LNaFVCrVUi9uejRCbPDe1xDFafwZ2k-nQqKPsoiPodBce8YajqYgX3S-kEbg&usqp=CAU" alt="">
    </template>
    <template v-slot:footer>
      <button>View Details</button>
    </template>
  </Card>

</template>

<script>
import Card from './components/Card.vue'

export default {
  name: 'App', 
  components: {
    Card,
  },
  data () {
    return {
      name: '',
      location: '',
    }
  },
  methods: {}
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

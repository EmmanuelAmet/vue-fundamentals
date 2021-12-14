<template>
<!-- Event Handing -->
<h2>{{name}}</h2>
<div>
  <button @click="changeName($event), increment(2, $event)">Change name</button>
</div>
<h2>{{count}}</h2>
<div>
  <button v-on:click="increment(10, $event)">Increment</button>
  <button v-on:click="decrement(20)">Decrement</button>
  <button @click="increment(5)">Increment</button>
  <button @click="decrement(5)">Decrement</button>
</div>
</template>

<script>

export default {
  name: 'App', 
  data () {
    return{
      name: 'Manuel',
      count: 0
    }
  },
  methods: {
    changeName(event){
      console.log('Event', event)
      this.name = 'Emmanuel'
    },
    increment(num, event){
      console.log('Event', event)
      this.count += num
    },
    decrement(num){
      this.count -= num
    }
  }
  }
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.underline{
  text-decoration: underline,
}

.promoted{
  font-style: italic;
}

.new {
  color: green;
}

.sold-out {
  color: red;
}
</style>

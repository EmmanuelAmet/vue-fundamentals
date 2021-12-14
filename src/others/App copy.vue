<template>
<!-- Mehtods -->
  <h2>{{ 1+2+2}}</h2>
  <h2>{{44+3+5}}</h2>
  <h2>Add methos {{add(2,4,5)}}</h2>
  <h2>Multiply {{multiply(10)}}</h2>
</template>

<script>

export default {
  name: 'App',
  data () {
    return{
      baseMultiplyier : 5
    }
  },
  methods: {
    add(a, b, c) {
      return a + b + c
    },
    multiply (num){
      return num * this.baseMultiplyier
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

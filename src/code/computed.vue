<template>
<!-- Directives -->
<h2>
  Fullname: {{firstName }} {{lastName}}
</h2>
<h2>computed Fullname: {{fullName}}</h2>
<button @click="items.push({id: 4, title: 'Keyboard', price: 500 })">Add item</button>
<h2>Computed Total: {{total}}</h2>
<h2>Method Total: {{getTotal( )}}</h2>
</template>

<script>

export default {
  name: 'App', 
  data () {
    return{
      firstName: 'Manuel',
      lastName: 'Emmanuel',
      items: [
        {
          id: 1,
          title: 'TV',
          price: 100
        },
        {
          id: 2,
          title: 'Phone',
          price: 200
        },
        {
          id: 3,
          title: 'Laptop',
          price: 300
        }
      ]
    }
  },
  methods: {
    getTotal(){
      return this.items.reduce((total, curr) => (total = total + curr.price), 0)
    }
  },
  computed: {
    fullName(){
      return `${this.firstName} ${this.lastName}`
    },
    total(){
      return this.items.reduce((total, curr) => (total = total + curr.price), 0)
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

label {
  font-weight: bold;
  display: flex;
  margin-bottom: 5px;
}

input + label {
  font-weight: bold;
  display: inline-flex;
  margin-bottom: 20px;
}

input[type='text'],
textarea,
select {
  display: block;
  width: 400px;
  font-size: 14px;
  padding: 6px 12px;
  line-height: 1.42857143;
  color: #555;
  background-color: #fff;
  background-image: none;

}

</style>

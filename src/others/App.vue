<template>

  <div>{{greet}} {{name}}</div>
  <div v-text="channel"></div>
  <div v-html="channel"></div>
  <h2 v-bind:id="headingId">Heading</h2>
  <button v-bind:disabled="isDisable">Bind</button>
  <h3 class="underline">Underline</h3>
  <h2 class="underline" v-bind:class="danger">Status</h2>
  <h2 :class="isPromoted && 'promoted'">Promoted Movie</h2>
  <h2 :class="isSoldOut? 'sold-out' : 'new'">Soldout? movie</h2>
  <h2 :class="['new', 'promoted']">Newly promoted movie</h2>
  <h2 :class="[isPromoted && isSoldOut? 'sold-out' : 'new']">Newly promoted movie</h2>
  <h2 :class="{
    promoted: isPromoted,
    new: !isSoldOut,
    'sold-out': isSoldOut
  }">Object Conditionals</h2>
  <h2 v-bind:style="{
    color: highlightColor,
    'font-size': headerSize + 'px',
    padding: '20px'
    }">Inline style</h2>
    <h2 v-bind:style="headerStyleObject">New Style Object</h2>
    <div v-bind:style="[baseStyleObject, successStyleObject]">Success Style</div>
    <div v-bind:style="[baseStyleObject, dangerStyleObject]">Danger Style</div> -->
    <h2 v-if="num === 0">The number is zero</h2>
  <h2 v-else-if="num > 0">The number is positive</h2>
  <h2 v-else-if="num < 0">The number is negative</h2>
  <h2 v-else>Not a number</h2>

  <template v-if="display">
    <h2>Manuel</h2>
    <h2>Vue is awesome</h2>
    <h2>Cloud is super cool</h2>
  </template>

  <h2 v-show="showElement">Using v-show</h2>

  <h2 v-for="name in names" :key="name.index">{{name}}</h2>
  <h2 v-for="name in fullNames" :key="name.fisrt">{{name.first}} {{name.last}}</h2>

  <div v-for="actor in actors" :key="actor.name">
    <h2>{{actor.name}}</h2>
    <h3 v-for="movie in actor.movies" :key="movie.index">{{movie}}</h3>
  </div>

  <h2 v-for="(value, key, index) in myInfo" :key="value.index">{{value}} {{key}} {{index}}</h2>

  <template v-for="name in names" :key="name">
    <h2 v-if="name === 'Bruce'">{{name}}</h2>
    <hr>
  </template>

</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      names: ['Bruce', 'Diana', 'Manuel', 'Henry', 'Charles'],
      fullNames: [
        {first: 'Manuel', last: 'Patrova'},
        {first: 'Henry', last: 'Mills'},
        {first: 'Florence', last: 'Amet'}
      ],
      actors: [
        {
          name: 'Bervely Jones',
          movies: ['Think like a CEO', 'Rich Dad, Poor Dad']
        },
        {
          name: 'Robert Tims',
          movies: ['No Death, no Life', 'The young Rich']
        }
      ],
      myInfo: {
        name: 'Manuel',
        channel: 'CodeManipulation',
        curse: 'Vue 3'
      },
      num: 'm',
      display: true,
      showElement: true,
      name: 'Manuel',
      greet: 'Hioshv;odhgvo',
      channel: '<b>CodeWithManuel</b>',
      headingId: 'heading',
      isDisable: false,
      status: 'danger',
      isPromoted: true,
      isSoldOut: true,
      highlightColor: 'orange',
      headerSize: 50,
      headerStyleObject:{
        color: 'orange',
        fontSize: '50px',
        padding: '24px'
      },
      baseStyleObject:{
        padding: '10px',
        fontSize: '50px'
      },
      successStyleObject:{
        color: 'green',
        backgroundColor: 'lightgreen',
        border: '1px solid green',
        padding: '20px'
      },
      dangerStyleObject:{
        color: 'darkred',
        backgroundColor: 'red',
        border: '1px solid darkred'
      }
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

<template>
  <div id="app">
    <button v-if="route == 'Statues'" @click="goToPaintings()">Paintings</button>
    <button v-if="route == 'Paintings'" @click="goToStatues()">Statues</button>
    <Paintings v-if="route == 'Paintings'"/>
    <Statues v-if="route == 'Statues'"/>
  </div>
</template>

<script>

import Paintings from './components/Paintings.vue'
import Statues from './components/Statues.vue'

export default {
  name: 'App',
  components: {
    Paintings,
    Statues
  },
  data() {
    return {
      route: "Paintings"
    }
  },
  methods: {
    
goToPaintings(){
  this.route = 'Paintings';
},
goToStatues(){
  this.route = 'Statues';
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
</style>

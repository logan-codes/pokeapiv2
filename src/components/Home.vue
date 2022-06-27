<template>
  <div class="Home">
    
    <ul>
      <li v-for="pokemon in pokemons" :key="">{{ pokemon.name }}</li>
    </ul>

  </div>
</template>

<script>

import Urls from '@/scripts/Urls'




export default {
  name: 'HomePoke',

  data(){
    return{
      pokemons:[],
    }   
  },

  created(){
    fetch(Urls.pokemon)
    .then(response => response.json()
    .then(data => { this.pokemons = data}))
  }
}



</script>


<style>

</style>

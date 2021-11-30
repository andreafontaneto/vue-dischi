<template>
  
  <main class="py-5">

    <div class="container">
      <div v-if="loaded === true" class="row">

        <Album
        v-for="(album, index) in albums" 
        :key="index"
        :album="album"/>
      
      </div>

      <Loading v-else/>

    </div>
  
  </main>

</template>

<script>

import axios from 'axios';
import Album from "./Album.vue";
import Loading from "./Loading.vue";

export default {
  name: 'Main',

  components: {
    Album,
    Loading
  },

  props: {
    genreSelected: String
  },

  computed: {

    filteredAlbums(){
      // se la stringa del genere è una stringa vuota restituisce tutti gli album
      if(this.genreSelected === ''){
        return this.albums
      }
      // ALTRIMENTI...
      // salvo in una costante un nuovo array filtrato 
      const albumFiltered = this.albums.filter( album => {
        // farà un "push" SOLO se è vera la condizione del return
        return album.genre === this.genreSelected;
      })
      // restituisce il nuovo array filtrato come risultato di filteredAlbums()
      return albumFiltered;
    }

  },

  data(){
    return{
      albums: [],
      loaded: false
    }
  },

  methods: {

    getAPI(){
      axios.get("https://flynn.boolean.careers/exercises/api/array/music")
        .then( r => {
          //console.log(r);
          //console.log(r.data);
          //console.log(r.data.response);
          this.albums = r.data.response;
          console.log(this.albums)

          this.loaded = true;
        })
        .catch( e => {
          console.log(e);
        })
    }

  },

  mounted(){
    //console.log(axios);
    this.getAPI();
  }
}
</script>

<style lang="scss" scoped>

@import "../assets/style/vars.scss";

main{
  background-color: $background-color;
  min-height: calc(100vh - 70px);
}

</style>
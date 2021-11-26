<template>
  
  <main class="py-5">

    <div class="container">
      <div v-if="loaded === true" class="row">

        <Album
        v-for="(album, index) in albums" 
        :key="index"
        :album="album"/>
      
      </div>
      
      <div v-else class="text-center my-5 loading">
        <p>LOADING...</p>
      </div>

    </div>
  
  </main>

</template>

<script>

import axios from 'axios';
import Album from "./Album.vue";

export default {
  name: 'Main',

  components: {
    Album
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

  .loading{
    font-size: 50px;
    font-weight: 700;
    color: white;
  }
}

</style>
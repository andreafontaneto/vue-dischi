<template>
  
  <main class="py-5">

    <div class="container">
      <div class="row">
        <Album 
        v-for="(album, index) in albums" 
        :key="index"
        :album="album"/>
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
      albums: []
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
}

</style>
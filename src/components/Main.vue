<template>
  
  <main @changeValue="getGenre" class="py-5">

    <select v-model="selectValue" @change="$emit('changeValue', selectValue)"
    class="form-select" aria-label="Default select example">
      <option selected>Seleziona il genere musicale</option>
      <option value="1">Rock</option>
      <option value="2">Pop</option>
      <option value="3">Jazz</option>
      <option value="4">Metal</option>
    </select>

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

  data(){
    return{
      albums: [],
      loaded: false,
      selectValue: ''
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
    },

    getGenre(value){
      // this.selectValue = value;
      console.log(value);
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
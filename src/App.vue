<template>
  <div>

    <Header @changeGenre="getGenre" />
    <Main :genreSelected="genreSelected"/>

  </div>
</template>

<script>

import Header from "./components/Header.vue";
import Main from "./components/Main.vue";

export default {
  name: 'App',
  components: {
    Header,
    Main
  },

  data(){
    return{
      genreSelected: ''
    }
  },

  methods: {

    getGenre(genre){
      this.genreSelected = genre;
      console.log(this.genreSelected);
    }

  }
}
</script>

<style lang="scss">

@import "./assets/style/vars.scss";
@import "./assets/style/generals.scss";

</style>

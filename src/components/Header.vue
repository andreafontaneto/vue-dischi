<template>
  
  <header class="px-4">
    
    <div class="py-3 logo">
      <img src="../assets/img/spotify-logo.png" alt="spotify-logo">
    </div>

    <div class="col-3">
      <select v-model="genre" @change="$emit('changeGenre', genre)" 
      class="form-select" aria-label="Default select example">
        <option selected>Seleziona il genere musicale</option>
        <option value="Rock">Rock</option>
        <option value="Pop">Pop</option>
        <option value="Jazz">Jazz</option>
        <option value="Metal">Metal</option>
      </select>
    </div>

  </header>

</template>

<script>

export default {
  name: 'Header',

  components: {

  },

  data(){
    return{
      genre: ''
    }
  },

  methods: {

  }

}
</script>

<style lang="scss" scoped>

@import "../assets/style/vars.scss";

header{
  height: 70px;
  background-color: $box-color;
  display: flex;
  justify-content: space-between;
  align-items: center;

  .logo{
    width: 40px;
  }
}

</style>
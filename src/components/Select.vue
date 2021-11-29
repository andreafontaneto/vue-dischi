<template>
  <div class="col-2">
    <select class="form-select" aria-label="Default select example">
      <option selected>Seleziona il genere musicale</option>
      <option value="">{{album.genre}}</option>
      <!-- <option value="1">Rock</option>
      <option value="2">Pop</option>
      <option value="3">Jazz</option>
      <option value="4">Metal</option> -->
    </select>
  </div>
</template>

<script>
export default {
  name: 'Select',

  props:{
    album: Object
  }
}
</script>

<style lang="scss" scoped>

// @import "../assets/style/vars.scss";


</style>
<template>
  <div class="col-3">
    <select v-model="selectValue" @change="$emit('changeValue', valueSelect)" 
    class="form-select" aria-label="Default select example">
      <option value="0" selected>Seleziona il genere musicale</option>
      <option value="1">Rock</option>
      <option value="2">Pop</option>
      <option value="3">Jazz</option>
      <option value="4">Metal</option>
    </select>
  </div>
</template>

<script>
export default {
  name: 'Select',

  props:{
    album: Object
  },

  data(){
    return{
      selectValue: 0
    }
  }
}
</script>

<style lang="scss" scoped>

// @import "../assets/style/vars.scss";


</style>
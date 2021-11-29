<template>
  <div>
    <select class="form-select af-select" aria-label="Default select example">
      <option selected>Seleziona il genere musicale</option>
      <option value="1">Rock</option>
      <option value="2">Pop</option>
      <option value="3">Jazz</option>
      <option value="4">Metal</option>
    </select>
  </div>
</template>

<script>
export default {
  name: 'Select'
}
</script>

<style lang="scss" scoped>

@import "../assets/style/vars.scss";

.af-select{
    width: 300px !important;
    height: 40px !important;
  }

</style>
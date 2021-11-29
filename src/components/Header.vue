<template>
  
  <header class="px-4">
    
    <div class="py-3 logo">
      <img src="../assets/img/spotify-logo.png" alt="spotify-logo">
    </div>

    <select class="form-select af-select" aria-label="Default select example">
      <option selected>Seleziona il genere musicale</option>
      <option value="1">Rock</option>
      <option value="2">Pop</option>
      <option value="3">Jazz</option>
      <option value="4">Metal</option>
    </select>

  </header>

</template>

<script>
export default {
  name: 'Header'
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

  .af-select{
    width: 300px;
    height: 40px;
  }
}

</style>
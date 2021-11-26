<template>
  
  <header>
    <div class="logo">
      <img src="../assets/img/spotify-logo.png" alt="spotify-logo">
    </div>
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
  height: 80px;
  background-color: lighten($main-color, 10%);
  padding: 0 20px;

  .logo{
    width: 40px;
    padding-top: 15px;
  }
}

</style>
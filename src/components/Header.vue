<template>
  
  <header class="px-4">
    <div class="py-3 logo">
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
  height: 70px;
  background-color: lighten($main-color, 10%);

  .logo{
    width: 40px;
  }
}

</style>
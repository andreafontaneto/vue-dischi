<template>
  
  <main>

    <div class="container">

      <Album />
      
    </div>
  
  </main>

</template>

<script>

import Album from "./Album.vue";

export default {
  name: 'Main',

  components: {
    Album
  }
}
</script>

<style lang="scss" scoped>

@import "../assets/style/vars.scss";

main{
  background-color: $main-color;
  height: calc(100vh - 70px);
}

</style>
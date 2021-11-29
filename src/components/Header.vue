<template>
  
  <header class="px-4">
    
    <div class="py-3 logo">
      <img src="../assets/img/spotify-logo.png" alt="spotify-logo">
    </div>

    <Select />

  </header>

</template>

<script>

import Select from "./Select.vue";

export default {
  name: 'Header',

  components: {
    Select
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
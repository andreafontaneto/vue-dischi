<template>

  <div class="col text-center mx-3 p-4 album-box ">

    <div class="mx-auto album-img">
      <img :src="album.poster" :alt="album.title">
    </div>
              
    <div class="py-3 album-title">
      <p>{{album.title}}</p>
    </div>
              
    <div class="album-info">
      <p class="ai-author">{{album.author}}</p>
      <p class="ai-year">{{album.year}}</p>
    </div>

  </div>



</template>

<script>
export default {
  name: 'Album',

  props:{
    album: Object
  }
}
</script>

<style lang="scss" scoped>

@import "../assets/style/vars.scss";

.album-box{
  background-color: $box-color;
  margin-bottom: 20px !important;

  .album-img{
    width: 150px;
    height: 150px;
  }

  .album-title{
    font-size: 25px;
    color: white;
    text-transform: uppercase;
  }

  .album-info{
    color: grey;
        
    .ai-author{
      font-size: 20px;
      margin-bottom: 0 !important;
    }

    .ai-year{
      font-size: 15px;
      margin-bottom: 0 !important;
    }
  }
}

</style>
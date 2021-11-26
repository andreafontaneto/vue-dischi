<template>

  <div class="col text-center p-4 album-box ">

    <div class="mx-auto album-img">
      <img src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="img">
    </div>
              
    <div class="py-3 album-title">
      <p>TITOLO</p>
    </div>
              
    <div class="album-info">
      <p class="ai-author">Autore</p>
      <p class="ai-year">ANNO</p>
    </div>

  </div>



</template>

<script>
export default {
  name: 'Album'
}
</script>

<style lang="scss" scoped>

@import "../assets/style/vars.scss";

.album-box{
  background-color: lighten($main-color, 30%);
  margin: 100px 20px 0 20px;

  .album-img{
    width: 150px;
    height: 150px;
  }

  .album-title{
    font-size: 30px;
    color: white;
  }

  .album-info{
    color: grey;
        
    .ai-author{
      font-size: 30px;
    }

    .ai-year{
      font-size: 20px;
    }
  }
}

</style>
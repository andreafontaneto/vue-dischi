<template>
  
  <main>
    <div class="container">
      <div class="row">

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

      </div>
    </div>
  </main>

</template>

<script>

import Album from "./Album.vue";

export default {
  name: 'Main',

  component: {
    Album
  }
}
</script>

<style lang="scss" scoped>

@import "../assets/style/vars.scss";

main{
  background-color: $main-color;
  height: calc(100vh - 70px);

  .album-box{
    //width: calc((100% / 5) - 40px);
    // height: 400px;
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
}

</style>
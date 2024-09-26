<script>
export default {
  data() {
    return {
      
    }
  }
}
</script>

<template>
  <div class="container">
    <div class="gallery">
      <div class="left-side">
        <div class="lu"></div>
        <div class="ld"></div>
      </div>
      <div class="centrale">
        <div class="c">
          <div class="bottoni">
            <button class="btn btn-light">Lfestyle</button>
            <button class="btn btn-light">Stories</button>
            <button class="btn btn-light">Travel</button>
          </div>

        </div>
      </div>
      <div class="right-side">
        <div class="ru"></div>
        <div class="rd"></div>
      </div>
      
     
    </div>
  </div>

</template>

<style scoped>
.gallery{
  height: 500px;
  border: 1px dashed dodgerblue;
  display: flex;
}

.c {
  background-image: url(../assets/img/best-places.webp);
  background-size: cover;
  border-radius: 10px;
  height: 100%;
  width: 675px;
  margin-left: 10px;
  margin-right: 10px;
  position: relative;
}
.lu{
  background-image: url(../assets/img/anime-fashion.webp);
  background-size: cover;
  border-radius: 10px;
  background-color: green;
  height: calc(100% / 2 - 5px);
  width: 300px;
  margin-bottom: 10px;
}
.ld{
  background-image: url(../assets/img/travel-alone.webp);
  background-size: cover;
  border-radius: 10px;
  background-color: green;
  height: calc(100% / 2 - 5px);
  width: 300px;

}
.ru {
  background-image: url(../assets/img/music-love.webp);
  background-size: cover;
  border-radius: 10px;
  background-color: green;
  height: calc(100% / 2 - 5px);
  width: 300px;
  margin-bottom: 10px;

}
.rd{  
  background-image: url(../assets/img/visit-france.webp);
  background-size: cover;
  border-radius: 10px;
  background-color: green;
  width: 100%;
  height: calc(100% / 2 - 5px);
  width: 300px;
}








</style>
<script>
export default {
  data() {
    return {
      messages:[
        {
          nome:'demo',
          data:'December25,2022',
          text:'Fashion Trend Now A Day'
        },
        {
          nome:'demo',
          data:'December26,2022',
          text:'Traveling Alone Is Awesome'
        }, {
          nome:'demo',
          data:'December25,2022',
          text:'Place For A Road Trip'
        }, {
          nome:'demo',
          data:'December25,2022',
          text:'Music The Love Of My Life'
        }, {
          nome:'demo',
          data:'December26,2022',
          text:'Reason To Visit France'
        },
      ]
      

    }
  }
}
</script>

<template>
  <div class="container">
    <div class="gallery">
      <div class="left-side">
        <div class="lu">
          <div class="bottoni">
            <button class="btn btn-light me-2">Lifestyle</button>
            <button class="btn btn-light me-2">Fashion</button>
          </div>
          <p>ciao</p>
          <p>{{ messages[0].name }}</p>

        </div>
        <div class="ld">
          <div class="bottoni">
            <button class="btn btn-light me-2">Stories</button>
            <button class="btn btn-light me-2">Travel</button>
          </div>
        </div>
      </div>
      <div class="centrale">
        <div class="c">
          <div class="bottoni">
            <button class="btn btn-light me-2">Lifestyle</button>
            <button class="btn btn-light me-2">Stories</button>
            <button class="btn btn-light">Travel</button>
          </div>

        </div>
      </div>
      <div class="right-side">
        <div class="ru">
          <div class="bottoni">
            <button class="btn btn-light me-2">Culture</button>
            <button class="btn btn-light me-2">Lifestyle</button>
          </div>
        </div>
        <div class="rd">
          <div class="bottoni">
            <button class="btn btn-light me-2">Lifestyle</button>
            <button class="btn btn-light me-2">Travel</button>
          </div>
        </div>
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
  position: relative;

}
.ld{
  background-image: url(../assets/img/travel-alone.webp);
  background-size: cover;
  border-radius: 10px;
  background-color: green;
  height: calc(100% / 2 - 5px);
  width: 300px;
  position: relative;


}
.ru {
  background-image: url(../assets/img/music-love.webp);
  background-size: cover;
  border-radius: 10px;
  background-color: green;
  height: calc(100% / 2 - 5px);
  width: 300px;
  margin-bottom: 10px;
  position: relative;


}
.rd{  
  background-image: url(../assets/img/visit-france.webp);
  background-size: cover;
  border-radius: 10px;
  background-color: green;
  width: 100%;
  height: calc(100% / 2 - 5px);
  width: 300px;
  position: relative;

}

.bottoni{
  position: absolute;
  top: 20px;
  transform: translateX(-50%, -50%);
}

p{
  position: absolute;
  font-size: 12px;
  color: white;
}








</style>
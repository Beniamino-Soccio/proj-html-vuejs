<script>
export default {
  components: {
 
  },
  data() {
    return {
     currentIndex: 0,
     newUpdates:[
      {
        img:'/src/assets/img/healthy-foods-150x150.webp',
        hours: '05.32',
        text: 'THE BEST HEALTHY FOODS'
      },
      {
        img:'/src/assets/img/rice-ball-150x150.webp',
        hours: '05.37',
        text: 'HYGENIC RECEIPE TO PREPARE RICE'
      },
      {
        img:'/src/assets/img/winter-150x150.webp',
        hours: '05.29',
        text: 'THE BEST WINTER OUTFITS'
      },
      {
        img:'/src/assets/img/meal-time-150x150.webp',
        hours: '05.35',
        text: 'THE BEST TIME TO HAVE A MEAL'
      },
    ]
    }
  },
  methods:{
      nextUpdate(){
        this.currentIndex = (this.currentIndex + 1) % this.newUpdates.length;
      },
      prevUpdate(){
        if (this.currentIndex > 0) {
        this.currentIndex--;
      } else {
        this.currentIndex = this.newUpdates.length - 1;
      }
      }
    }
}
</script>

<template>
    <div class="news-updates d-flex align-items-center py-2">
      <div class="container">
        <div class="row">
          <div class="col-2 updates-text d-flex justify-content-center align-items-center py-2">
            <p class="m-0">NEW UPDATES</p>
          </div>
          <!--Current New Updates-->
          <div class="current-new-updates col-7 d-flex align-items-center p-0 gap-3 text-white fw-bold">
            <img :src="newUpdates[currentIndex].img" :alt="newUpdates[currentIndex].text">
            <div><span>{{ newUpdates[currentIndex].hours }}</span></div>
            <div><span>{{ newUpdates[currentIndex].text }}</span></div>
          </div>
          <!--Social Icon-->
          <div class="social-icons col-3 d-flex justify-content-end align-items-center">
            <div @click="prevUpdate"><i class="bi bi-caret-left-fill"></i></div>
            <div @click="nextUpdate"><i class="bi bi-caret-right-fill me-5"></i></div>
            <a href="#"><i class="bi bi-facebook"></i></a>
            <a href="#"><i class="bi bi-twitter-x"></i></a>
            <a href="#"><i class="bi bi-instagram"></i></a>
            <a href="#"><i class="bi bi-youtube"></i></a>
          </div>
        </div>
      </div>
    </div>
</template>

<style lang="scss" scoped>
@use 'bootstrap/scss/bootstrap.scss' as *;

.bi-caret-left-fill, .bi-caret-right-fill{
  cursor: pointer;
}

.current-new-updates{
  height: 50px;
}

.current-new-updates img{
  height: 100%;
}

.updates-text{
  background-color: #545454;
  color: white;
  font-weight: bold;
  height: 50px;
}

.news-updates{
  background-color: #BF1D2E;
  height: 50px;
}

.social-icons i{
  background-color: white;
  border-radius: 50%;
  padding: 5px 8px;
  color: #BF1D2E;
  font-size: 15px;
  margin-right: 10px;
}
</style>
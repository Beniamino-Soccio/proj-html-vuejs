<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';

import 'swiper/css/pagination';
import 'swiper/css/navigation';



// import required modules
import { Pagination, Navigation } from 'swiper/modules';

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Pagination, Navigation],
      cardList: [
        {
          title: 'Live Ideas You Might Be Anime',
          image: '/src/assets/img/ideas-anime.webp',
          date: 'December 26, 2022'
        },
        {
          title: 'Reasons To Visit France',
          image: '/src/assets/img/visit-france.webp',
          date: 'December 26, 2022'
        },
        {
          title: 'Traveling Alone Is Awesome',
          image: '/src/assets/img/travel-alone-300x200.webp',
          date: 'December 26, 2022'
        },
        {
          title: 'The Best Success Stories',
          image: '/src/assets/img/success-story.webp',
          date: 'December 26, 2022'
        },
        {
          title: 'Places For A Road Trip',
          image: '/src/assets/img/best-places-300x200.webp',
          date: 'December 25, 2022'
        },
        {
          title: 'Music The Love Of My Life',
          image: '/src/assets/img/music-love.webp',
          date: 'December 25, 2022'
        },
        {
          title: 'Fashion Trend Now A Days',
          image: '/src/assets/img/anime-fashion.webp',
          date: 'December 25, 2022'
        },
        {
          title: 'The Best Winter Outfits',
          image: '/src/assets/img/winter.webp',
          date: 'December 26, 2022'
        },
      ]
    };
  },

};
</script>

<template>
  <div class="main-slider">
    <swiper ref="{swiperRef}" :slidesPerView="4" :loop="true" :centeredSlides="false" :spaceBetween="10"
      :navigation="true" :modules="modules" class="mySwiper">
      <swiper-slide class="card" v-for="(card, index) in cardList" :key="index">
        <img :src="card.image" class="card-img-top" alt="">
        <div class="card-body">
          <p class="mb-0 fw-bold title"> {{ card.title }} </p>
          <p class="mb-1 date"> {{ card.date }} </p>
        </div>
      </swiper-slide>
    </swiper>
    <p class="append-buttons"></p>
  </div>
</template>

<style scoped>
#app {
  height: 100%;
}

html,
body {
  position: relative;
  height: 100%;
}

body {
  background: #eee;
  font-family: Helvetica Neue, Helvetica, Arial, sans-serif;
  font-size: 14px;
  color: #000;
  margin: 0;
  padding: 0;
}

.swiper {
  width: 100%;
  height: 100%;
}

.swiper-slide {
  text-align: center;
  font-size: 18px;
  background: #fff;

  /* Center slide text vertically */
  display: flex;
  justify-content: center;
  align-items: center;
}

.swiper-slide img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.swiper {
  width: 100%;
  margin: 20px auto;
}

.append-buttons {
  text-align: center;
  margin-top: 20px;
}

.append-buttons button {
  display: inline-block;
  cursor: pointer;
  color: purple;
  text-decoration: none;
  padding: 4px 10px;
  border-radius: 4px;
  margin: 0 10px;
  font-size: 13px;
}

.title {
  font-size: 14px;
}

.date {
  font-size: 13px;
  color: #545454;
}
.main-slider{
  background-color: #f3f3f3;
  padding: 15px 30px;
}
::v-deep div.swiper-button-next,
::v-deep div.swiper-button-prev {
  color: red;
  font-weight: bold;
  background-color: #fff;
  border-radius: 50%;
  height: 25px;
}
.custom-prev{
  font-size: 26px;
  color: red;
}
.custom-next{
font-size: 26px;
color: red;
}
</style>

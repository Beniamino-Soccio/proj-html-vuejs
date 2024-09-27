<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';

import 'swiper/css/pagination';
import 'swiper/css/navigation';



// import required modules
import { Autoplay, Pagination, Navigation } from 'swiper/modules';

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Autoplay, Pagination, Navigation],
      cardList: [
        {
          title: 'Live Ideas You Might Be Anime',
          image: '/src/assets/img/ideas-anime.webp',
          date: 'December 26, 2022',
          firstTopic: 'Culture',
          secondTopic: 'Stories',
        },
        {
          title: 'Reasons To Visit France',
          image: '/src/assets/img/visit-france.webp',
          date: 'December 26, 2022',
          firstTopic: 'Lifestyle',
          secondTopic: 'Travel',
        },
        {
          title: 'Traveling Alone Is Awesome',
          image: '/src/assets/img/travel-alone-300x200.webp',
          date: 'December 26, 2022',
          firstTopic: 'Stories',
          secondTopic: 'Travel',
        },
        {
          title: 'The Best Success Stories',
          image: '/src/assets/img/success-story.webp',
          date: 'December 26, 2022',
          firstTopic: 'Culture',
          secondTopic: 'Stories',
        },
        {
          title: 'Places For A Road Trip',
          image: '/src/assets/img/best-places-300x200.webp',
          date: 'December 25, 2022',
          firstTopic: 'Lifestyle',
          secondTopic: 'Stories',
          thirdTopic: 'Travel',
        },
        {
          title: 'Music The Love Of My Life',
          image: '/src/assets/img/music-love.webp',
          date: 'December 25, 2022',
          firstTopic: 'Culture',
          secondTopic: 'Lifestyle',
        },
        {
          title: 'Fashion Trend Now A Days',
          image: '/src/assets/img/anime-fashion.webp',
          date: 'December 25, 2022',
          firstTopic: 'Fashion',
          secondTopic: 'Lifestyle',
        },
        {
          title: 'Hygenic receipe to prepare rice',
          image: 'src/assets/img/rice-ball.webp',
          date: 'December 26, 2022',
          firstTopic: 'Food',
        },
        {
          title: 'The Best Time To Have A Meal',
          image: 'https://demo.hasnaindev.com/animetech/wp-content/uploads/2022/12/meal-time.webp',
          date: 'December 26, 2022',
          firstTopic: 'Food',
        },
        {
          title: 'The Best Healty Food',
          image: 'src/assets/img/healthy-foods.webp',
          date: 'December 26, 2022',
          firstTopic: 'Food',
        },
        {
          title: 'The Best Winter Outfits',
          image: '/src/assets/img/winter.webp',
          date: 'December 26, 2022',
          firstTopic: 'Fashion',
        },
        {
          title: "Beginner Photographer's Mistakes",
          image: 'src/assets/img/photographers-mistakes.webp',
          date: 'December 26, 2022',
          firstTopic: 'Fashion',
        },
      ]
    }
  },
}
</script>

<template>
  <div class="custom-prev"><i class="bi bi-caret-left-fill"></i></div>
  <div class="custom-next"><i class="bi bi-caret-right-fill"></i></div>
  <div class="main-slider">
    <swiper ref="{swiperRef}" :slidesPerView="4" :loop="true" :centeredSlides="false" :spaceBetween="10" :navigation="{ nextEl: '.custom-next', prevEl: '.custom-prev' }" :modules="modules" class="mySwiper" :autoplay="{ delay: 5000 }">
      <swiper-slide class="card position-relative" v-for="(card, index) in cardList" :key="index">
        <img :src="card.image" class="card-img-top" alt="">
        <div class="d-flex badges-group position-absolute gap-2">
          <button class="first-topic border-0">{{ card.firstTopic }}</button>
          <button v-if="card.secondTopic" class="second-topic border-0" >{{ card.secondTopic }}</button>
          <button v-if="card.thirdTopic"class="third-topic border-0">{{ card.thirdTopic }}</button>
        </div>
        <div class="card-body p-2">
          <p class="mb-0 fw-bold title"> {{ card.title }} </p>
          <p class="mb-1 date fw-semibold"> {{ card.date }} </p>
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
  position: relative;
}
.bi{
  font-size: 18px;
  color: #bf1d2e;
  background-color: #fff;
  border-radius: 50%;
  height: 35px;
  width: 35px;
  text-align: center;
  line-height: 35px;
  position: absolute;
  top: 480px;
  z-index: 2;
  transition-property: background-color;
  transition-duration: 0.6s;
  cursor: pointer;
}
.bi-caret-left-fill{
  left: 50px;
}
.bi-caret-right-fill{
  right: 50px;
}
.bi:hover{
  color: white;
  background-color: #bf1d2e;
}
.card-body p{
  font-size: 16px;
  cursor: pointer;
}
.card-body p:first-child{
  font-size: 18px;
}
.badges-group{
  top: 10px;
}
.first-topic, .second-topic, .third-topic{
  padding: 2px 15px;
  border-radius: 5px;
}
img{
  height: 300px;
  cursor: pointer;
}
.card-body p:hover, .badges-group button:hover{
  color: #bf1d2e;
}
</style>

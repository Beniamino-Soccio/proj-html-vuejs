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
          date: 'December 26, 2022',
          firstTopic: 'Culture',
          secondTopic: 'Stories'
        },
        {
          title: 'Reasons To Visit France',
          image: '/src/assets/img/visit-france.webp',
          date: 'December 26, 2022',
          firstTopic: 'Lifestyle',
          secondTopic: 'Travel'
        },
        {
          title: 'Traveling Alone Is Awesome',
          image: '/src/assets/img/travel-alone-300x200.webp',
          date: 'December 26, 2022',
          firstTopic: 'Stories',
          secondTopic: 'Travel'
        },
        {
          title: 'The Best Success Stories',
          image: '/src/assets/img/success-story.webp',
          date: 'December 26, 2022',
          firstTopic: 'Culture',
          secondTopic: 'Stories'
        },
        {
          title: 'Places For A Road Trip',
          image: '/src/assets/img/best-places-300x200.webp',
          date: 'December 25, 2022',
          firstTopic: 'Lifestyle',
          secondTopic: 'Stories'
        },
        {
          title: 'Music The Love Of My Life',
          image: '/src/assets/img/music-love.webp',
          date: 'December 25, 2022',
          firstTopic: 'Culture',
          secondTopic: 'Lifestyle'
        },
        {
          title: 'Fashion Trend Now A Days',
          image: '/src/assets/img/anime-fashion.webp',
          date: 'December 25, 2022',
          firstTopic: 'Fashion',
          secondTopic: 'Lifestyle'
        },
        {
          title: 'The Best Winter Outfits',
          image: '/src/assets/img/winter.webp',
          date: 'December 26, 2022',
          firstTopic: 'Fashion'
        },
        {
          title: 'Beginner Photographer\'s Mistakes',
          image: '/src/assets/img/photographers-mistakes.webp',
          date: 'December 26, 2022',
          firstTopic: 'Fashion'
        },
      ]
    };
  },

};
</script>

<template>
  <div class="container">
    <div class="top-post d-flex justify-content-between">
      <h3 class="my-4 fw-bold">FEATURED POST</h3>
      <div class="arrows d-flex position-relative text-center">
        <div class="custom-prev"><i class="bi bi-caret-left-fill position-absolute rounded-circle prev"></i></div>
        <div class="custom-next"><i class="bi bi-caret-right-fill position-absolute rounded-circle next"></i></div>
      </div>
    </div>

    <swiper ref="{swiperRef}" :slidesPerView="3" :loop="true" :centeredSlides="false" :spaceBetween="30"
      :navigation="{ nextEl: '.custom-next', prevEl: '.custom-prev' }" :modules="modules" class="mySwiper">
      <swiper-slide class="card position-relative" v-for="(card, index) in cardList" :key="index">
        <img :src="card.image" class="card-img-top" alt="post's image">
        <button class="first-topic position-absolute border-0"> {{ card.firstTopic }} </button>
        <button class="second-topic position-absolute border-0"> {{ card.secondTopic }} </button>
        <div class="card-body">
          <p class="mb-0 fw-bold title"> {{ card.title }} </p>
          <p class="mb-1 date"> {{ card.date }} </p>
          <p class="lorem"> Lorem ipsum dolor sit amet consectetur, adipisicing elit.</p>
          <button class="btn text-white read-more">Read More</button>
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
  color: black;
  text-decoration: none;
  padding: 4px 10px;
  border-radius: 4px;
  margin: 0 10px;
  font-size: 13px;
}

::v-deep .swiper-button-next,
::v-deep .swiper-button-prev {
  color: black;
}

::v-deep .swiper-pagination-bullet {
  background-color: black;
}

.lorem {
  font-size: 12px;
}

.title {
  font-size: 14px;
}

.date {
  font-size: 13px;
  color: #545454;
}

.read-more {
  background-color: #BF1D2F;
  border-radius: 15px;
  padding: 1px 40px;
}

.read-more:hover {
  background-color: #333333;
}

.first-topic,
.second-topic {
  top: 10px;
  font-size: 16px;
  padding: 0 15px;
  border-radius: 5px;
}

.first-topic:hover {
  color: red;
}

.second-topic:hover {
  color: red;
}

.first-topic {
  left: 25%;
}

.second-topic {
  left: 55%;
}

.arrows i {
  background-color: #333333;
  width: 35px;
  height: 35px;
  top: 20px;
  color: white;
  line-height: 35px;
  cursor: pointer;
  transition-property: background-color;
  transition-duration: 0.6s;
}

i:hover {
  background-color: #BF1D2E;
}

.prev {
  right: 50px;
}

.next {
  right: 0;
}

.card-body,
.card {
  background-color: #F3F3F3;
}
</style>

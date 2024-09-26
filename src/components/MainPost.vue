<script>
import 'bootstrap/dist/js/bootstrap.bundle.min.js';
import 'bootstrap-icons/font/bootstrap-icons.css';

export default {
  data() {
    return {
      activeIndex: 0,
      cardList: [
        {
          title: 'Live Ideas You Might Be Anime',
          image: '/src/assets/img/ideas-anime.webp'
        },
        {
          title: 'Reasons To Visit France',
          image: '/src/assets/img/visit-france.webp'
        },
        {
          title: 'Traveling Alone Is Awesome',
          image: '/src/assets/img/travel-alone-300x200.webp'
        },
        {
          title: 'The Best Success Stories',
          image: '/src/assets/img/success-story.webp'
        },
        {
          title: 'Places For A Road Trip',
          image: '/src/assets/img/best-places-300x200.webp'
        },
        {
          title: 'Music The Love Of My Life',
          image: '/src/assets/img/music-love.webp'
        },
        {
          title: 'Fashion Trend Now A Days',
          image: '/src/assets/img/anime-fashion.webp'
        },
        {
          title: 'The Best Winter Outfits',
          image: '/src/assets/img/winter.webp'
        },
      ]
    }
  }
}
</script>

<template>
  <section class="container py-5">
    <div class="top-post d-flex justify-content-between">
      <h3>FEATURED POSTS</h3>
      <div class="change d-flex gap-3">
        <i class="bi bi-caret-left-square-fill"></i>
        <i class="bi bi-caret-right-square-fill"></i>
      </div>
    </div>
    <div class="py-4 text-center">
      <div class="row">
        <div class="col-4">
          <div class="card">
            <img :src='cardList[0].image' class="card-img-top" alt="immagine">
            <div class="card-body">
              <h5 class="card-title"> {{ cardList[0].title }} </h5>
              <h6>December 26,2022</h6>
              <p class="card-text">Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
              <a href="#" class="btn btn-primary">Read More</a>
            </div>
          </div>
        </div>
        <div class="col-4">
          <div class="card">
            <img :src='cardList[1].image' class="card-img-top" alt="immagine">
            <div class="card-body">
              <h5 class="card-title"> {{ cardList[1].title }} </h5>
              <h6>December 26,2022</h6>
              <p class="card-text">Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
              <a href="#" class="btn btn-primary">Read More</a>
            </div>
          </div>
        </div>
        <div class="col-4">
          <div class="card">
            <img :src='cardList[2].image' class="card-img-top" alt="immagine">
            <div class="card-body">
              <h5 class="card-title"> {{ cardList[2].title }} </h5>
              <h6>December 26,2022</h6>
              <p class="card-text">Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
              <a href="#" class="btn btn-primary">Read More</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.card-body {
  background-color: #F3F3F3;
}

h5 {
  font-size: 19px;
}

h6 {
  color: #757575
}

.btn {
  background-color: #BF1D2F;
  padding: 2px 30px;
  border-radius: 15px;
  border: 0;
}
</style>
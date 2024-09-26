<script>
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
    <h3>FEATURED POSTS</h3>
    <div class="py-4 text-center">
      <div class="row">

        <div v-for="(card, index) in cardList" :key="index" class="card col">
          <img :src='card.image' class="card-img-top" alt="immagine">
          <div class="card-body">
            <h5 class="card-title"> {{ card.title }} </h5>
            <h6>December 26,2022</h6>
            <p class="card-text">Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
            <a href="#" class="btn btn-primary">Read More</a>
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
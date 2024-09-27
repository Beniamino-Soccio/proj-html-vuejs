<script>
export default {
  data() {
    return {
      lifestyleStoriesCard: [
        {
          img: '/src/assets/img/anime-fashion.webp',
          author: 'demo',
          date: 'December 25, 2022',
          title: 'Fashion trend now a days',
          badge: 'Fashion'
        },
        {
          img: '/src/assets/img/best-places-300x200.webp',
          author: 'demo',
          date: 'December 25, 2022',
          title: 'Places for a road trip',
          badge: 'Lifestyle'
        },
        {
          img: '/src/assets/img/ideas-anime.webp',
          author: 'demo',
          date: 'December 25, 2022',
          title: 'Live Ideas you might be anime',
          badge: 'Culture'
        }
    ]
    }
  }
}
</script>

<template>
  <!--Main news-->
  <div class="container mt-5">
    <div class="row">
      <h3 class="p-0">LIFESTYLE & STORIES</h3>
    </div>
    <div class="row box">
      <div class="col box-left ps-0">
        <a href="#"><img src="/src/assets/img/music-love.webp" alt="Music Love"></a>
      </div>

      <div class="col d-flex flex-column">
        <!--lifestyle stories card-->
        <div class="lifestyle-stories-card d-flex align-items-center gap-4" v-for="(card, index) in lifestyleStoriesCard" :key="index">

          <!--Immagine della card-->
          <a href="#"><img class="img-card me-3" :src="card.img" :alt="card.title"></a>

          <!--Badge dell'immagine-->
          <p class="badge-card">{{ card.badge }}</p>

          <!--Info card-->
          <div class="info-card">
            <span class="me-3"><i class="bi bi-person-fill"></i> {{ card.author }}</span>
            <span><i class="bi bi-calendar2-fill"></i> {{ card.date }}</span>
            <p>{{ card.title }}</p>
          </div>
 
        </div>
      </div>
    </div>
  </div>
<div>
</div>
</template>

<style lang="scss" scoped>
@use 'bootstrap/scss/bootstrap.scss' as *;
h3{
  font-weight: bold;
}

.box-left img{
  height: 500px;
  width: 100%;
  cursor: pointer;
}
.img-card{
  object-fit: contain;
  max-width: 200px;
  border-radius: 5px;
  margin-bottom: 25px;
  cursor: pointer;
  
}
.badge-card{
  position: absolute;
  top: 15px;
  left: 15px;
  background-color: white;
  border-radius: 5px;
  padding: 2px 15px;
  font-weight: bold;
  cursor: pointer;
}
.badge-card:hover{
  color: #BF1D2E;
}
.bi{
  font-size: 20px;
}

.box{
  height: 500px;
}

.info-card{
  font-weight: bold;
  span{
    color: #545454;
    cursor: pointer;
  }
  &
  :hover{
    color: #BF1D2E;
  }
}

.lifestyle-stories-card{
  margin-bottom: 25px;
  border-bottom: 1px solid black;
  position: relative;
}
.lifestyle-stories-card:last-child{
  border-color: transparent;
}
// effetto hover
img{
  filter: brightness(50%);
}
img:hover{
  filter: brightness(60%)
}

p{
  cursor: pointer;
}
</style>
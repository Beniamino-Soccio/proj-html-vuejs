<script>
export default {
  data() {
    return {
      isLoading: false,
      selectedCategory: 'ALL',
      lifestyleStoriesCard: [
        {
          img: '/src/assets/img/anime-fashion.webp',
          author: 'demo',
          date: 'December 25, 2022',
          title: 'Fashion trend now a days',
          badge: 'Fashion',
          category: 'LIFESTYLE'
        },
        {
          img: '/src/assets/img/best-places-300x200.webp',
          author: 'demo',
          date: 'December 25, 2022',
          title: 'Places for a road trip',
          badge: 'Lifestyle',
          category: 'LIFESTYLE'
        },
        {
          img: '/src/assets/img/ideas-anime.webp',
          author: 'demo',
          date: 'December 25, 2022',
          title: 'Live Ideas you might be anime',
          badge: 'Culture',
          category: 'STORIES'
        },
        {
          img: '/src/assets/img/music-love.webp',
          author: 'demo',
          date: 'December 25, 2022',
          title: 'Music the Love of my life',
          badge: 'Culture',
          category: 'STORIES'
        }
      ]
    };
  },
  computed: {
    filteredCards() {
      if (this.selectedCategory === 'ALL') {
        return this.lifestyleStoriesCard;
      }
      return this.lifestyleStoriesCard.filter(
        card => card.category === this.selectedCategory
      );
    },
    mainImage() {
      return this.filteredCards[0] || this.lifestyleStoriesCard[0];
    },
    rightSideCards() {
      let rightCards = this.filteredCards.slice(1, 4);
      if (rightCards.length < 3) {
        const remainingCards = this.lifestyleStoriesCard.filter(card => !this.filteredCards.includes(card));
        rightCards = rightCards.concat(remainingCards.slice(0, 3 - rightCards.length));
      }
      return rightCards;
    }
  },
  methods: {
    changeCategory(category) {
      this.isLoading = true; 
      console.log("Loading started...");

      
      setTimeout(() => {
        this.selectedCategory = category;
        this.isLoading = false; 
        console.log("Loading finished...");
      }, 500); 
    }
  }
};
</script>

<template>
  <div class="container mt-5">
    <div class="row">
      <h3 class="p-0">LIFESTYLE & STORIES</h3>      
      <div class="category-buttons my-3">
        <button class="btn category-btn" :class="{ active: selectedCategory === 'ALL' }" @click="changeCategory('ALL')">ALL</button>
        <button class="btn category-btn" :class="{ active: selectedCategory === 'LIFESTYLE' }" @click="changeCategory('LIFESTYLE')">LIFESTYLE</button>
        <button class="btn category-btn" :class="{ active: selectedCategory === 'STORIES' }" @click="changeCategory('STORIES')">STORIES</button>
      </div>
    </div>

    <div class="custom-loader-mask" v-if="isLoading">
      <div class="custom-loader"></div>
    </div>

    <div class="row box position-relative"> 
      <div class="col-lg-7 box-left ps-0">
        <a href="#">
          <img :src="mainImage.img" :alt="mainImage.title" class="main-img">
          <span class="badge-card main-badge">{{ mainImage.badge }}</span>
        </a>
        <div v-if="!isLoading" class="main-info text-white">
          <p class="main-info-text">
            <i class="bi bi-person-fill"></i> {{ mainImage.author }} 
            <i class="bi bi-calendar2-fill"></i> {{ mainImage.date }}
          </p>
          <h5>{{ mainImage.title }}</h5>
        </div>
      </div>

      <div class="col-lg-5 d-flex flex-column">
        <div class="lifestyle-stories-card d-flex align-items-center gap-3" v-for="(card, index) in rightSideCards" :key="index">
          <a href="#"><img class="img-card me-3" :src="card.img" :alt="card.title"></a>
          <div class="info-card text-secondary">
            <span class="badge-card">{{ card.badge }}</span>
            <p><i class="bi bi-person-fill"></i> {{ card.author }} <i class="bi bi-calendar2-fill"></i> {{ card.date }}</p>
            <p>{{ card.title }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>


<style lang="scss" scoped>
@use 'bootstrap/scss/bootstrap.scss' as *;

.custom-loader-mask {
  background: rgba(54, 54, 54, 0.8);
  position: fixed; 
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: 9999; 
}

.custom-loader {
  left: 50%;
  top: 50%;
  position: absolute;
  transform: translate(-50%, -50%);
}

.custom-loader:before {
  border-top: 1em solid #21759b;
  border-right: 1em solid #21759b;
  border-bottom: 1em solid #21759b;
  border-left: 1em solid transparent;
  border-radius: 50%;
  content: '';
  display: block;
  height: 5rem;
  width: 5rem;
  animation: animation 1.1s infinite linear;
}

@keyframes animation {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

h3 {
  font-weight: bold;
}

.box-left {
  position: relative; 
}

.main-badge {
  position: absolute; 
  top: 15px; 
  left: 15px; 
  background-color: white;
  border-radius: 5px;
  padding: 2px 15px;
  font-weight: bold;
  z-index: 1; 
}

.box-left img {
  height: 500px;
  width: 100%;
  cursor: pointer;
  filter: brightness(50%); 
}

.img-card {
  object-fit: contain;
  max-width: 200px;
  border-radius: 5px;
  margin-bottom: 25px;
  cursor: pointer;
}

.badge-card {
  position: absolute;
  top: 15px;
  left: 15px;
  background-color: white;
  border-radius: 5px;
  padding: 2px 15px;
  font-weight: bold;
  cursor: pointer;
}

.text-white {
  color: white; 
}

.text-secondary {
  color: #545454; 
}

.main-info {
  margin-top: 10px;
    position: relative;
    top: -75px;
    left: 10px;
}

.info-card {
  font-weight: bold;
  span {
    color: #545454;
    cursor: pointer;
  }
}

.lifestyle-stories-card {
  margin-bottom: 25px;
  border-bottom: 1px solid black;
  position: relative;
}

.lifestyle-stories-card:last-child {
  border-color: transparent;
}

p {
  cursor: pointer;
}

.my-3 {
    margin-top: 1rem !important;
    margin-bottom: 1rem !important;
    position: relative;
    top: -58px;
    left: 850px;
}

.row {
  margin: -40px;
}

.p-0 {
    padding: 0 !important;
    margin: 10px;
}

.category-buttons {
  display: flex;
  gap: 10px;
}

.category-btn {
  border: 2px solid grey;
  background-color: white;
  color: grey;
  padding: 5px 15px;
  font-weight: bold;
  cursor: pointer;
  transition: all 0.3s ease;
}

.category-btn:hover {
  color: red;
  border-color: red;
}

.category-btn.active {
  color: white;
  background-color: red;
  border-color: red;
}

.main-info-text {
  font-size: 14px; 
  color: #ffffff; 
  margin-bottom: 5px;
}
</style>
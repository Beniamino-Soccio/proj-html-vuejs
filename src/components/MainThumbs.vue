<script>
export default {
  data() {
    return {
      categories: [
        {
          image: 'src/assets/img/anime-fashion.webp',
          title: 'Fashion',
          posts: '3 POSTS',
          link: 'https://demo.hasnaindev.com/animetech/category/fashion/'
        },
        {
          image: 'src/assets/img/success-story.webp',
          title: 'Culture',
          posts: '3 POSTS',
          link: 'https://demo.hasnaindev.com/animetech/category/culture/'
        },
        {
          image: 'src/assets/img/healthy-foods.webp',
          title: 'Food',
          posts: '3 POSTS',
          link: 'https://demo.hasnaindev.com/animetech/category/food/'
        },
        {
          image: 'src/assets/img/visit-france.webp',
          title: 'Lifestyle',
          posts: '4 POSTS',
          link: 'https://demo.hasnaindev.com/animetech/category/lifestyle/'
        },
        {
          image: 'src/assets/img/travel-alone.webp',
          title: 'Stories',
          posts: '4 POSTS',
          link: 'https://demo.hasnaindev.com/animetech/category/stories/'
        },
        {
          image: 'src/assets/img/best-places-300x200.webp',
          title: 'Travel',
          posts: '3 POSTS',
          link: 'https://demo.hasnaindev.com/animetech/category/travel/'
        }
      ]
    }
  }
}
</script>

<template>
  <div class="container-fluid py-5">
    <div class="d-flex justify-content-center g-4">
      <div 
        class="p-2 thumb-card" 
        v-for="(category, index) in categories" 
        :key="index">
        <div class="card h-100 position-relative">
          <a :href="category.link">
            <div class="card-img-overlay d-flex align-items-center justify-content-center">
              <h5 class="card-title text-white text-uppercase">{{ category.title }}</h5>
            </div>
            <img 
              :src="category.image" 
              class="card-img-top" 
              :alt="category.title">
          </a>
          <div class="hover-info">
            <p class="card-text text-center">{{ category.posts }}</p>
          </div>
          <div class="border-box"></div>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>


.thumb-card {
  position: relative;
  flex-basis: 30%;
}

.card-img-overlay {
  background-color: rgba(0, 0, 0, 0.377);
}

.card-title {
  font-size: 1.25rem;
  text-align: center;
}

.card {
  overflow: hidden;
  position: relative;
  cursor: pointer; 
}

.card img {
  transition: transform 0.2s ease; 
  
}

img{}


.card:hover {
  background-color: red; 
}

.card:hover img {
  transform: translateX(3%);
  opacity: 0.4;
}

.hover-info {
  position: absolute;
  bottom: 36px;
  left: 0;
  right: 0;
  color: white;
  text-align: center;
  opacity: 0; 
  transition: opacity 0.3s ease;
  transform: translateX(3%);
}

.card:hover .hover-info {
  opacity: 1; 
}

.border-box {
  position: absolute;
  top: 30px;
  left: 30px;
  right: 30px;
  bottom: 30px;
  border: 2px solid white;
  opacity: 0;
  transition: opacity 0.5s ease;
  transform: translateX(3%);
}

.card:hover .border-box {
  opacity: 1;
  transform: scale(1.05);
}


.card a {
  display: block;
  width: 100%;
  height: 100%;
}

</style>
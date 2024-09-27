<script>
import MainGallery from "./MainGallery.vue";
import MainNews from ".//MainNews.vue";
import MainPost from "./MainPost.vue";
import MainSlider from "./MainSlider.vue";
import MainTrailer from "./MainTrailer.vue";
import MainThumbs from "./MainThumbs.vue";

export default {
  components: {
    MainGallery,
    MainNews,
    MainPost,
    MainSlider,    
    MainTrailer,
    MainThumbs,
  },
  data() {
    return {
      
    }
  }
}
</script>

<template>

<MainSlider />
<MainGallery />
<MainNews />
<div class="banner d-flex justify-content-center align-items-center">
  <div class="container p-0">
    <img src="../assets/img/page-banner-1.webp" alt="">
  </div>
</div>
<MainPost />
<MainTrailer />
<MainThumbs />

</template>

<style scoped>
.banner{
  padding: 30px 0;
  background-color: #f3f3f3;
}
img{
  width: 100%;
  height: 110px;
  border-radius: 5px;
}
</style>
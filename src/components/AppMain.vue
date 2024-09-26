<script>
import MainGallery from "./MainGallery.vue";
import MainNews from ".//MainNews.vue";
import MainPost from "./MainPost.vue";
import MainSlider from "./MainSlider.vue";
import MainThumbs from "./MainThumbs.vue";
import MainTrailer from "./MainTrailer.vue";

export default {
  components: {
    MainGallery,
    MainNews,
    MainPost,
    MainSlider,
    MainThumbs,
    MainTrailer,
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
  <img src="../assets/img/page-banner-1.webp" alt="">
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
.banner img{
  width: 1200px;
  height: 110px;
  border-radius: 5px;
}
</style>
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

<MainGallery />
<MainNews />
<MainPost />
<MainSlider />
<MainTrailer />
<MainThumbs />

</template>

<style scoped>
</style>
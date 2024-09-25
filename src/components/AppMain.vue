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

<MainGallery />
<MainNews />
<MainPost />
<MainSlider />
<MainThumbs />
<MainTrailer />

</template>

<style scoped>
</style>
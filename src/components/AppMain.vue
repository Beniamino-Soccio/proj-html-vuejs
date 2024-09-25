<script>
import MainGallery from "./components/MainGallery.vue";
import MainNews from "./components/MainNews.vue";
import MainPost from "./components/MainPost.vue";
import MainSlider from "./components/MainSlider.vue";
import MainThumbs from "./components/MainThumbs.vue";
import MainTrailer from "./components/MainTrailer.vue";

export default {
  components: {
    MainGallery,
    MainNews,
    MainPost,
    MainSlider,
    MainThumbs,
    MainTrailer,
  }
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
<script>
export default {
  data() {
    return {
      urlVideos:[
      https://www.youtube.com/embed/9rYkZlt2hHE?si=3dtJ99zCLUHm3fv6,
      
      ]

    }
  }
}
</script>

<template>
  <div class="base">
    <div class="container">
      <div class="current-video">
        <iframe src="https://www.youtube.com/embed/9rYkZlt2hHE?si=3dtJ99zCLUHm3fv6" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>      </div>
      <div class="playlist-video">

      </div>
    </div>
  </div>
</template>

<style scoped>
.base{
  height: 650px;
  border: 1px dashed #ff00c8;
}
iframe{
  width: 840px;
  height: 550px;
}
</style>
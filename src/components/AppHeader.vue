<script>
export default {
  data() {
    return {
      
    }
  }
}

const navLink = [
  "HOME",
  "ABOUT US",
  "LIFESTYLE",
  "STORIES",
  "PAGES",
  "CONTACT US",
]
</script>

<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col d-flex justify-content-center">
        <img id="logo" src="/src/assets/img/anime-logo.webp" alt="">
      </div>
      <div class="col d-flex align-items-center">
          <img class="banner-header" src="/src/assets/img/page-banner-1-768x71.webp" alt="">
      </div>
    </div>
  </div>
  <div>
    <div class="container">
      <div class="row">
        <div class="col">
          <h1>ciao</h1>

        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
div{
  border-bottom: 1px solid lightgray;
  height: 150px;
}

#logo{
  object-fit: contain;
  width: 250px;
}

.banner-header{
  width: 70%;
  border-radius: 5px;
}
</style>
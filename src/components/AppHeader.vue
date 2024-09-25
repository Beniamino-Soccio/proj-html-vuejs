<script>
export default {
  data() {
    return {
      
    }
  }
}

const navLink = [
  
]
</script>

<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col d-flex justify-content-center">
        <img id="logo" src="/src/assets/img/anime-logo.webp" alt="">
      </div>
      <div class="col d-flex align-items-center">
          <img class="banner-header" src="/src/assets/img/header-banner-300x38.webp" alt="">
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
  object-fit: contain;
  border-radius: 10px;
}
</style>
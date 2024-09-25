<script>
export default {
  data() {
    return {

    }
  }
}
</script>

<template>
  <section class="container d-flex gap-3 py-4 text-center">
    <div class="card">
      <img src="../assets/img/ideas-anime.webp" class="card-img-top" alt="immagine">
      <div class="card-body">
        <h5 class="card-title">Live Ideas You Might Be Anime</h5>
        <h6>December 26,2022</h6>
        <p class="card-text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi vitae officia vero voluptates
          reprehenderit?</p>
        <a href="#" class="btn btn-primary">Read More</a>
      </div>
    </div>
    <div class="card">
      <img src="../assets/img/visit-france.webp" class="card-img-top" alt="immagine">
      <div class="card-body">
        <h5 class="card-title">Reasons To Visit France</h5>
        <h6>December 26,2022</h6>
        <p class="card-text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi vitae officia vero voluptates
          reprehenderit?</p>
        <a href="#" class="btn btn-primary">Read More</a>
      </div>
    </div>
    <div class="card">
      <img src="../assets/img/travel-alone-300x200.webp" class="card-img-top" alt="immagine">
      <div class="card-body">
        <h5 class="card-title">Traveling Alone Is Awesome</h5>
        <h6>December 26,2022</h6>
        <p class="card-text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi vitae officia vero voluptates
          reprehenderit?</p>
        <a href="#" class="btn btn-primary">Read More</a>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.card {
  width: calc(100% / 3);

  h5 {
    font-size: 19px;
  }

  h6 {
    color: #757575
  }

  .btn {
    background-color: #BF1D2F;
  }
}
</style>
<script>
export default {
  data() {
    return {

    }
  }
}
</script>

<template>
  <section class="container py-5">
    <h3>FEATURED POSTS</h3>
    <div class="d-flex py-4 text-center">
      <div class="row">
        <div class="col">
          <div class="card">
            <img src="../assets/img/ideas-anime.webp" class="card-img-top" alt="immagine">
            <div class="card-body">
              <h5 class="card-title">Live Ideas You Might Be Anime</h5>
              <h6>December 26,2022</h6>
              <p class="card-text">Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
              <a href="#" class="btn btn-primary">Read More</a>
            </div>
          </div>
        </div>
        <div class="col">
          <div class="card">
            <img src="../assets/img/visit-france.webp" class="card-img-top" alt="immagine">
            <div class="card-body">
              <h5 class="card-title">Reasons To Visit France</h5>
              <h6>December 26,2022</h6>
              <p class="card-text">Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
              <a href="#" class="btn btn-primary">Read More</a>
            </div>
          </div>
        </div>
        <div class="col">
          <div class="card">
            <img src="../assets/img/travel-alone-300x200.webp" class="card-img-top" alt="immagine">
            <div class="card-body">
              <h5 class="card-title">Traveling Alone Is Awesome</h5>
              <h6>December 26,2022</h6>
              <p class="card-text">Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
              <a href="#" class="btn btn-primary">Read More</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.card-body {
  background-color: #F3F3F3;
}

h5 {
  font-size: 19px;
}

h6 {
  color: #757575
}

.btn {
  background-color: #BF1D2F;
  padding: 2px 30px;
  border-radius: 15px;
  border: 0;
}
</style>
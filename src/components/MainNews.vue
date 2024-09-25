<script>
export default {
  data() {
    return {

    }
  }
}
</script>

<template>
  <section class="container">
    <div class="top-news d-flex justify-content-between">
      <h3>LIFESTYLE & STORIES</h3>
      <div class="links">
        <button type="button" class="btn btn-secondary">ALL</button>
        <button type="button" class="btn btn-secondary mx-5">LIFESTYLE</button>
        <button type="button" class="btn btn-secondary">STORIES</button>
      </div>
    </div>
    <div class="main-news">
      <div class="row">
        <div class="col-8">
          <img src="../assets/img/success-story.webp" alt="">
        </div>
        <div class="col-4 flex">uno</div>
      </div>
    </div>
  </section>
</template>

<style scoped>
section {
  height: 500px;
  border: 1px dashed goldenrod;
}
</style>
<script>
export default {
  data() {
    return {
      
    }
  }
}
</script>

<template>
  <div class="conteiner">
    <div class="gallery">
      <div class="row ">
        <div class="col-3 side">
        </div>
        <div class="col-6 central">
        </div>
        <div class="col-3 side">
        </div>


      </div>

    </div>

  
  </div>

</template>

<style scoped>
.gallery{
  height: 500px;
  border: 1px dashed dodgerblue;
  display: flex;
}

.central {
  border-radius: 10px;
  background-color: gray;
  width: 400px;
  height: 450 px,
}
.side{
  border-radius: 10px;
  background-color: green;
  width: 100px;
  height: 200px,
}


</style>
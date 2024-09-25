<script>
export default {
  data() {
    return {
      
    }
  }
}
</script>

<template>
  <div class="container">
    <div class="gallery">
      <div class="left-side">
        <div class="lu"></div>
        <div class="ld"></div>
      </div>
      <div class="centrale">
        <div class="c"></div>
      </div>
      <div class="right-side">
        <div class="ru"></div>
        <div class="rd"></div>
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

.c {
  border-radius: 10px;
  background-color: gray;
  height: 100%;
  width: 680px;
  margin-left: 10px;
  margin-right: 10px;
}
.lu{
 
  border-radius: 10px;
  background-color: green;
  height: calc(100% / 2 - 5px);
  width: 300px;
  margin-bottom: 10px;
}
.ld{
 
  border-radius: 10px;
  background-color: green;
  height: calc(100% / 2 - 5px);
  width: 300px;

}
.ru {
  border-radius: 10px;
  background-color: green;
  height: calc(100% / 2 - 5px);
  width: 300px;
  margin-bottom: 10px;

}
.rd{

  border-radius: 10px;
  background-color: green;
  width: 100%;
  height: calc(100% / 2 - 5px);
  width: 300px;

}




</style>
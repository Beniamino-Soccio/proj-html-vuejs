<script>
export default {
  data() {
    return {
      cards:[
        {
          nome:'demo',
          data:'December25,2022',
          text:'Fashion Trend Now A Day'
        },
        {
          nome:'demo',
          data:'December26,2022',
          text:'Traveling Alone Is Awesome'
        }, {
          nome:'demo',
          data:'December25,2022',
          text:'Place For A Road Trip'
        }, {
          nome:'demo',
          data:'December25,2022',
          text:'Music The Love Of My Life'
        }, {
          nome:'demo',
          data:'December26,2022',
          text:'Reason To Visit France'
        },
      ]
      
    }
  }
}
</script>

<template>
  <div class="container">
    <div class="gallery">
      <div class="left-side">
        <div class="boxLup">
          <div class="data align-items-center ">
            <div class="d-flex">
              <p><i class="bi bi-person-fill me-2"></i>{{ cards[0].nome }}</p><p class="ms-2"><i class="bi bi-calendar2-fill me-2 ms-2"></i>{{ cards[0].data }}</p>
            </div>
            <div>
              <h6 class="fw-bold">{{ cards[0].text }}</h6>
            </div>
          </div>
        
        </div>
        <div class="boxLdown">
          <div class="data align-items-center ">
            <div class="d-flex">
              <p><i class="bi bi-person-fill me-2"></i>{{ cards[1].nome }}</p><p class="ms-2"><i class="bi bi-calendar2-fill me-2 ms-2"></i>{{ cards[1].data }}</p>
            </div>
            <div>
              <h6 class="fw-bold">{{ cards[1].text }}</h6>
            </div>
          </div>
          
        </div>
      </div>
      <div class="centrale">
        <div class="boxCentrale">
          <div class="data align-items-center ">
            <div class="d-flex">
              <p><i class="bi bi-person-fill me-2"></i>{{ cards[2].nome }}</p><p class="ms-2"><i class="bi bi-calendar2-fill me-2 ms-2"></i>{{ cards[2].data }}</p>
            </div>
            <div>
              <h6 class="fw-bold">{{ cards[2].text }}</h6>
            </div>
          </div>

        </div>
      </div>
      <div class="right-side">
        <div class="boxRup">
          <div class="data align-items-center ">
            <div class="d-flex">
              <p><i class="bi bi-person-fill me-2"></i>{{ cards[3].nome }}</p><p class="ms-2"><i class="bi bi-calendar2-fill me-2 ms-2"></i>{{ cards[3].data }}</p>
            </div>
            <div>
              <h6 class="fw-bold">{{ cards[3].text }}</h6>
            </div>
          </div>
        </div>
        <div class="boxRdown">
          <div class="data align-items-center ">
            <div class="d-flex">
              <p><i class="bi bi-person-fill me-2"></i>{{ cards[4].nome }}</p><p class="ms-2"><i class="bi bi-calendar2-fill me-2 ms-2"></i>{{ cards[4].data }}</p>
            </div>
            <div>
              <h6 class="fw-bold">{{ cards[4].text }}</h6>
            </div>
          </div>
        </div>
      </div>

      
     
    </div>
  </div>

</template>

<style scoped>

.gallery {
  height: 500px;
  border: 1px dashed dodgerblue;
  display: flex;
  justify-content: space-between;
}

.boxCentrale {
  background-image: url(../assets/img/best-places.webp);
  background-size: cover;
  border-radius: 10px;
  height: 100%;
  width: 675px;
  margin-left: 10px;
  margin-right: 10px;
  position: relative;
}
.boxLup{
  background-image: url(../assets/img/anime-fashion.webp);
  background-size: cover;
  border-radius: 10px;
  background-color: green;
  height: calc(100% / 2 - 5px);
  width: 300px;
  margin-bottom: 10px;
  position: relative;

}
.boxLdown{
  background-image: url(../assets/img/travel-alone.webp);
  background-size: cover;
  border-radius: 10px;
  background-color: green;
  height: calc(100% / 2 - 5px);
  width: 300px;
  position: relative;


}
.boxRup {
  background-image: url(../assets/img/music-love.webp);
  background-size: cover;
  border-radius: 10px;
  background-color: green;
  height: calc(100% / 2 - 5px);
  width: 300px;
  margin-bottom: 10px;
  position: relative;


}
.boxRdown{  
  background-image: url(../assets/img/visit-france.webp);
  background-size: cover;
  border-radius: 10px;
  background-color: green;
  width: 100%;
  height: calc(100% / 2 - 5px);
  width: 300px;
  position: relative;

}


.boxCentrale, .boxLup, .boxLdown, .boxRup, .boxRdown {
  display: flex;
  flex-direction: column;
  justify-content: center;  
  align-items: center;      
  background-size: cover;
  border-radius: 10px;
  position: relative;
  color: white;
  padding: 15px;
  text-align: center;
  height: 100%;
  width: 100%;
}

.data {
  display: flex;
  flex-direction: column;
  justify-content: center;  
  align-items: center;      
  position: absolute;
  bottom: 0;                
  left: 50%;
  transform: translateX(-50%); 
  width: 100%;
  color: white;
}

p, h6 {
  margin: 5px 0;
  text-align: center;
}




.boxLup, .boxLdown, .boxRup, .boxRdown {
  width: 300px;
  height: calc(50% - 5px);
  margin-bottom: 10px;
}

.boxCentrale {
  width: 675px;
  margin: 0 10px;
}
</style>
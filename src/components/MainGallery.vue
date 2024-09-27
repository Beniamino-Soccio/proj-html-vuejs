<script>
export default {
  data() {
    return {
      cards:[
        {
          firstTopic: 'Fashion',
          secondTopic: 'Lifestyle',
          nome:'demo',
          data:'December25,2022',
          text:'Fashion Trend Now A Day'
        },
        {
          firstTopic: 'Fashion',
          secondTopic: 'Stories',
          nome:'demo',
          data:'December26,2022',
          text:'Traveling Alone Is Awesome'
        }, 
        {
          firstTopic: 'Fashion',
          secondTopic: 'Stories',
          thirdTopic: 'Travel',
          nome:'demo',
          data:'December25,2022',
          text:'Place For A Road Trip'
        }, 
        {
          firstTopic: 'Culture',
          secondTopic: 'Lifestyle',
          nome:'demo',
          data:'December25,2022',
          text:'Music The Love Of My Life'
        }, 
        {
          firstTopic: 'Lifestyle',
          secondTopic: 'Travel',
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
        <div class="boxLup ">
          <div class="buttons d-flex ms-2">
            <button class="first-topic border-0 me-2">{{ cards[0].firstTopic }} </button>
            <button class="second-topic border-0">{{ cards[0].secondTopic }} </button>
          </div>
          <div class="data ">
            <div class="d-flex">
              <p><i class="bi bi-person-fill me-2"></i>{{ cards[0].nome }}</p><p class="ms-2"><i class="bi bi-calendar2-fill me-2 ms-2"></i>{{ cards[0].data }}</p>
            </div>
            <div>
              <h6 class="fw-bold">{{ cards[0].text }}</h6>
            </div>
          </div>
        
        </div>
        <div class="boxLdown">
          <div class="buttons d-flex ms-2">
            <button class="first-topic border-0 me-2">{{ cards[1].firstTopic }} </button>
            <button class="second-topic border-0">{{ cards[1].secondTopic }} </button>
          </div>
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
          <div class="buttons d-flex ms-2">
            <button class="first-topic border-0 me-2">{{ cards[2].firstTopic }} </button>
            <button class="second-topic border-0 me-2">{{ cards[2].secondTopic }} </button>
            <button class="third-topic border-0">{{ cards[2].thirdTopic }} </button>
          </div>
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
          <div class="buttons d-flex ms-2">
            <button class="first-topic border-0 me-2">{{ cards[3].firstTopic }} </button>
            <button class="second-topic border-0 me-2">{{ cards[3].secondTopic }} </button>
          </div>
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
          <div class="buttons d-flex ms-2">
            <button class="first-topic border-0 me-2">{{ cards[4].firstTopic }} </button>
            <button class="second-topic border-0">{{ cards[4].secondTopic }} </button>
          </div>
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
  display: flex;
  justify-content: space-between;
  margin-top: 50px;
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
  height: calc(100% / 2 - 5px);
  width: 300px;
  margin-bottom: 10px;
  position: relative;

}
.boxLup img{
  border-radius: 10px;
  height: calc(100% / 2 - 5px);
  width: 100%;
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
  filter: brightness(50%);
  z-index: 1;

}

.boxCentrale:hover, .boxLup:hover, .boxLdown:hover, .boxRup:hover, .boxRdown:hover {
  filter: brightness(70%); 
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

.first-topic,
.second-topic,
.third-topic
 {
  top: 10px;
  font-size: 16px;
  padding: 0 15px;
  border-radius: 5px;
  background-color: white;
  z-index: 2;
}

.first-topic:hover {
  color: red;
}

.second-topic:hover {
  color: red;
}

.third-topic:hover {
  color: red;
}

.buttons {
  position: absolute;
  top: 15px; 
  left: 10px; 
  right: 10px; 
  display: flex;
  justify-content: center; 
}

.data, .buttons {
  z-index: 3; /* Porta i bottoni e il testo sopra l'effetto */
}
</style>
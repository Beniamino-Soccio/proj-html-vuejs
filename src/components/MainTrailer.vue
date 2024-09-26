<script>
export default {
  data() {
    return {
      activeVideo: 0,
      videos:[
        {
          url: "https://www.youtube.com/embed/9rYkZlt2hHE?si=3dtJ99zCLUHm3fv6",
          name: "Eternal Cultivation Anime",
          img: "https://i.ytimg.com/vi/9rYkZlt2hHE/hqdefault.jpg",
          index:1
        },
        {
          url: "https://www.youtube.com/embed/zlwQERpksnw?si=wDOqxFA5RRVfJypX",
          name: "Sun's Out, Guns Out",
          img: "https://i.ytimg.com/vi/zlwQERpksnw/hqdefault.jpg",
          index:2
        },
        {
          url: "https://www.youtube.com/embed/itQnUDMMhaU?si=9PYUEuQkEzBVg5pQ",
          name: "Top 10 Vinland Saga Moments",
          img: "https://i.ytimg.com/vi/itQnUDMMhaU/hqdefault.jpg",
          index:3
        },
        {
          url: "https://www.youtube.com/embed/IrU2dklT11s?si=niklH5vQLpJrQ2Vf",
          name: "Everytime Sukuna Appears",
          img: "https://i.ytimg.com/vi/IrU2dklT11s/hqdefault.jpg",
          index:4
        },
        {
          url: "https://www.youtube.com/embed/H5qupR6YQpQ?si=kfkvAtk_7NMEfdbx",
          name: "Wizard King (Julios) Vs Licht (Patri) Full Fight",
          img: "https://i.ytimg.com/vi/H5qupR6YQpQ/hqdefault.jpg",
          index:5
        },
        {
          url: "https://www.youtube.com/embed/ICt1jYfucec?si=bd1cfgu_l5AI4ab9",
          name: "Vinland Saga | SHATTERED",
          img: "https://i.ytimg.com/vi/ICt1jYfucec/hqdefault.jpg",
          index:6

        },
        {
          url: "https://www.youtube.com/embed/CkC5CtabT1Y?si=KANDaR0hfcUebBsv",
          name: "Konan Arranges",
          img: "https://i.ytimg.com/vi/CkC5CtabT1Y/hqdefault.jpg",
          index: 7
        },
      
      ]

    }
  },
  methods: {
    selectVideo(video) {
            this.activeVideo = video; 
        },
    
  }
}
</script>

<template>
  <div class="base">
    <div class="container d-flex">
      <div class="current-video">
        <iframe :src="activeVideo.url" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>      
      </div>
      <div class="playlist-video">
        <div class="info-playlist d-flex align-items-center px-3">
          <i class="bi bi-play-fill text-white"></i>
          <div class="d-flex flex-column">
            <p>Video Playlist</p> 
            <p class="fs-6">{{ activeVideo.index }}/7</p>
          </div>
        </div>
        <ul>
          <li class="d-flex align-items-center gap-3" v-for="(video, index) in videos" @click="selectVideo(video)">
            <p class="text-center">{{video.index}}</p>
            <img :src="video.img" :alt="video.name">
            <p>{{video.name}}</p>
          </li>
        </ul>
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
ul{
  list-style-type: none;
  overflow: auto;
  height: 470px;
  padding: 0;
  max-width: 400px;
}
li{
  border-bottom: 1px solid #7c7c7c;
  padding: 12px;
}
ul img{
  width: 85px;
  height: 65px;
  border-radius: 10px;
}
li p:first-child{
  min-height: 24px;
  min-width: 24px;
  color: #fff;
  background-color: #000;
  line-height: 24px;
  border-radius: 5px;
}
.info-playlist{
  color: white;
  background-color: #333;
  height: 80px;
}
p{
  margin: 0;
}
.playlist-video{
  height: 550px;
}
i{
  font-size: 50px;
}
li:hover{
  color: red;
}
li:hover p:first-child{
  background-color: red;
}
</style>
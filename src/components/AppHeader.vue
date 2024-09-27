<script>
import 'bootstrap/dist/js/bootstrap.bundle.min.js';
import 'bootstrap-icons/font/bootstrap-icons.css';
import { getCurrentInstance } from 'vue';
export default {
  data() {
    return {
    navLink: [
      {
        name:  'HOME',
        url: ''
       },
       { 
        name: 'ABOUT US',
        url: ''
       },
       { 
        name: 'LIFESTYLE',
        url: ''
       },
       { 
        name: 'STORIES',
        url: ''
       },
       {
        name: 'PAGES',
        url: ''
       },
       { 
        name: 'CONTACT US',
        url: ''
       },
    ],
    currentIndex: 0,
    newUpdates:[
      {
        img:'/src/assets/img/healthy-foods-150x150.webp',
        hours: '05.32',
        text: 'THE BEST HEALTHY FOODS'
      },
      {
        img:'/src/assets/img/rice-ball-150x150.webp',
        hours: '05.37',
        text: 'HYGENIC RECEIPE TO PREPARE RICE'
      },
      {
        img:'/src/assets/img/winter-150x150.webp',
        hours: '05.29',
        text: 'THE BEST WINTER OUTFITS'
      },
      {
        img:'/src/assets/img/meal-time-150x150.webp',
        hours: '05.35',
        text: 'THE BEST TIME TO HAVE A MEAL'
      },
    ]
  }
    },
    methods:{
      nextUpdate(){
        this.currentIndex = (this.currentIndex + 1) % this.newUpdates.length;
      },
      prevUpdate(){
        this.currentIndex = (this.currentIndex - 1) % this.newUpdates.length;
      }
    }
  }
</script>

<template>
  <header>
    <div class="news-updates d-flex align-items-center py-2">
      <div class="container">
        <div class="row">
          <div class="col-2 updates-text d-flex justify-content-center align-items-center py-2">
            <p class="m-0">NEW UPDATES</p>
          </div>
          <!--Current New Updates-->
          <div class="current-new-updates col-7 d-flex align-items-center p-0 gap-3 text-white fw-bold">
            <img :src="newUpdates[currentIndex].img" :alt="newUpdates[currentIndex].text">
            <div><span>{{ newUpdates[currentIndex].hours }}</span></div>
            <div><span>{{ newUpdates[currentIndex].text }}</span></div>
          </div>
          <!--Social Icon-->
          <div class="social-icons col-3 d-flex justify-content-end align-items-center">
            <a href="#"><i class="bi bi-facebook"></i></a>
            <a href="#"><i class="bi bi-twitter-x"></i></a>
            <a href="#"><i class="bi bi-instagram"></i></a>
            <a href="#"><i class="bi bi-youtube"></i></a>
          </div>
        </div>
      </div>
    </div>
    <div class="container my-3">
      <div class="row">
        <!--logo header-->
        <div class="col d-flex align-items-center">
          <img id="logo" src="/src/assets/img/anime-logo.webp" alt="">
        </div>
        <!--banner header-->
        <div class="box-banner col-lg-6 col-sm-12 d-flex align-items-center">
          <img class="banner-header" src="/src/assets/img/header-banner.webp" alt="">
        </div>
      </div>
    </div>
    <hr class="m-0">
    <!--Navbar-->
    <div class="container py-3">
      <div class="row">
        <div class="col-2 d-flex align-items-center">
          <a href="#"><i class="bi bi-list fs-2"></i></a>
        </div>
        <div class="col-8 d-flex align-items-center justify-content-center">
          <ul class="m-0" v-for="(nav, index) in navLink">
            <a href="#"><li>{{navLink[index].name }}</li></a>
          </ul>
        </div>
        <div class="col-2 d-flex align-items-center justify-content-end">
          <a href="#"><i class="bi bi-search fs-2"></i></a>
        </div>
      </div>
    </div>
    </header>
  </template>

<style lang="scss" scoped>
@use 'bootstrap/scss/bootstrap.scss' as *;


.current-new-updates{
  height: 50px;
}

.current-new-updates img{
  height: 100%;
}

.updates-text{
  background-color: #545454;
  color: white;
  font-weight: bold;
  height: 50px;
}

.news-updates{
  background-color: #BF1D2E;
  height: 50px;
}

a{
  text-decoration: none;
  color: black;
  &
  :hover{
    color: #BF1D2E;
  }
}

#logo{
  object-fit: contain;
  width: 250px;
}
.banner-header{
    border-radius: 5px;
    width: 100%;
    height: 90px;
}

li{
  list-style-type: none;
  font-size: 20px;
  font-weight: bold;
}

a.nav-link:hover{
  color: #BF1D2E
}

.social-icons i{
  background-color: white;
  border-radius: 50%;
  padding: 5px 8px;
  color: #BF1D2E;
  font-size: 15px;
  margin-right: 10px;
}
</style>
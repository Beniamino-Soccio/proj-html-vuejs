<script>
import 'bootstrap/dist/js/bootstrap.bundle.min.js';
import 'bootstrap-icons/font/bootstrap-icons.css';
import NewUpdatesHeaderTop from './NewUpdatesHeaderTop.vue';
import AnimatedBurgerMenuHeader from './AnimatedBurgerMenuHeader.vue';
export default {
  data() {
    return {
    navLink: [
      {
        name:  'HOME',
        url: '',
        icon: 'bi-house-fill'
       },
       { 
        name: 'ABOUT US',
        url: '',
        icon: 'bi bi-person-fill'
       },
       { 
        name: 'LIFESTYLE',
        url: '',
        icon: 'bi bi-suitcase-lg-fill'
       },
       { 
        name: 'STORIES',
        url: '',
        icon: 'bi bi-book-fill'
       },
       {
        name: 'PAGES',
        url: '',
        icon: 'bi bi-file-text-fill'
       },
       { 
        name: 'CONTACT US',
        url: '',
        icon: 'bi bi-envelope-fill'
       },
    ],
  }
},
components: {
  NewUpdatesHeaderTop,
  AnimatedBurgerMenuHeader
}
  }
</script>

<template>
  <header>
    <NewUpdatesHeaderTop/>
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
    <div class="container">
      <div class="row">
        <div class="col-2 d-flex align-items-center">
          <a href="#"><AnimatedBurgerMenuHeader/></a>
        </div>
        <div class="col-8 d-flex align-items-center justify-content-center">
          <ul class="m-0" v-for="(nav, index) in navLink" :key="index">
            <li class="fw-semibold">
             <a :href="nav.url">
               <span><i :class="[nav.icon]"></i> {{nav.name }}</span>
             </a>
           </li>
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

a{
  text-decoration: none;
  color: black;
  &
  :hover{
    color: #BF1D2E;
  }
}

li{
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
}

a.nav-link:hover{
  color: #BF1D2E
}
</style>
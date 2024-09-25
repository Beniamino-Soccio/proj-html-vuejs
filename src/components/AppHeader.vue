<script>
import 'bootstrap/dist/js/bootstrap.bundle.min.js';
import 'bootstrap-icons/font/bootstrap-icons.css';
export default {
  data() {
    return {
    navLink: [
      {
        name:  'HOME',
        url: ''
       },
       { name: 'ABOUT US',
        url: ''
       },
       { name: 'LIFESTYLE',
        url: ''
       },
       { name: 'STORIES',
        url: ''
       },
       { name: 'PAGES',
        url: ''
       },
       { name: 'CONTACT US',
        url: ''
       },
    ]
  }
    }
  }
</script>

<template>
  <header>
    <div class="container py-4">
      <div class="row">
        <div class="col d-flex align-items-center">
          <img id="logo" src="/src/assets/img/anime-logo.webp" alt="">
        </div>
        <div class="col-lg-6 col-sm-12 d-flex align-items-center">
          <img class="banner-header" src="/src/assets/img/page-banner-1-768x71.webp" alt="">
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
        <div class="col-8 d-flex align-items-center">
          <ul class="m-0" v-for="(nav, index) in navLink">
            <a href="#"><li>{{navLink[index].name }}</li></a>
          </ul>
        </div>
        <div class="col-2 d-flex align-items-center justify-content-end">
          <a href="#"><i class="bi bi-search fs-2"></i></a>
        </div>
      </div>
    </div>
    
    










    <!--
      <div class="container px-0">
        <nav class="navbar navbar-expand-lg">
          <div class="container-fluid">
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
              <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
              <ul class="navbar-nav me-auto mb-2">
                <!--burger menù
                <a href="#"><span><i class="bi bi-list fs-2"></i></span></a>
                <li class="nav-item" v-for="(nav, index) in navLink ">
                  <a class="nav-link" aria-current="page" href="#">{{navLink[index].name }}</a>
                </li>
              </ul>
            </div>
            
            <a class="navbar-brand" href="#"><i class="bi bi-search"></i></a>
          </div>
        </nav>
      </div>
    -->
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

#logo{
  object-fit: contain;
  width: 250px;
}

.banner-header{
  border-radius: 5px;
  width: 100%;
}

li{
  list-style-type: none;
  font-size: 20px;
}

a.nav-link:hover{
  color: #BF1D2E
}
</style>
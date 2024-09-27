<script>
export default {
  name: 'AppFooter',
  data() {
    return {
      footerSections: [
        {
          title: "GET STARTED",
          links: ["Resources", "Tutorials", "Examples", "Docs"]
        },
        {
          title: "ABOUT",
          links: ["Stories", "Community", "Blog", "Brand Assets"]
        },
        {
          title: "FEATURES",
          links: ["Overview", "Design", "Code", "Collaborate"]
        },
        {
          title: "QUICK LINKS",
          links: ["Stories", "Community", "Blog", "Brand Assets"]
        }
      ]
    };
  }
};
</script>

<template>    
  <footer class="footer text-light">
    <div class="bar-container">
      <div class="bar"></div>
      <div class="triangle"></div>
    </div>
    <div class="container">
      <div class="row">

        <!-- Sezione con v-for per renderlo dinamico -->
        <div v-for="(section, index) in footerSections" :key="index" class="col-md-2 list">
          <h5>{{ section.title }}</h5>
          <ul class="list-unstyled">
            <li v-for="(link, linkIndex) in section.links" :key="linkIndex">
              <a href="#" class="text-light">{{ link }}</a>
            </li>
          </ul>
        </div>
        
        <!-- Form di iscrizione -->
        <div class="col-md-4 list">
          <h5>SUBSCRIBE TO NEWSLETTER</h5>
          <form>
            <input type="email" class="form-control mb-2" placeholder="Email" />
            <button type="submit" class="btn button w-100">SUBSCRIBE</button>
          </form>
        </div>
      </div>
      <hr>
      <div class="row mt-4 justify-content-between align-items-center">
        <div class="col-md-6">
          <img class="logo" src="/src/assets/img/anime-whitelogo.png" alt="Anime Tech Logo">
        </div>
        <div class="col-md-6 text-md-end">
          <p>© Anime Tech, Theme by HasnainDEV</p>
        </div>
      </div>
    </div>          
  </footer>
</template>


<style scoped>
footer {
  color: #ffffff;
  height: 420px;
  background-color: #bf1d2e;
  padding: 80px 0;
  font-size: 1.1em;
}

.footer a {
  text-decoration: none;
  color: #0a0202;
  transition: color 0.3s ease;
}

.footer a:hover {
  color: grey !important;
}

.list {
  line-height: 35px;
}

.button {
  background-color: #545454;
  color: aliceblue;
}

.button:hover {
  background-color: aliceblue;
  color: red;
}

hr {
  border: 0;
  border-top: 3px solid #ffffff;
}

.logo {
  width: 40%;
}

p {
  margin-top: 0;
  margin-bottom: 1rem;
}

.bar-container {
    position: relative;
    width: 100%;
    height: 20px;
    background-color: transparent;
  }

  .bar {
    width: 100%;
    height: 5px;
    background-color: #333;
    position: absolute;
    left: 0;
    top: -80px;
  }

  .triangle {
    width: 0;
    height: 0;
    border-left: 13px solid transparent;
    border-right: 13px solid transparent;
    border-top: 13px solid #333;
    position: absolute;
    top: -75px;
    left: 50%;
    transform: translateX(-50%);
  }
</style>
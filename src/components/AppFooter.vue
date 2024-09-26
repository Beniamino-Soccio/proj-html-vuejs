<script>
export default {
  name: 'AppFooter',
};
</script>

<template>
  <footer class="footer text-light">
    <div class="container">
      <div class="row">
        <div class="col-md-2 list">
          <h5>GET STARTED</h5>
          <ul class="list-unstyled">
            <li><a href="#" class="text-light">Resources</a></li>
            <li><a href="#" class="text-light">Tutorials</a></li>
            <li><a href="#" class="text-light">Examples</a></li>
            <li><a href="#" class="text-light">Docs</a></li>
          </ul>
        </div>
        <div class="col-md-2 list">
          <h5>ABOUT</h5>
          <ul class="list-unstyled">
            <li><a href="#" class="text-light">Stories</a></li>
            <li><a href="#" class="text-light">Community</a></li>
            <li><a href="#" class="text-light">Blog</a></li>
            <li><a href="#" class="text-light">Brand Assets</a></li>
          </ul>
        </div>
        <div class="col-md-2 list">
          <h5>FEATURES</h5>
          <ul class="list-unstyled">
            <li><a href="#" class="text-light">Overview</a></li>
            <li><a href="#" class="text-light">Design</a></li>
            <li><a href="#" class="text-light">Code</a></li>
            <li><a href="#" class="text-light">Collaborate</a></li>
          </ul>
        </div>
        <div class="col-md-2 list">
          <h5>QUICK LINKS</h5>
          <ul class="list-unstyled">
            <li><a href="#" class="text-light">Stories</a></li>
            <li><a href="#" class="text-light">Community</a></li>
            <li><a href="#" class="text-light">Blog</a></li>
            <li><a href="#" class="text-light">Brand Assets</a></li>
          </ul>
        </div> 
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
</style>

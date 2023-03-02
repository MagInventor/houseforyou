<template>
  <div class="home-page">
    <div class="home-page__bg">
      <div class="home-page__bg-overlay">
        <img class="home-page__bg-img" :src="require('../assets/bg-main.jpg')">
      </div>
    </div>
    <div class="home-page__content">
      <div class="container">
        <div class="home-page__content-logo">
          <img class="home-page__content-logo-logo" alt="Logo" src="../assets/logo.png"> 
        </div>
        <h1 class="home-page__content-title">Domki <span> dla zwierząt</span></h1>
        <div class="home-page__content-start">
          <p>Wybierz piękny dom dla swojego zwierzaka</p>
          <router-link to="/catalog"><button>Start</button></router-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomePage',
  props: {
    msg: String
  },
  data() {},
  comuted: {
  },
  methods: {
    checkWindowWidth() {}
  }
}
</script>

<style>
body {
  padding: 0;
  margin: 0;
}

a {
  text-decoration: none;
}

.container {
  margin: 0 auto;
}

.home-page {
  position: relative;
}

.home-page__bg {
  width: 100%;
  background: #06050a;
}

.home-page__bg-overlay {
  background: #000;
  opacity: .7;
}

.home-page__bg-img {
  width: 100%;
  height: 100vh;
  object-fit: cover;
}

.home-page__content {
  width: 100%;
  height: auto;
  position: absolute;
  top: 0;
  left: 0;
}

.home-page__content .container {
  height: 100vh;
  padding: 0 20px;
  display: grid;
  justify-items: center;
  grid-template-rows: 1fr 1fr 150px;
}

.home-page__content-logo {
    padding: 10px;
    background: #FFD56F;
    border-radius: 15px;
    text-align: center;
    display: grid;
    align-self: end;
}

.home-page__content-logo-logo {
  width: 50px;
  height: 50px;
}

.home-page__content-title {
  width: 150px;
  text-transform: uppercase;
  font-size: 40px;
  font-family: Gloock-Regular, OpenSans-Regular, Arial, serif;
  color: #fff;
  text-align: center;
  line-height: 1;
}

.home-page__content-title span {
  color: #E1F1DD;
  font-family: 'Montserrat', Tahoma, Verdana, sans-serif;
  font-size: 16px;
  font-weight: 400;
  line-height: 1;
}

.home-page__content-start {
  font-family: 'Montserrat', Tahoma, Verdana, sans-serif;
}

.home-page__content-start p {
  padding: 10px;
  color: #FFD56F;
  font-size: 14px;
}

.home-page__content-start button {
  width: 180px;
  height: 40px;
  padding: 10px;
  background: transparent;
  color: #939B62;
  border-radius: 50px;
  border: 0;
  font-size: 18px;
  font-weight: 600;
  letter-spacing: 0.5px;
  text-align: left;
  cursor: pointer;
}

.home-page__content-start button:hover {
  background: #FFD56F;
  border: 1px solid #FFD56F;
  color: #000;
}

@media (min-width: 480px) {
  .home-page__content .container {
    display: grid;
    grid-template-rows: 1fr 160px 1fr;
    grid-gap: 25px;
  }

  .home-page__content-start button  {
    border: 1px solid #939B62;
  }
}

@media (min-width: 768px) {
  .home-page__content .container {
    display: grid;
    grid-template-rows: 1fr 100px 1fr;
    grid-gap: 10px;
  }

  .home-page__content-start button {
    color: #FFB26B;
    border: 1px solid #FFB26B;
  }
}

@media (min-width: 980px) {
  .home-page__content .container {
    display: grid;
    grid-template-rows: 200px 170px 1fr;
    grid-gap: 20px;
  }
}
</style>

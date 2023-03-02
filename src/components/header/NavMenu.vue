<template>
    <nav class="nav-menu__mobile">
      <router-link to="/">
        <button>
          <img class="nav-menu__mobile-icon icon-show" :src="require('../../assets/icons/home.png')">
          <p class="nav-hide"> Główna</p>
        </button>
      </router-link>
      <router-link to="/catalog">
        <button>
          <img class="nav-menu__mobile-icon icon-show" :src="require('../../assets/icons/catalog.png')">
            <p class="nav-hide">Katalog</p>
        </button>
      </router-link>
      <div class="nav-menu__mobile-window icon-show"></div>
      <router-link to="/about">
        <button>
          <img class="nav-menu__mobile-icon icon-show" :src="require('../../assets/icons/about.png')">
          <p class="nav-hide">O nas</p>
        </button>
      </router-link>
      <router-link to="/contacts">
        <button><img class="nav-menu__mobile-icon icon-show" :src="require('../../assets/icons/contacts.png')">
          <p class="nav-hide">Kontakty</p>
        </button>
      </router-link>
  </nav>
</template>

<script>
	export default {
  name: 'NavMenu',
  components: {}
}
</script>

<style>
nav {
  width: calc(100% - 40px);
  margin: 0 20px 20px 20px;
  height: 60px;
  position: fixed;
  bottom: 0;
  z-index: 1;
/*  background: #FFB26B;*/
  background: #3c3c3c;
  border-radius: 50px;
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  justify-items: center;
  align-items: center;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
  cursor: pointer;
}

nav a.router-link-exact-active {
  color: #42b983;
  background: #FFD56F;
}

.nav-menu__mobile  {

}

.nav-menu__mobile button {
  width: 50px;
  height: 50px;
  background: transparent;
  border: transparent;
  border-radius: 50px;
  cursor: pointer;
}

.nav-menu__mobile button:hover {
  background: #FFD56F;
}

.nav-menu__mobile img {
  width: 30px;
  height: 30px;
}

.icon-show {
  display: block;
}

.nav-hide {
  display: none;
}

nav p {
  color: #fff;
  font-size: 14pxs;
  font-weight: bold;
}


@media (min-width: 480px) {

}

@media (min-width: 768px) {
  nav {
    width: 100%;
    margin: 0;
    height: 52px;
    position: fixed;
    top: 80px;
    z-index: 1;
  /*  background: #FFB26B;*/
    background: #3c3c3c;
    border-radius: 0;
    display: grid;
    grid-template-columns: repeat(4, 100px);
    justify-items: center;
    justify-content: center;
    align-items: center;
  }
  .nav-hide {
    display: block;
  }

  .icon-show {
    display: none;
  }

  nav a.router-link-exact-active {
    background: transparent;
  }
  nav a.router-link-exact-active p {
    color: #FFD56F;
  }

  .nav-menu__mobile button {
    width: 100px;
    height: 50px;
    background: transparent;
    border: transparent;
    border-radius: 0;
    cursor: pointer;
  }

  .nav-menu__mobile button:hover {
    background: transparent;
    color: #FFD56F;
  }

  .nav-menu__mobile button:hover p {
    background: transparent;
    color: #FFD56F;
  }
}

@media (min-width: 980px) {

}
</style>

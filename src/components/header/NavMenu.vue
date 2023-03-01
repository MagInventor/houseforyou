<template>
    <nav class="nav-menu__mobile">
      <router-link to="/">
        <button><img class="nav-menu__mobile-icon" :src="require('../../assets/icons/home.png')"></button>
      </router-link>
      <router-link to="/catalog">
        <button><img class="nav-menu__mobile-icon" :src="require('../../assets/icons/catalog.png')"></button>
      </router-link>
      <div class="nav-menu__mobile-window"></div>
      <router-link to="/about">
        <button><img class="nav-menu__mobile-icon" :src="require('../../assets/icons/about.png')"></button>
      </router-link>
      <router-link to="/contacts">
        <button><img class="nav-menu__mobile-icon" :src="require('../../assets/icons/contacts.png')"></button>
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
  width: 100%;
  height: 66px;
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
</style>

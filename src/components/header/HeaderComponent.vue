<template>
  <header>
    <header-elements></header-elements>
    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/catalog">Catalog</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/blog">Blog</router-link> |
      <router-link to="/contacts">Contacts</router-link> 
  </nav>
  </header>
</template>

<script>
	
</script>

<style>
nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>

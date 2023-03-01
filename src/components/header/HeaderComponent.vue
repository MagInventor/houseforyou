<template>
  <header>
    <header-elements/>
    <nav-menu/>
  </header>
</template>

<script>
import HeaderElements from './HeaderElements'
import NavMenu from './NavMenu'

export default {
  name: 'TheHeader',
  components: {
    HeaderElements, NavMenu
  }
}
</script>

<style>

</style>

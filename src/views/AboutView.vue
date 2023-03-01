<template>
  <div class="about">
    <header-component/>
    <h1>This is an about page</h1>
    <!-- <about-page/> -->
  </div>
</template>

<script>
import HeaderComponent from '@/components/header/HeaderComponent'

export default {
  name: 'AboutView',
  components: {
    HeaderComponent
  }
}
</script>

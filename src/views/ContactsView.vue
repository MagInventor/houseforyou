<template>
  <div class="contacts">
    <header-component/>
    <h1>This is a contacts page</h1>
    <!-- <contacts-page/> -->
  </div>
</template>

<script>
import HeaderComponent from '@/components/header/HeaderComponent'

export default {
  name: 'ContactsView',
  components: {
    HeaderComponent
  }
}
</script>

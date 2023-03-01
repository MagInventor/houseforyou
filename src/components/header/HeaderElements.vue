<template>
  <div class="heading">
    <div class="container">
      <div>
        <router-link to="/" class="logo">
          <img class="logo-img" src="../../assets/logo.png" alt="logo">
            <!-- <span>OM</span> -->
        </router-link>
      </div>
      <div class="head-elements">
        <div class="head-elements">
        <form class="head-elements__search" onsubmit="return false;" >
          <input 
            id="search"
            type="search"
            name="search"
            placeholder="Czego shukasz?" 
            autocomplete="off"

          >
           <button 
            class="search"

            >
            <img alt="Search" class="head-elements__search_img" src="../../assets/icons/search.png">
           </button>
        </form>
        <router-link to="/like" class="head-elements__like">
          <img alt="Like" class="head-elements__like_img" src="../../assets/icons/favorite.png">
          <!-- <p class="head-elements__like_quantity show-quantity">{{this.LIKE.length}}</p> -->
        </router-link>
        <router-link to="/cart" class="head-elements__cart">
          <img alt="Cart" class="head-elements__cart_img" src="../../assets/icons/cart.png">
          <!-- <p class="head-elements__cart_quantity show-quantity">{{this.CART.length}}</p> -->
        </router-link>
        <router-link to="/user" class="head-elements__user">
          <img alt="User" class="head-elements__user_img" src="../../assets/icons/user.png">
        </router-link>
      </div>
      </div>
    </div>
  </div>
</template>

<script>
	export default {
  name: 'HeaderElements',
  components: {}
}
</script>

<style>

</style>

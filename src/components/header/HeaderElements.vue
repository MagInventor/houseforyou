<template>
  <div class="heading">
    <div class="container">
      <div>
        <router-link to="/" class="logo">
          <img class="logo-img" src="../../assets/logo.png" alt="logo">
            <!-- <span>OM</span> -->
        </router-link>
      </div>
      <form class="head-elements__search" onsubmit="return false;" >
        <input 
          class="hide" 
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
      <div class="burger-menu">
        <div class="burger-menu__img">
          <img alt="menu" src="../../assets/burger-menu.png" width="25" height="25">
        </div>
      </div>
      <div class="head-elements">
        <div class="head-elements__menu hide">
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
.heading .container {
  height: 80px;
  padding: 0 20px;
/*  background: #eeaabb;*/
  display: grid;
  grid-template-columns: 40px auto 40px;
  align-content: center;
  align-items: center;
}

.head-elements {
  display: flex;
  flex-direction: row;
  justify-self: end;
  align-items: center;
}

.logo {
  width: 40px;
  height: 40px;
  cursor: pointer;
}

.logo-img {
  width: 40px;
  height: 40px;
}

span {
  padding-top: 16px;
  font-size: 26px;
}

#search {
  height: 30px;
}

input[type=search] {
  width: 125px;
  border: 1px solid #e1dddb;
  border-radius: 50px;
  padding-left: 9px;
  color: #e1dddb;
}

::-webkit-input-placeholder {
  color: #e1dddb;
}
:-moz-placeholder {
  color: #e1dddb;
}
::-moz-placeholder {
  color: #e1dddb;
}
:-ms-input-placeholder {
  color: #e1dddb;
}

.head-elements__search {
  height: 40px;
  margin-right: 3;
  margin-bottom: 5px;
  display: flex;
  align-items: center;
  justify-content: end;
}

.head-elements__search button {
  width: 30px;
  height: 30px;
  background: transparent;
  border: transparent;
  cursor: pointer;
}

.burger-menu__img {
  padding-left: 15px;
}

.head-elements__search button:hover {
  background: #ffc18e;
  border-radius: 0 3px 3px 0;
}

.head-elements__like,
.head-elements__cart,
.head-elements__user {
  width: 40px;
  height: 40px;
  border-radius: 50px;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  position: relative;
}

.head-elements__like:hover,
.head-elements__cart:hover,
.head-elements__user:hover {
background: #ffc18e;
}

.head-elements__search_img,
.head-elements__like_img,
.head-elements__cart_img,
.head-elements__user_img {
  width: 25px;
  height: 25px;
}

.head-elements__like_img {
  margin-bottom: 1px;
}

.head-elements__cart_img {
/*  margin-bottom: 2px;*/
}

.head-elements__like_quantity,
.head-elements__cart_quantity {
  width: 18px;
  height: 18px;
  background: #ffc18e;
  color: #000;
  border-radius: 50px;
  text-align: center;
  font-size: 10px;
  line-height: 1.7;
  position: absolute;
  top: 7px;
  right: 4px;
  display: none;
}

.show-quantity {
  display: block;
}

.hide {
  display: none;
}

@media (min-width: 480px) {
    input[type=search] {
    width: 170px;
  }
}

@media (min-width: 768px) {
    input[type=search] {
    width: 220px;
  }
}

@media (min-width: 980px) {

}
</style>

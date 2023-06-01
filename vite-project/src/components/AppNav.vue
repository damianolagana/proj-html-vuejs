<script >
import { store } from '../data/store';



export default {
  name: "AppNavBar",
  data() {
    return {
      store
    };
  },
  methods: {},

}

</script>

<template>
  <div id="navBar" class="container flex">
    <div class="navLogo">
      <img src="../assets/img/dark-logo.png" alt="">
    </div>
    <div class="flex justifySpaceB navOptions">
      <div v-for="option in store.navBar">
        {{ option }}
        <font-awesome-icon width="10px" :icon="['fas', 'chevron-down']" />
      </div>
      <div class="flex justifySpaceB alignCenter w35">
        <font-awesome-icon class="fontIcon" :icon="['fas', 'cart-shopping']" />
        <font-awesome-icon class="fontIcon" :icon="['far', 'circle-user']" />
        <div class="flex searchBox">
          <input type="text" placeholder="Search">
          <div class="flex textCenter alignCenter justifyCenter">
            <font-awesome-icon :icon="['fas', 'magnifying-glass']" />

          </div>

        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/general.scss";

#navBar {
  color: white;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
  height: 100px;

  .navLogo {
    filter: brightness(6);
    width: 13%;

    img {
      width: 100%;
    }
  }

  .navOptions {
    width: 75%;
    height: 100%;
    align-items: center;
  }
}

.fontIcon {
  font-size: 17px;
}

input {
  height: 50px;
  border: none;
  padding: 10px;
  width: 85%;
  font-size: 16px;
}

.searchBox {
  border: 1px solid;
  border-radius: 5%;

  div {
    height: 50px;
    width: 30%;
    background-color: white;
    color: green;
    font-size: 20px;
  }
}

.w35 {
  width: 35%;
}
</style>


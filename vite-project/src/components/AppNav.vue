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
    <div class="flex justifySpaceB">
      <div v-for="option in store.navBar">{{ option }}</div>
      <div>
        <font-awesome-icon :icon="['fas', 'cart-shopping']" />
        <font-awesome-icon :icon="['far', 'circle-user']" />
      </div>
    </div>

    <div>
      <input type="text" placeholder="Search">
      <font-awesome-icon :icon="['fas', 'magnifying-glass']" />
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

  .navLogo {
    filter: brightness(6);

  }
}
</style>


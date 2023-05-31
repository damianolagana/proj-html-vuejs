<script >
import AppNav from './AppNav.vue';




export default {
  name: "AppHeader",
  components: {
    AppNav,

  },
  data() {
    return {

    };
  },
  methods: {},

}

</script>

<template>
  <header>
    <AppNav />


  </header>
</template>

<style lang="scss" scoped>
header {
  height: 800px;
  background-color: #1f1f52;
  background-size: cover;



}
</style>

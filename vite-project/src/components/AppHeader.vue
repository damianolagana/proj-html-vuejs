<script >
import { isSVGTag } from '@vue/shared';



export default {
  name: "AppHeader",
  data() {
    return {};
  },
  methods: {},
  components: { isSVGTag }
}

</script>

<template>
  <header>
    <div class="jumboSvg">


    </div>

    <!-- <img src="../assets/img/jumbotron-background-wave-medium.svg" alt="">
              <img src="../assets/img/jumbotron-background-wave-small.svg" alt=""> -->
  </header>
</template>

<style lang="scss" scoped>
header {
  height: 800px;
  background-color: #1f1f52;
  background-size: cover;
  position: relative;

  .jumboSvg {
    background-image: url(../assets/img/jumbotron-background-wave-big.svg);
  }
}
</style>

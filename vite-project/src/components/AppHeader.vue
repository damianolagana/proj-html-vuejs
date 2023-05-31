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
    <section id="headerSection">
      <div>
        <h1>Learn At Your Own Pace!</h1>
        <p>Get teamed up with people of the same will</p>
        <button class="greenButton">Get started for free</button>
      </div>
      <div>
        <img src="../assets/img/home-6-hero-left-person-244x300.png" alt="">
        <img src="../assets/img/home-6-hero-poster-final.jpg" alt="">
        <img src="../assets/img/home-6-hero-right-person-195x300.png" alt="">
      </div>
    </section>

  </header>
</template>

<style lang="scss" scoped>
header {
  height: 800px;
  background-color: #1f1f52;
  background-size: cover;
  color: white;


}

#headerSection {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 2rem;

  div {
    text-align: center;
    line-height: 2rem;
    margin-top: 5rem;

    h1 {
      font-size: 40px;
    }

    p {
      padding: 20px;
    }
  }
}
</style>

<script >





export default {
  name: "AppHelpSection",
  components: {


  },
  data() {
    return {


    };
  },
  methods: {},

}

</script>

<template>
  <section>
    <div class="container">
      <div class="HelpBoxTitle textCenter">
        <h3>WANNA TRANSFORM YOUR LIFE?</h3>
        <h1>Glad to <span>Help you</span> Learn</h1>
      </div>
      <div class="cardBox">
        <div class="helpCard">
          <div class="helpIcon">
            <font-awesome-icon :icon="['far', 'flag']" />

          </div>
          <h3>Idea Discussion</h3>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Eos praesentium repudiandae ullam!</p>
        </div>

        <div class="helpCard">
          <div class="helpIcon">
            <font-awesome-icon :icon="['fas', 'gear']" />

          </div>
          <h3> Web Development</h3>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Eos praesentium repudiandae ullam!</p>
        </div>

        <div class="helpCard">
          <div class="helpIcon">
            <font-awesome-icon :icon="['far', 'life-ring']" />

          </div>
          <h3>System Administration</h3>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Eos praesentium repudiandae ullam!</p>
        </div>

        <div class="helpCard">
          <div class="helpIcon">
            <font-awesome-icon :icon="['fas', 'display']" />

          </div>
          <h3>Graphic Design</h3>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Eos praesentium repudiandae ullam! </p>
        </div>
      </div>
      <div class="helpImgBox">
        <img src="../assets/img/home-6-services-image.png" alt="">
      </div>
    </div>


  </section>
  <div>
    <div class="container">
      <div class="certificationBox">
        <h4>Start today for getting <span>Online Certification</span></h4>
        <h2>You can be your own guiding star with our help!</h2>
        <button class="greenButton">Get started now</button>
      </div>

    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/general.scss";

section {
  background: rgb(209, 218, 218);
  background: linear-gradient(0deg, rgba(209, 218, 218, 1) 0%, rgba(255, 255, 255, 1) 40%);
}

.HelpBoxTitle {
  line-height: 3rem;
  padding: 3rem 0;


  h3 {
    color: grey;
    font-size: 12px;
  }

  h1 {
    font-size: 40px;

    span {
      color: #20ad96;
      font-weight: 400;
    }
  }
}

.cardBox {
  display: flex;
  padding: 2rem 0;
}

.helpCard {
  width: calc(100%/4);
  padding-right: 2rem;

  .helpIcon {
    font-size: 60px;
    color: rgb(31, 30, 30);
  }

  h3 {
    padding: 1rem 0;
  }

  p {
    color: rgb(100, 97, 97);
  }

}

.helpImgBox {
  position: relative;
  height: 500px;

  img {
    position: absolute;
    top: 5rem;
  }
}

.certificationBox {
  text-align: center;
  padding: 6rem 0 6rem 0;
  line-height: 1.5rem;

  h4 {
    span {
      color: #20ad96;
      font-weight: 500;
    }
  }

  h2 {
    padding-bottom: 2rem;
  }

  button {
    width: 20%;
  }
}
</style>

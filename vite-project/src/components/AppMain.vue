<script>
import AppCourses from "./AppCourses.vue"
import AppTalkAbout from "./AppTalkAbout.vue";
import AppBlogSection from "./AppBlogSection.vue";
import AppHelpSection from "./AppHelpSection.vue";

export default {
  name: "AppMain",
  components: {
    AppCourses,
    AppTalkAbout,
    AppBlogSection,
    AppHelpSection
  },
  data() {
    return {
      statistic: [
        {
          figure: "1.926",
          item: "FINISHED SESSIONS"
        },
        {
          figure: "3.092+",
          item: "ENROLLED LEARNERS"
        },
        {
          figure: "200",
          item: "ONLINE INSTRUCTORS"
        },
        {
          figure: "100%",
          item: "SATISFACTION RATE"
        },



      ]
    }
  },
  methods: {

  }
}

</script>

<template>
  <section class="container">
    <div class="quoteBox">

      <div class="quote">
        <h2>Let passion and determination be the guide along the way and develop at your own pace that's comfortable</h2>
        <div class="author">
          <h4>FANNIE MORENO</h4>
          <p>/Founder & CEO</p>
        </div>
      </div>
      <div class="statistics">
        <div v-for="stat in statistic">
          <span>{{ stat.figure }}</span>
          <p>{{ stat.item }}</p>
        </div>


      </div>
    </div>

    <div class="cardBox">
      <div class="cardSet">
        <div class="card">
          <h3>Graphic Design</h3>
          <p>Have a passion for graphics and arts? Show your talents with confidence and self-assertiveness</p>
          <div>
            <img src="../assets/img/home-6-service-image-01.png" alt="">

          </div>
        </div>
        <div class="card">
          <div>
            <img src="../assets/img/home-6-service-image-02.png" alt="">

          </div>
          <h3>Business Administration</h3>
          <p>have a passion for graphics and arts? Show your talents with confidence and self-assertiveness</p>
        </div>


      </div>
      <div class="cardSet cardSet2">
        <div class="card">
          <h3>Idea Discussion</h3>
          <p>have a passion for graphics and arts? Show your talents with confidence and self-assertiveness</p>
          <div>
            <img src="../assets/img/home-6-service-image-03.png" alt="">

          </div>
        </div>
        <div class="card">
          <div>
            <img src="../assets/img/home-6-service-image-04.png" alt="">

          </div>
          <h3>Web Development</h3>
          <p>have a passion for graphics and arts? Show your talents with confidence and self-assertiveness</p>
        </div>

      </div>
      <div class="servicesBox">
        <h4>TOGETHER WE CAN CREATE</h4>
        <h1>Services We <span>Can Provide</span> For My Clients</h1>
        <ul>
          <li>Select & customize courses to your preferences</li>
          <li>Change the tutor and make arrangements</li>
          <li>Participate in events to join others</li>
          <li>Get the desired certificate delivered at house</li>
        </ul>
        <button class="greenButton">Get started for free</button>
      </div>
    </div>
  </section>
  <AppCourses />
  <AppTalkAbout />
  <AppBlogSection />
  <AppHelpSection />
</template>

<style lang="scss" scoped>
@use "../styles/general.scss";


.quoteBox {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 5rem;

  .quote {
    text-align: center;
    width: 52%;
    margin-top: 2rem;
    padding: 3rem;
    line-height: 2.5rem;
  }

  .author {
    padding: 2rem;
    line-height: 2rem;

    h4 {
      font-size: smaller;
    }

    p {
      color: gray;
      font-size: small;
    }
  }
}

.statistics {
  display: flex;
  width: 100%;
  justify-content: space-around;

  div {
    text-align: center;
    line-height: 2rem;

    span {
      font-size: 30px;
      font-weight: 800;
      color: #20ad96;
    }

    p {
      font-size: smaller;
      font-weight: 600;
      color: #696969;
    }
  }
}

.cardBox {
  display: flex;
  margin-top: 6rem;


  .card {
    background-color: white;
    box-shadow: 1px 2px 15px #889999;
    padding: 30px 20px 0 20px;
    line-height: 1.5rem;
    margin: 0 20px 30px 0;


    h3 {
      padding: 10px;
    }

    p {
      padding-bottom: 10px;
    }

    div {
      height: 220px;

      img {
        display: block;
        width: 100%;
        object-fit: contain;
        height: 100%;
      }
    }

  }

}



.cardSet {
  width: 23%;
}

.cardSet2 {
  margin-top: 4rem;
}

.servicesBox {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-left: 3rem;

  h4 {
    padding: 10px;
    font-size: 12px;
    color: grey;
  }

  h1 {
    padding: 10px;
    width: 46%;
    font-size: 2rem;

    span {
      color: #20ad96;
    }
  }

  ul {
    list-style-type: none;
    padding: 20px;
    line-height: 2rem;
    color: grey;
  }

  button {
    width: 30%;
  }
}
</style>

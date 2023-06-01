<script >
import { store } from '../data/store';




export default {
  name: "AppCourses",
  components: {


  },
  data() {
    return {
      store
    };
  },
  methods: {},

}

</script>

<template>
  <section>
    <div class="container">
      <div class="courseBoxTitle textCenter">
        <h3>CHOOSE A COURSE TO GET STARTED</h3>
        <h1>Latest Featured <span>Courses</span></h1>
      </div>
      <div class="courseBox">
        <div class="courseCard" v-for="courseCard in store.courses">
          <div class="imgCourse">
            <img :src="courseCard.img_Path" alt="">
          </div>
          <div class="courseInfo lineHeight2rem">
            <h3>{{ courseCard.price }}</h3>
            <p>{{ courseCard.title }}</p>
            <div class="courseIcons">
              <div>
                <font-awesome-icon :icon="['far', 'file-lines']" /> {{ courseCard.lessons }}
              </div>
              <div>
                <font-awesome-icon :icon="['far', 'user']" /> {{ courseCard.students }}
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="buttonCourses textCenter">
        <button class="greenButton">View all courses <font-awesome-icon :icon="['fas', 'arrow-right']" /></button>
      </div>

    </div>
  </section>
</template>

<style lang="scss" scoped>
@use "../styles/general.scss";


section {
  background-color: #f5f7fa;
  margin-top: 4rem;
}

.courseBoxTitle {
  line-height: 3rem;
  padding-top: 4rem;

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

.courseBox {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  margin-top: 4rem;

  .courseCard {
    display: flex;
    width: calc(100%/2);
    align-items: center;
    padding-bottom: 4rem;

    .imgCourse {
      width: 26%;

      img {
        width: 100%;
        display: block;
        height: 151px;
        border-radius: 50%;
        object-fit: cover;
      }
    }

    .courseInfo {
      padding-left: 30px;

      h3 {
        color: #20ad96;
        font-weight: 800;
      }

      p {
        font-weight: 600;
        font-size: 18px;
        width: 85%;
      }

      .courseIcons {
        display: flex;
        align-items: center;
        justify-content: space-between;
        width: 75%;
        color: grey;
      }

    }
  }
}

.buttonCourses {
  padding-bottom: 4rem;
}

button {
  width: 20%;
}
</style>

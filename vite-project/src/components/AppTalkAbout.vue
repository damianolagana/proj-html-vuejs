<script >





export default {
  name: "AppTalkAbout",
  components: {


  },
  data() {
    return {
      clientLogos: [
        { logoPath: "/img/client-logo-colored-01.png" },
        { logoPath: "/img/client-logo-colored-02.png" },
        { logoPath: "/img/client-logo-colored-03.png" },
        { logoPath: "/img/client-logo-colored-04.png" },
        { logoPath: "/img/client-logo-colored-05.png" },
        { logoPath: "/img/client-logo-colored-06.png" }

      ]
    };
  },
  methods: {},

}

</script>

<template>
  <section>
    <div class="container">
      <div class="talkBox">
        <h1>Why People Talk About <span>MaxCoach</span>?</h1>
        <div class="testimonialBox">
          <div class="imgTestimonial">
            <img src="../assets/img/testimonial-avata-02.jpg" alt="">
          </div>
          <div class="testimonialSpeech">
            <p>I am free to learn at my own pace, follow my own schedule and choose the subject I like, Great study portal
              for people like me.</p>
            <div class="author">
              <h4>MINA HOLLACE</h4>
              <p>/Freelancer</p>
            </div>
          </div>
        </div>
        <div class="clientBox">
          <div v-for="logo in this.clientLogos">
            <img :src="logo.logoPath" alt="">
          </div>
        </div>
      </div>

    </div>
  </section>
</template>

<style lang="scss" scoped>
@use "../styles/general.scss";

.talkBox {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  h1 {
    font-size: 40px;
    padding: 3rem 0;

    span {
      color: #20ad96;
      font-weight: 400;
    }
  }

  .testimonialBox {
    display: flex;
    padding: 2rem 0;
    justify-content: center;
    align-items: center;

    .testimonialSpeech {
      width: 42%;
      padding-left: 4rem;
      line-height: 2rem;
      font-size: 23px;

      .author {
        padding-top: 20px;

        h4 {
          font-size: 12px;
          font-weight: 800;
        }

        p {
          font-size: 13px;
          color: gray;
        }
      }
    }

    .imgTestimonial {
      width: 13%;

      img {
        width: 100%;
        display: block;
        border-radius: 50%;
        object-fit: cover;
      }
    }
  }
}

.clientBox {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 72%;
  padding: 2rem 0;
}
</style>

<script>


export default {
  name: "AppMain",
  data() {
    return {

    }
  },
  methods: {

  }
}

</script>

<template>
  <div class="container">
    <div class="quoteBox">

      <div class="quote">
        <h2>Let passion and determination be the guide along the way and develop at your own pace that's comfortable</h2>
        <div class="author">
          <h4>FANNIE MORENO</h4>
          <p>/Founder & CEO</p>
        </div>
      </div>
      <div class="statistics">
        <div>
          <span>1.926</span>
          <p>FINISHED SESSIONS</p>
        </div>
        <div>
          <span>3.092+</span>
          <p>ENROLLED LEARNERS</p>
        </div>
        <div>
          <span>200</span>
          <p>ONLINE INSTRUCTORS</p>
        </div>
        <div>
          <span>100%</span>
          <p>SATISFACTION RATE</p>
        </div>

      </div>
    </div>

  </div>
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
</style>

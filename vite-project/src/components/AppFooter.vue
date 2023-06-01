<script >


export default {
  name: "AppFooter",
  data() {
    return {
      addressInfo: {
        street: "382 NE 191st St # 87394 Miami, FL 33179-3899",
        phoneNumber: "+1(305) 547-9909 (9am - 5pm EST, Monday - Friday)",
        mail: "support@maxcoach.com"

      },
      exploreInfo: [
        "Start here",
        "Blog",
        "About us",
        "Success story",
        "Courses",
        "Contact us"
      ],
      information: [
        "Membership",
        "Purchase guide",
        "Privacy policy",
        "Terms of service"
      ]


    }



  },
  methods: {

  }
}

</script>

<template>
  <section>
    <div class="container">
      <div class="footerBox flex">
        <div class="addressInfo">
          <h4>Address</h4>
          <div class="lineHeight2rem flex flexCol">
            <span>{{ this.addressInfo.street }}</span>
            <span>{{ this.addressInfo.phoneNumber }}</span>
            <span>{{ this.addressInfo.mail }}</span>

          </div>
          <div class="socialBox">
            <font-awesome-icon :icon="['fab', 'square-facebook']" />
            <font-awesome-icon :icon="['fab', 'twitter']" />
            <font-awesome-icon :icon="['fab', 'instagram']" />
            <font-awesome-icon :icon="['fab', 'linkedin']" />
          </div>
        </div>
        <div class="exploreInfoBox">
          <div class="exploreInfo ">
            <h4>Explore</h4>
            <div class="lineHeight2rem flex flexCol flexWrap">
              <span v-for="explore in exploreInfo">{{ explore }}</span>
            </div>
          </div>
          <div class="info ">
            <h4>Information</h4>
            <div class="lineHeight2rem flex flexCol">
              <span v-for="info in information">{{ info }}</span>

            </div>
          </div>
        </div>
      </div>
      <div class="copyright">
        <font-awesome-icon :icon="['far', 'copyright']" /> 2020 Maxcoach. All Rights Reserved
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use "../styles/general.scss";



section {
  background-color: #f8f8f8;
}

h4 {
  padding-bottom: 1.5rem;
}

span {
  color: rgb(82, 80, 80);
  font-size: 13px;
  font-weight: 600;
}


.socialBox {
  display: flex;
  justify-content: space-between;
  width: 50%;
  padding-top: 1.5rem;
  font-size: 25px;
  color: grey;
  cursor: pointer;

}

.footerBox {
  display: flex;
  padding: 3rem 0;
  justify-content: space-around;

  .addressInfo {
    width: 30%;
  }

  .exploreInfoBox {
    display: flex;
    justify-content: flex-end;
    width: 40%;

    .exploreInfo {
      width: 50%;


      div {
        height: 100px;
      }
    }

    .info {
      padding-left: 2rem;
    }
  }
}

.copyright {
  text-align: center;
  padding: 2rem 0;
  color: grey;
  font-size: 13px;
}
</style>

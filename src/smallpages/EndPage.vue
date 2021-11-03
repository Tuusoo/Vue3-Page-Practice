<template>
  <div class="green-page">
    <div class="background"></div>
    <div class="start">Let’s Get Started Now</div>
    <div class="title">
      We’ll Help You Overcome Your <br />
      Technology Challenges
    </div>
    <BigButtonVue buttonType="2" />
  </div>
  <div class="contact-page">
    <div class="column-1">
      <img src="../assets/footer-logo.png" class="logo" />
      <div class="describe">
        There are many vari of pass of lorem ipsum availab but the majority have
        suffered in some forms.
      </div>
      <div class="social-apps">
        <div class="app">
          <img src="../assets/svg/twitter.svg" />
        </div>
        <div class="app">
          <img src="../assets/svg/facebook.svg" />
        </div>
        <div class="app">
          <img src="../assets/svg/pinterest.svg" />
        </div>
        <div class="app">
          <img src="../assets/svg/instagram.svg" />
        </div>
      </div>
    </div>
    <div class="column-2">
      <div class="column-title">Links</div>
      <div class="column-2-columns">
        <div class="column-2-column">
          <div class="mini-button">About</div>
          <div class="mini-button">Leadership Team</div>
          <div class="mini-button">IT Blog</div>
          <div class="mini-button">Case Studies</div>
          <div class="mini-button">Locations</div>
        </div>
        <div class="column-2-column">
          <div class="mini-button">Managed IT</div>
          <div class="mini-button">IT Support</div>
          <div class="mini-button">IT Consultancy</div>
          <div class="mini-button">Cloud Computing</div>
        </div>
      </div>
    </div>
    <div class="column-3">
      <div class="column-title">Contact</div>
      <div class="text">
        66 Road Broklyn Street, 600 <br />
        New York, USA
      </div>
      <div class="email">
        <img src="../assets/svg/chat.svg" />
        <div>needhelp@company.com</div>
      </div>
      <div class="email">
        <img src="../assets/svg/people.svg" />
        <div>+ 92 666 888 0000</div>
      </div>
    </div>
    <div class="column-4">
      <div class="column-title">Newsletter</div>
      <div class="text">
        Subscribe to our newsletter for daily <br />
        new and updates
      </div>
      <div class="email-button">
        <input type="email" class="email" placeholder="Email Address"/>
        <span class="send">send</span>
      </div>
    </div>
  </div>
  <div class="copy-right">😈 Plagiarized by Tuusoo~</div>
</template>

<script>
import BigButtonVue from "../components/BigButton.vue";

export default {
  name: "EndPage",
  inheritAttrs: false,
  components: {
    BigButtonVue,
  },
  props: {},
  data() {
    return {};
  },
  computed: {},
  watch: {},
  created() {},
  mounted() {},
  beforeUnmount() {},
  unmounted() {},
  methods: {},
};
</script> 

<style scoped lang="less">
.green-page {
  position: relative;
  height: 500px;
  width: 100%;
  background-color: #42d9be;
  z-index: 1;
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 100px;
  color: #ffffff;
  text-align: center;

  .background {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    z-index: -1;
    background-image: url(../assets/cta-one-bg.jpg);
    background-color: #42d9be;
    background-size: cover;
    background-blend-mode: luminosity;
    opacity: 0.15;
  }

  .start {
    font-family: "Barlow-SemiBold";
    font-size: 18px;
  }

  .title {
    font-family: "Barlow-ExtraBold";
    font-size: 50px;
    margin: 30px 0 50px;
  }
}

.contact-page {
  background: #1b1825;
  padding: 150px 0;
  display: flex;
  justify-content: center;
  color: #ada8ba;

  .column-title {
    font-family: "Barlow-ExtraBold";
    font-size: 20px;
    color: #ffffff;
  }

  .column-1 {
    width: 270px;
    margin-right: 20px;
    .logo {
      width: 150px;
    }

    .describe {
      line-height: 30px;
      font-family: "Barlow-Medium";
      margin-top: 20px;
    }

    .social-apps {
      display: flex;
      margin-top: 30px;

      .app {
        width: 40px;
        height: 40px;
        border-radius: 50%;
        text-align: center;
        padding-top: 12.5px;
        box-sizing: border-box;
        background: #000000;
        margin-right: 10px;

        img {
          width: 15px;
        }
      }
    }
  }

  .column-2 {
    .column-2-columns {
      display: flex;
      align-items: flex-start;
      font-family: "Barlow-Medium";
      margin-top: 40px;

      .column-2-column {
        margin-right: 20px;

        .mini-button {
          line-height: 30px;
          cursor: pointer;
        }
      }
    }
  }

  .column-3 {
    margin-left: 20px;
    .text {
      font-family: "Barlow-Medium";
      margin: 40px 0 30px;
      line-height: 30px;
    }

    .email {
      color: #ffffff;
      font-family: "Barlow-Medium";
      display: flex;
      align-items: center;
      line-height: 30px;

      img {
        width: 15px;
        margin-right: 10px;
      }
    }
  }

  .column-4 {
    margin-left: 100px;
    .text {
      font-family: "Barlow-Medium";
      margin: 40px 0 30px;
      line-height: 30px;
    }

    .email-button {
      display: flex;
      .email {
        height: 70px;
        width: 180px;
        border-radius: 10px 0 0 10px;
        margin: 0;
        border: 0;
        padding-left: 20px;
        box-sizing: border-box;
      }

      .send {
        background: #1989fb;
        display: inline-block;
        height: 70px;
        width: 100px;
        text-align: center;
        color: #ffffff;
        line-height: 70px;
        cursor: pointer;
        font-family: "Barlow-SemiBold";
        letter-spacing: 1px;
        border-radius: 0 10px 10px 0;
        transition: all 0.5s;

        &:hover {
          background: #42D8BD;
        }
      }
    }
  }
}

.copy-right {
  font-family: "Barlow-Medium";
  background: #100D16;
  height: 60px;
  box-sizing: border-box;
  padding: 0 calc((100vw - 1200px) / 2);
  line-height: 60px;
  color: #ada8ba;
}
</style>
<template>
  <div class="improve-innovate">
    <div class="left">
      <div class="column-text">8008 PROJECTS ARE COMPLETED</div>
      <img src="../assets/improve-one-img-1.jpg" class="robot-pic" />
    </div>
    <div class="right">
      <LittleTitleWithGreenLineVue text="IT Technology" />
      <div class="big-title">
        Improve and Innovate <br />
        with Tech Trends
      </div>
      <div class="row">
        <RotateImageVue :image="require('../assets/svg/robot.svg')" />
        <div class="texts">
          <div class="big-text">Artificial Intelligence</div>
          <div class="small-text">
            There are many variations of passages of available but <br />
            the majority have suffered alteration in some form <br />
            injected
          </div>
        </div>
      </div>
      <div class="gray-line"></div>
      <div class="row">
        <RotateImageVue :image="require('../assets/svg/electric.svg')" />
        <div class="texts">
          <div class="big-text">Augmented Reality</div>
          <div class="small-text">
            There are many variations of passages of available but <br />
            the majority have suffered alteration in some form <br />
            injected
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import LittleTitleWithGreenLineVue from "../components/LittleTitleWithGreenLine.vue";
import RotateImageVue from "../components/RotateImage.vue";

export default {
  name: "ImproveAndInnovate",
  inheritAttrs: false,
  components: {
    LittleTitleWithGreenLineVue,
    RotateImageVue,
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
.improve-innovate {
  position: relative;
  width: 100%;
  background-color: #1b1825;
  background-image: url(../assets/improve-one-bg.jpg);
  background-blend-mode: luminosity;
  background-size: cover;
  background-attachment: fixed;
  display: flex;

  .left {
    position: relative;
    width: 55%;

    .column-text {
      position: absolute;
      right: 400px;
      top: 100px;
      background: #42d9be;
      width: 400px;
      text-align: center;
      border-radius: 10px 10px 0 0;
      font-family: "Barlow-ExtraBold";
      color: #ffffff;
      line-height: 60px;
      font-size: 14px;
      letter-spacing: 2px;
      transform: rotate(-90deg);
    }

    .robot-pic {
      position: absolute;
      right: 20px;
      top: -70px;
      width: 550px;
    }
  }

  .right {
    width: 45%;
    padding: 100px;

    .big-title {
      font-family: "Barlow-ExtraBold";
      font-size: 50px;
      color: #ffffff;
    }

    .row {
      display: flex;
      align-items: flex-start;
      margin-top: 40px;

      .texts {
        display: inline-block;
        margin-left: 20px;

        .big-text {
          font-family: "Barlow-ExtraBold";
          font-size: 25px;
        }

        .small-text {
          font-family: "Barlow-Medium";
          line-height: 30px;
          color: #7b7981;
        }
      }
    }

    .gray-line {
      width: 400px;
      border-bottom: 1px solid #dae3e9;
      margin-top: 40px;
    }
  }
}
</style>
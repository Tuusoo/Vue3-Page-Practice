<template>
  <div class="know-about-us">
    <div class="image-area">
      <div class="blocks">
        <div class="green"></div>
        <div class="blue"></div>
      </div>
      <img src="../assets/about-one-img-1.jpg" class="big-img" />
      <img src="../assets/about-one-small-img.jpg" class="small-img" />
    </div>
    <div class="text-area">
      <LittleTitleWithGreenLineVue text="Get to Know About us" />
      <div class="big-title">
        The Leading IT Solutions <br />
        Company & Your Partner <br />
        for Innovations
      </div>
      <div class="gray-text">
        There are many variations of passages of Lorem Ipsum available, but the
        <br />
        majority have suffered alteration in some form, by injected humour, or
        <br />
        randomised words which don't look even.
      </div>
      <div class="check-list">
        <div class="list-item">
          <img src="../assets/svg/check.svg" />
          <span>Take a look at our round up of the best shows</span>
        </div>
        <div class="list-item">
          <img src="../assets/svg/check.svg" />
          <span>It has survived not only five centuries</span>
        </div>
        <div class="list-item">
          <img src="../assets/svg/check.svg" />
          <span>Lorem Ipsum has been the ndustry standard dummy text</span>
        </div>
      </div>
      <div class="gray-line"></div>
      <div class="introduce-area">
        <RotateImageVue :image="require('../assets/svg/computer.svg')" />
        <span>
          We Run all Kinds of IT Solutions & Services <br />
          that Vow your Success
        </span>
      </div>
      <BigButtonVue />
    </div>
  </div>
</template>

<script>
import LittleTitleWithGreenLineVue from "../components/LittleTitleWithGreenLine.vue";
import RotateImageVue from "../components/RotateImage.vue";
import BigButtonVue from "../components/BigButton.vue";

export default {
  name: "KnowAboutUs",
  inheritAttrs: false,
  components: {
    LittleTitleWithGreenLineVue,
    RotateImageVue,
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
.know-about-us {
  position: relative;
  display: flex;
  box-sizing: border-box;
  padding: 150px calc((100vw - 1300px) / 2);
  background: #fefefe;

  .image-area {
    position: relative;
    width: 50%;
    display: flex;

    .blocks {
      margin: 0 20px;

      div {
        width: 30px;
        height: 200px;
        border-radius: 8px;
        box-sizing: border-box;
        margin-bottom: 20px;

        &.green {
          background: #42d9be;
        }

        &.blue {
          background: #1989fb;
        }
      }
    }

    .big-img {
      width: 500px;
    }

    .small-img {
      width: 350px;
      position: absolute;
      bottom: -80px;
      left: -50px;
    }
  }

  .text-area {
    width: 50%;
    position: relative;
    transform: translate(10px, 0);

    .big-title {
      font-family: "Barlow-ExtraBold";
      font-size: 50px;
      margin-top: 10px;
    }

    .gray-text {
      font-family: "Barlow-Medium";
      font-size: 18px;
      line-height: 30px;
      color: #7b7981;
      margin-top: 20px;
    }

    .check-list {
      border-left: 2px solid #1989fb;
      margin-top: 40px;

      .list-item {
        margin: 10px 0;

        img {
          width: 20px;
          margin: 0 20px;
        }

        span {
          font-family: "Barlow-Medium";
          font-size: 18px;
        }
      }
    }

    .gray-line {
      width: 85%;
      height: 0;
      border-bottom: 1px solid #dae3e9;
      margin-top: 50px;
    }

    .introduce-area {
      margin: 30px 0;

      span {
        font-family: "Barlow-SemiBold";
        display: inline-block;
        font-size: 18px;
        margin-left: 20px;
        line-height: 30px;
      }
    }
  }
}
</style>
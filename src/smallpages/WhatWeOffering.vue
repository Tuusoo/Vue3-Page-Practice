<template>
  <div class="what-we-offering">
    <LittleTitleWithGreenLineVue text="Wide Range of Services" />
    <div class="bit-title">What We’re Offering</div>
    <div class="three-block-area">
      <OfferingCardVue />
      <OfferingCardVue />
      <OfferingCardVue />
    </div>
  </div>
  <div class="blue-area">
    <img src="../assets/share-the-joy-map.png" class="left-pic" />
    <div class="title">
      Share the Joy of Achieving <br />
      Glorious Moments & Climbing <br />
      Up the Top
    </div>
    <BigButtonVue buttonType="2" />
    <img src="../assets/share-the-joy-shape-1.png" class="share-arrow">
    <img src="../assets/share-the-joy-img-1.png" class="man">
  </div>
</template>

<script>
import LittleTitleWithGreenLineVue from "../components/LittleTitleWithGreenLine.vue";
import OfferingCardVue from "../components/OfferingCard.vue";
import BigButtonVue from "../components/BigButton.vue";

export default {
  name: "WhatWeOffering",
  inheritAttrs: false,
  components: {
    LittleTitleWithGreenLineVue,
    OfferingCardVue,
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
.what-we-offering {
  background: #eef3f7;
  padding: 100px 0;
  display: flex;
  flex-direction: column;
  align-items: center;

  .bit-title {
    font-family: "Barlow-ExtraBold";
    font-size: 50px;
  }

  .three-block-area {
    width: 1185px;
    display: flex;
    justify-content: space-between;
    margin-top: 50px;
  }
}

.blue-area {
  position: relative;
  height: 500px;
  background: #1989fb;
  box-sizing: border-box;
  border-radius: 10px;
  padding: 110px calc((100vw - 1200px) / 2);

  .left-pic {
    position: absolute;
    left: 0;
    top: 0;
    height: 100%;
    mix-blend-mode: lighten;
    opacity: 0.75;
    -webkit-user-drag: none;
  }

  .title {
    font-family: "Barlow-ExtraBold";
    font-size: 50px;
    color: #ffffff;
    margin-bottom: 60px;
  }

  .share-arrow {
    width: 100px;
    transform: translate(20px, -40px);
    animation: shakeArrow 2s infinite;
  }

  @keyframes shakeArrow {
    0% {
      transform: translate(20px, -40px) rotateZ(-2deg);
    }
    50% {
      transform: translate(20px, -40px) rotateZ(2deg);
    }
    100% {
      transform: translate(20px, -40px) rotateZ(-2deg);
    }
  }

  .man {
    position: absolute;
    right: calc((100vw - 1500px) / 2);
    bottom: 0;
    height: 560px;
    animation: shakeMan 5s infinite;
  }

  @keyframes shakeMan {
    0% {
      transform: translate(-5px, 0);
    }
    50% {
      transform: translate(5px, 0);
    }
    100% {
      transform: translate(-5px, 0);
    }
  }
}
</style>
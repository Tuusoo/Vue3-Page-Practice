<template>
  <div class="cover-page">
    <img :src="backGrounds[currentPage]" class="background-img" />
    <div class="title-area">
      <div class="page-title">
        Better Solution at <br />
        Your Fingertips
      </div>
      <div class="small-title">
        We’ve One Mission to be the Best IT Software Company in UK
      </div>
      <BigButtonVue />
    </div>
  </div>
</template>

<script>
import BigButtonVue from "../components/BigButton.vue";

export default {
  name: "",
  inheritAttrs: false,
  components: {
    BigButtonVue,
  },
  props: {},
  data() {
    return {
      currentPage: 0,
      backGrounds: [
        require("../assets/main-slider-1-1.jpg"),
        require("../assets/main-slider-1-2.jpg"),
        require("../assets/main-slider-1-3.jpg"),
      ],
    };
  },
  computed: {},
  watch: {
    currentPage(newVal) {
      if (newVal > 2) {
        this.currentPage = 0;
        return;
      }
    },
  },
  created() {},
  mounted() {},
  beforeUnmount() {},
  unmounted() {},
  methods: {},
};
</script> 

<style scoped lang="less">
.cover-page {
  position: relative;
  box-sizing: border-box;
  padding: 0 calc((100vw - 1150px) / 2);
  width: 100vw;
  height: 100vh;
  background: #1b1825;

  .background-img {
    height: 100%;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    mix-blend-mode: luminosity;
    opacity: .3;
  }

  .title-area {
    position: absolute;
    top: 50vh;
    transform: translate(0, -50%);
    color: #ffffff;

    .page-title {
      font-family: "Barlow-ExtraBold";
      font-size: 85px;
    }

    .small-title {
      font-family: "Barlow-SemiBold";
      font-size: 20px;
      margin: 20px 0 50px 0;
    }
  }
}
</style>
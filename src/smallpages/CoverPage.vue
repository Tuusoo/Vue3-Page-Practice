<template>
  <div class="cover-page">
    <img :src="backGrounds[currentPage]" :class="backgroundImg" />
    <div :class="titleArea">
      <div class="page-title">
        Better Solution at <br />
        Your Fingertips
      </div>
      <div class="small-title">
        We’ve One Mission to be the Best IT Software Company in UK
      </div>
      <BigButtonVue />
    </div>
    <div class="switch-button">
      <img src="../assets/svg/arrow-left.svg" @click="toPreviousPage" />
      <img src="../assets/svg/arrow-right.svg" @click="toNextPage" />
    </div>
    <img src="../assets/page-header-shape.png" :class="electricFadeIn" />
    <div class="three-point">
      <span
        v-for="(i, index) in backGrounds"
        :key="i"
        :class="index == currentPage ? 'big-point' : ''"
        @click="turnToPage(index)"
      ></span>
    </div>
  </div>
  <div class="logo-banner">
    <div class="logo-container">
      <div class="img-container" v-for="i in logos" :key="i">
        <img :src="i" @mouseover="changeToWhite" @mouseout="changeToGray" />
      </div>
    </div>
    <div class="cards">
      <CardVue v-for="i in cards" :key="i" :title="i" />
    </div>
  </div>
  <div class="gray-area">
    <div class="text">
      IT services built specifically for your business.
      <a href="#">Find Your Solution</a>
    </div>
    <div class="gray-line"></div>
  </div>
</template>

<script>
import BigButtonVue from "../components/BigButton.vue";
import CardVue from "../components/Card.vue";

export default {
  name: "CoverPage",
  inheritAttrs: false,
  components: {
    BigButtonVue,
    CardVue,
  },
  props: {},
  data() {
    return {
      currentPage: -1,
      backGrounds: [
        require("../assets/main-slider-1-1.jpg"),
        require("../assets/main-slider-1-2.jpg"),
        require("../assets/main-slider-1-3.jpg"),
      ],
      switchTimer: {},
      animateTimer: {},
      electricFadeIn: "electric",
      titleArea: "title-area",
      backgroundImg: "background-img",
      logos: [
        require("../assets/brand-1-1.png"),
        require("../assets/brand-1-2.png"),
        require("../assets/brand-1-3.png"),
        require("../assets/brand-1-4.png"),
        require("../assets/brand-1-5.png"),
        require("../assets/brand-1-6.png"),
      ],
      cards: ["IT Management", "Cyber Security", "PC Computing"],
    };
  },
  computed: {},
  watch: {
    currentPage(newVal) {
      this.clearTimer();
      clearTimeout(this.animateTimer);
      if (newVal > 2) {
        this.currentPage = 0;
        return;
      }
      if (newVal < 0) {
        this.currentPage = 2;
        return;
      }
      this.electricFadeIn = "electric";
      this.titleArea = "title-area";
      this.backgroundImg = "background-img";
      this.animateTimer = setTimeout(() => {
        this.electricFadeIn = "electric fadeInLeft";
        this.titleArea = "title-area fadeInUp";
        this.backgroundImg = "background-img fadeInBigger";
      }, 100);
      this.setTimer();
    },
  },
  created() {},
  mounted() {
    this.setTimer();
    this.currentPage = 0;
  },
  beforeUnmount() {
    this.clearTimer();
  },
  unmounted() {},
  methods: {
    setTimer() {
      this.switchTimer = setInterval(() => {
        this.currentPage++;
      }, 4000);
    },
    clearTimer() {
      clearInterval(this.switchTimer);
    },
    toNextPage() {
      this.currentPage++;
    },
    toPreviousPage() {
      this.currentPage--;
    },
    turnToPage(index) {
      this.currentPage = index;
    },
    changeToWhite(e) {
      e.currentTarget.style.opacity = "1";
    },
    changeToGray(e) {
      e.currentTarget.style.opacity = "0.3";
    },
  },
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
    opacity: 0.3;
    -webkit-user-drag: none;
    &.fadeInBigger {
      animation: fadeInBigger 4s;
    }
  }

  @keyframes fadeInBigger {
    from {
      height: 100%;
    }
    to {
      height: 110%;
    }
  }

  .title-area {
    position: absolute;
    top: 60vh;
    opacity: 0.5;
    transform: translate(0, -50%);
    color: #ffffff;
    &.fadeInUp {
      animation: fadeInUp 4s;
    }

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

  @keyframes fadeInUp {
    0% {
      top: 60vh;
      opacity: 0.5;
    }
    50% {
      top: 50vh;
      opacity: 1;
    }
    100% {
      top: 50vh;
      opacity: 1;
    }
  }

  .switch-button {
    position: absolute;
    top: 50%;
    right: calc((100vw - 1150px) / 2);
    transform: translate(0, -50%);
    display: flex;
    flex-direction: column;
    z-index: 10;

    img {
      width: 80px;
      margin: 5px;
      cursor: pointer;
      -webkit-user-drag: none;
    }
  }

  .electric {
    position: absolute;
    bottom: 0;
    right: -200px;
    opacity: 0;
    height: 400px;

    &.fadeInLeft {
      animation: fadeInLeft 4s;
    }
  }

  .three-point {
    position: absolute;
    bottom: 50px;
    width: 50px;
    display: flex;
    align-items: center;
    justify-content: space-between;

    span {
      display: inline-block;
      width: 10px;
      height: 10px;
      border-radius: 50%;
      box-sizing: border-box;
      background: #76747c;
      transition: all 0.5s;
      cursor: pointer;
      &.big-point {
        width: 12px;
        height: 12px;
        background: #ffffff;
      }
    }
  }

  @keyframes fadeInLeft {
    0% {
      right: -200px;
      opacity: 0;
    }
    50% {
      right: 0;
      opacity: 1;
    }
    100% {
      right: 0;
      opacity: 1;
    }
  }
}

.logo-banner {
  position: relative;
  background: #1b1825;
  box-sizing: border-box;
  height: 400px;
  padding: 100px calc((100vw - 1200px) / 2) 200px;

  .logo-container {
    display: flex;
    justify-content: space-between;
    overflow: scroll;
    width: 1200px;

    &::-webkit-scrollbar {
      display: none;
    }

    .img-container {
      width: 200px;

      img {
        width: 150px;
        opacity: 0.3;
        transition: all 0.5s;
      }
    }
  }

  .cards {
    position: relative;
    z-index: 1;
    width: 1200px;
    display: flex;
    justify-content: space-between;
    transform: translate(0, 100px);
  }
}

.gray-area {
  position: relative;
  height: 200px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: #fefefe;

  .text {
    font-family: "Barlow-Medium";
    color: #7b7981;
    transform: translate(0, 50px);

    a {
      color: #1989fb;
      transition: color 0.5s;
      &:hover {
        color: #42d8bd;
      }
    }
  }

  .gray-line {
    position: absolute;
    bottom: 0;
    left: 50%;
    transform: translate(-50%, 0);
    width: 1200px;
    border-bottom: 1px solid #dae3e9;
  }
}
</style>
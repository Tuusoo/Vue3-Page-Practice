<template>
  <div class="explore-project">
    <LittleTitleWithGreenLineVue text="Our Case Studies" />
    <div class="bit-title">Explore Projects</div>
    <div class="rotate-area" :style="rotateTransition" ref="rotateArea">
      <RotateItemVue v-for="i in rotateItems" :key="i" :backImage="i" />
    </div>
    <div class="three-point">
      <span
        v-for="i in 3"
        :key="i"
        :class="pointClass(i)"
        @click="clickToPage(i)"
      ></span>
    </div>
  </div>
</template>

<script>
import LittleTitleWithGreenLineVue from "../components/LittleTitleWithGreenLine.vue";
import RotateItemVue from "../components/RotateItem";

export default {
  name: "ExploreProjects",
  inheritAttrs: false,
  components: {
    LittleTitleWithGreenLineVue,
    RotateItemVue,
  },
  props: {},
  data() {
    return {
      rotateIndex: 0,
      rotateItems: [
        require("../assets/project-one-img-1.jpg"),
        require("../assets/project-one-img-2.jpg"),
        require("../assets/project-one-img-1.jpg"),
        require("../assets/project-one-img-2.jpg"),
        require("../assets/project-one-img-3.jpg"),
        require("../assets/project-one-img-4.jpg"),
        require("../assets/project-one-img-1.jpg"),
        require("../assets/project-one-img-2.jpg"),
        require("../assets/project-one-img-1.jpg"),
        require("../assets/project-one-img-2.jpg"),
      ],
      rotateTimer: null,
    };
  },
  computed: {
    rotateTransition() {
      return `transform: translate(${1060 - this.rotateIndex * 530}px, 0);`;
    },
  },
  watch: {
    rotateIndex(newVal) {
      if (newVal > 5) {
        this.rotateIndex = 0;
      }
      if (newVal < 0) {
        this.rotateIndex = 5;
      }
    },
  },
  created() {},
  mounted() {
    this.rotateTimer = setInterval(() => {
      this.rotateIndex++;
    }, 2000);
  },
  beforeUnmount() {
    clearInterval(this.rotateTimer);
  },
  unmounted() {},
  methods: {
    pointClass(i) {
      if (i == parseInt((this.rotateIndex + 2) / 2)) {
        return "on";
      }
    },
    clickToPage(i) {
      clearInterval(this.rotateTimer);
      this.rotateIndex = (i - 1) * 2;
      this.rotateTimer = setInterval(() => {
        this.rotateIndex++;
      }, 2000);
    },
  },
};
</script> 

<style scoped lang="less">
.explore-project {
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 100px 0;

  .bit-title {
    font-family: "Barlow-ExtraBold";
    font-size: 50px;
  }

  .rotate-area {
    display: flex;
    width: 5300px;
    justify-content: space-around;
    transition: all 0.5s;
    transform: translate(1060px, 0);
    margin-top: 50px;
  }

  .three-point {
    width: 50px;
    height: 50px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-top: 100px;

    span {
      width: 10px;
      height: 10px;
      border-radius: 50%;
      background: #a4a3a8;
      transition: all 0.5s;
      cursor: pointer;

      &.on {
        width: 14px;
        height: 14px;
        background: #42d9be;
      }
    }
  }
}
</style>
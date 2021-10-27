<template>
  <div class="top-menu">
    <img src="../assets/logo-1.png" class="logo" />
    <div class="buttons">
      <TopHeaderButtonVue v-for="i in buttonTexts" :text="i" :key="i" />
    </div>
    <div class="right-area">
      <div class="devider"></div>
      <img src="../assets/svg/fangdajing.svg" />
      <img src="../assets/svg/ren.svg" />
    </div>
  </div>
</template>

<script>
import TopHeaderButtonVue from "../components/TopHeaderButton.vue";

export default {
  name: "",
  inheritAttrs: false,
  components: {
    TopHeaderButtonVue,
  },
  props: {},
  data() {
    return {
      buttonTexts: ["Home", "About", "Services", "Projects", "News", "Contact"],
    };
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
.top-menu {
  box-sizing: border-box;
  padding: 0 calc((100vw - 1300px) / 2);
  height: 100px;
  display: flex;
  align-items: center;

  .logo {
    width: 130px;
    margin-right: 60px;
    cursor: pointer;
  }

  .buttons {
    flex: 1;
  }

  .right-area{
    display: flex;
    align-items: center;
    justify-content: space-between;

    .devider {
      height: 70px;
      border-right: 1px solid #dae3e9;
    }

    img {
      width: 30px;
      margin-left: 25px;
    }
  }
}
</style>
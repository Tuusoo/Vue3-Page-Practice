<template>
  <div class="card">
    <img src="../assets/svg/bulb.svg" />
    <div class="title">{{ title }}</div>
    <div class="text">Lorem ipsum is simply of free text dolor.</div>
  </div>
</template>

<script>
export default {
  name: "Card",
  inheritAttrs: false,
  components: {},
  props: {
    title: String,
  },
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
.card {
  position: relative;
  display: inline-block;
  width: 350px;
  height: 180px;
  box-shadow: 0px 10px 60px 0px rgba(0, 0, 0, 7%);
  border-radius: 10px;
  background: #ffffff;
  img {
    width: 100px;
    position: absolute;
    top: 40px;
    left: 20px;
  }
  .title {
    position: absolute;
    top: 40px;
    left: 130px;
    font-family: "Barlow-SemiBold";
    font-size: 20px;
  }
  .text {
    position: absolute;
    top: 70px;
    left: 130px;
    font-family: "Barlow-Medium";
    color: #7b7981;
    font-size: 14px;
    line-height: 30px;
  }
}
</style>
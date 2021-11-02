<template>
  <div class="talking-about-card">
    <div class="personal-data">
      <img :src="itemData.picture" />
      <div>
        <div class="name">{{ itemData.person }}</div>
        <div class="job">Customer</div>
      </div>
    </div>
    <div class="main-text">
      Lorem ipsum is simply free text dolor sit amet, consectetur notted
      adipisicing elit sed do eiusmod tempor incididunt ut labore et dolore
      text.
    </div>
  </div>
</template>

<script>
export default {
  name: "TalkingAboutCard",
  inheritAttrs: false,
  components: {},
  props: {
    itemData: Object,
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
.talking-about-card {
  width: 470px;
  height: 350px;
  border-radius: 5px;
  background: #ffffff;
  padding: 60px;
  box-sizing: border-box;
  display: inline-block;
  margin: 0 10px;

  .personal-data {
    display: flex;
    align-items: center;
    font-family: "Barlow-Medium";
    line-height: 26px;

    img {
      margin-right: 20px;
    }

    .name {
      font-family: "Barlow-SemiBold";
      font-size: 18px;
    }

    .job {
      color: #1989fb;
    }
  }
  
  .main-text {
    font-family: "Barlow-Light";
    color: #7b7981;
    line-height: 35px;
    font-size: 20px;
    margin-top: 20px;
  }
}
</style>
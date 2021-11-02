<template>
  <div class="rotate-item">
    <img :src="backImage" class="image" />
    <div class="dark-cover"></div>
    <div class="bottom-button">
      <div class="texts">
        <div class="little-title">Cloud Services</div>
        <div class="big-title">Research & Energy</div>
      </div>
      <img src="../assets/svg/right_arrow.svg" alt="" />
    </div>
  </div>
</template>

<script>
export default {
  name: "",
  inheritAttrs: false,
  components: {},
  props: {
    backImage: String,
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
.rotate-item {
  position: relative;
  display: inline-block;
  width: 500px;
  height: 400px;

  .image {
    width: 100%;
    height: 100%;
    border-radius: 10px;
  }

  .dark-cover {
    position: absolute;
    z-index: 1;
    bottom: 0;
    width: 100%;
    height: 0;
    border-radius: 10px;
    transition: all 0.5s;
    background: rgba(0, 0, 0, 0.3);
  }

  .bottom-button {
    position: absolute;
    z-index: 2;
    bottom: -60px;
    left: 50%;
    transform: translate(-50%, 0);
    width: 440px;
    height: 130px;
    border-radius: 10px;
    padding: 30px;
    box-sizing: border-box;
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: #ffffff;
    box-shadow: 0px 10px 60px 0px rgba(0, 0, 0, 7%);
    overflow: hidden;

    &::before {
      content: "";
      position: absolute;
      z-index: 2;
      top: 0;
      left: 0;
      border-radius: 10px;
      width: 100%;
      height: 0;
      background: #1989fb;
      transition: all 0.5s;
    }

    .texts {
      position: relative;
      z-index: 3;
      transition: all 0.5s;
      .little-title {
        font-family: "Barlow-Medium";
        font-size: 14px;
        color: #7b7981;
        transition: all 0.5s;
      }
      .big-title {
        font-family: "Barlow-ExtraBold";
        font-size: 30px;
        margin-top: 10px;
      }
    }

    img {
      width: 30px;
      position: relative;
      z-index: 3;
    }
  }

  &:hover {
    .dark-cover {
      height: 100%;
    }

    .bottom-button {
      &::before {
        height: 100%;
      }

      .texts {
        color: #ffffff;

        .little-title {
          color: #ffffff;
        }
      }
    }
  }
}
</style>
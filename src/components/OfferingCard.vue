<template>
  <div
    :class="isHovered ? 'offering-card hovered' : 'offering-card'"
    @mouseover="hovered"
    @mouseout="unHovered"
  >
    <div class="circle" :style="isHovered ? 'background: #1A89FB' : ''">
      <img
        :src="
          isHovered
            ? require('../assets/svg/cloud_white.svg')
            : require('../assets/svg/cloud.svg')
        "
      />
      <div
        :class="isHovered ? 'blue-line first hovered' : 'blue-line first'"
      ></div>
      <div
        :class="isHovered ? 'blue-line second hovered' : 'blue-line second'"
      ></div>
    </div>
    <div class="title">
      IT Consulting <br />
      Services
    </div>
    <div class="text">
      There are many variations of <br />
      passages of lorem im available, <br />
      but majority suffered.
    </div>
    <div
      class="arrow"
      :style="isHovered ? 'background: #42D9BE' : 'background: #EEF3F7'"
    >
      <img
        :src="
          isHovered
            ? require('../assets/svg/right_arrow_white.svg')
            : require('../assets/svg/right_arrow.svg')
        "
      />
    </div>
  </div>
</template>

<script>
export default {
  name: "OfferingCard",
  inheritAttrs: false,
  components: {},
  props: {},
  data() {
    return {
      isHovered: false,
    };
  },
  computed: {},
  watch: {},
  created() {},
  mounted() {},
  beforeUnmount() {},
  unmounted() {},
  methods: {
    hovered() {
      this.isHovered = true;
    },
    unHovered() {
      this.isHovered = false;
    },
  },
};
</script> 

<style scoped lang="less">
.offering-card {
  position: relative;
  width: 385px;
  height: 480px;
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
  background: #ffffff;

  .circle {
    position: relative;
    width: 130px;
    height: 130px;
    border-radius: 50%;
    background: #eef3f7;
    padding: 25px;
    box-sizing: border-box;
    margin-top: 40px;
    transition: all 0.5s;

    img {
      width: 80px;
      position: relative;
      z-index: 1;
    }

    .blue-line {
      position: absolute;
      top: 50%;
      left: 50%;
      height: 150px;
      width: 0;
      border-right: 2px solid #1a89fb;
      opacity: 0;
      transition: all 0.5s;

      &.first {
        transform: translate(calc(-50% - 2px), calc(-50% - 2px));

        &.hovered {
          transform: translate(calc(-50% - 2px), calc(-50% - 2px))
            rotateZ(45deg);
          opacity: 1;
        }
      }

      &.second {
        transform: translate(calc(-50% + 2px), calc(-50% + 2px));

        &.hovered {
          transform: translate(calc(-50% + 2px), calc(-50% + 2px))
            rotateZ(45deg);
          opacity: 1;
        }
      }
    }
  }

  .title {
    font-family: "Barlow-ExtraBold";
    text-align: center;
    font-size: 23px;
    margin-top: 20px;
  }

  .text {
    font-family: "Barlow-Medium";
    font-size: 18px;
    text-align: center;
    color: #7b7981;
    line-height: 30px;
    margin-top: 15px;
  }

  .arrow {
    width: 60px;
    height: 60px;
    border-radius: 50%;
    padding: 10px;
    transition: all 0.5s;
    box-sizing: border-box;
    margin-top: 30px;

    img {
      width: 40px;
    }
  }
}
</style>
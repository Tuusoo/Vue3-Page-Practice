<template>
  <div
    :class="isHover ? 'top-header-button hovered' : 'top-header-button'"
    @mouseover="mouseOver"
    @mouseout="mouseOut"
  >
    <div class="green-line"></div>
    <div class="text">
      {{ text }}
    </div>
  </div>
</template>

<script>
export default {
  name: "",
  inheritAttrs: false,
  components: {},
  props: {
    text: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      isHover: false,
    };
  },
  computed: {},
  watch: {},
  created() {},
  mounted() {},
  beforeUnmount() {},
  unmounted() {},
  methods: {
    mouseOver() {
      this.isHover = true;
    },
    mouseOut() {
      this.isHover = false;
    },
  },
};
</script> 

<style scoped lang="less">
.top-header-button {
  display: inline-flex;
  align-items: center;
  height: 100px;
  width: 100px;

  .green-line {
    height: 0;
    width: 10px;
    box-sizing: border-box;
    border: 2px solid #42d9be;
    opacity: 0;
    transition: opacity 0.5s;
  }

  .text {
    font-family: "Barlow-Medium";
    font-size: 16px;
    color: #7b7981;
    margin-left: 10px;
    cursor: pointer;
  }

  &.hovered {
    .green-line {
      opacity: 1;
    }

    .text {
      font-family: "Barlow-SemiBold";
    }
  }
}
</style>
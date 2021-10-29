<template>
  <div class="big-button" @mouseover="hovering" @mouseout="unHovering">
    <span>DISCOVER MORE</span>
    <span
      class="black-block"
      :style="isHover ? 'height: 100%' : 'height: 0'"
    ></span>
  </div>
</template>

<script>
export default {
  name: "BigButton",
  inheritAttrs: false,
  components: {},
  props: {},
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
    hovering() {
      this.isHover = true;
    },
    unHovering() {
      this.isHover = false;
    },
  },
};
</script> 

<style scoped lang="less">
.big-button {
  display: inline-block;
  position: relative;
  width: 260px;
  height: 70px;
  line-height: 70px;
  border-radius: 7px;
  text-align: center;
  font-size: 14px;
  letter-spacing: 2px;
  font-family: "Barlow-Medium";
  color: #ffffff;
  background: #1989fb;
  cursor: pointer;
  user-select: none;
  overflow: hidden;

  span {
    position: relative;
    z-index: 2;
  }

  .black-block {
    position: absolute;
    bottom: 0;
    left: 0;
    content: "";
    width: 100%;
    background: #1b1825;
    z-index: 1;
    transition: all 0.5s;
  }
}
</style>
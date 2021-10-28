<template>
  <div class="big-button">DISCOVER MORE</div>
</template>

<script>
export default {
  name: "BigButton",
  inheritAttrs: false,
  components: {},
  props: {},
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

  &::after {
    position: absolute;
    top: 0;
    left: 0;
    border-radius: 7px;
    content: "";
    height: 100%;
    width: 100%;
    background: #1b1825;
    z-index: -1;
  }
}
</style>
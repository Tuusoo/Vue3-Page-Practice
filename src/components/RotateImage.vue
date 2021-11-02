<template>
  <div class="rotate-img-back">
    <img :src="image" class="rotate-image" />
  </div>
</template>

<script>
export default {
  name: "RotateImage",
  inheritAttrs: false,
  components: {},
  props: {
    image: {
      type: String,
      required: true,
    },
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
.rotate-img-back {
  display: inline-block;
  .rotate-image {
    width: 50px;
  }
  &:hover {
    .rotate-image {
      animation: rotate 0.5s;
    }
  }
  @keyframes rotate {
      0% {
        transform: rotateY(0deg);
      }
      50% {
        transform: rotateY(180deg);
      }
      100% {
        transform: rotateY(0deg);
      }
    }
}
</style>
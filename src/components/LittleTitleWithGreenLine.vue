<template>
  <div class="little-title">
    <div class="green-line"></div>
    <div class="text">
      {{ text }}
    </div>
  </div>
</template>

<script>
export default {
  name: "LittleTitleWithGreenLine",
  inheritAttrs: false,
  components: {},
  props: {
    text: {
      type: String,
      required: true,
    },
  },
  data() {
    return {}
  },
  computed: {},
  watch: {},
  created() {
  },
  mounted() {
  },
  beforeUnmount() {
  },
  unmounted() {
  },
  methods: {},
}
</script> 

<style scoped lang="less">
.little-title {
  display: inline-flex;
  align-items: center;

  .green-line {
    height: 0;
    width: 10px;
    box-sizing: border-box;
    border: 2px solid #42d9be;
  }

  .text {
    font-family: "Barlow-Medium";
    font-size: 18px;
    color: #7b7981;
    margin-left: 10px;
  }
}
</style>
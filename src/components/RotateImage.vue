<template>
  <img :src="image" class="rotate-image">
</template>

<script>
export default {
  name: "RotateImage",
  inheritAttrs: false,
  components: {},
  props: {
    image: {
      type: Object,
      required: true,
    }
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
.rotate-image {
  width: 50px;
}
</style>
<template>
  <div class="news-and-articles">
    <LittleTitleWithGreenLineVue text="Direct from the Blog" />
    <div class="big-title">News & Articles</div>
  </div>
</template>

<script>
import LittleTitleWithGreenLineVue from "../components/LittleTitleWithGreenLine.vue"

export default {
  name: "",
  inheritAttrs: false,
  components: {
    LittleTitleWithGreenLineVue,
  },
  props: {},
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
.news-and-articles {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 100px;

  .big-title {
    font-family: "Barlow-ExtraBold";
    font-size: 50px;
  }
}
</style>
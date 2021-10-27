<template>
  <TopHeaderVue />
  <TopMenuVue />
</template>

<script>
import TopHeaderVue from "./smallpages/TopHeader.vue"
import TopMenuVue from "./smallpages/TopMenu.vue"

export default {
  name: "",
  inheritAttrs: false,
  components: {
    TopHeaderVue,
    TopMenuVue,
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

<style>
@font-face {
  font-family: "Barlow-Regular";
  src: url(./fonts/Barlow-Regular.ttf);
}

@font-face {
  font-family: "Barlow-Medium";
  src: url(./fonts/Barlow-Medium.ttf);
}

@font-face {
  font-family: "Barlow-SemiBold";
  src: url(./fonts/Barlow-SemiBold.ttf);
}

body {
  margin: 0;
}
</style>

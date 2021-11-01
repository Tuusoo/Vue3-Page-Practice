<template>
  <TopHeaderVue />
  <TopMenuVue />
  <CoverPageVue />
  <KnowAboutUsVue />
  <WhatWeOfferingVue />
</template>

<script>
import TopHeaderVue from "./smallpages/TopHeader.vue";
import TopMenuVue from "./smallpages/TopMenu.vue";
import CoverPageVue from "./smallpages/CoverPage.vue";
import KnowAboutUsVue from "./smallpages/KnowAboutUs.vue";
import WhatWeOfferingVue from "./smallpages/WhatWeOffering.vue";

export default {
  name: "",
  inheritAttrs: false,
  components: {
    TopHeaderVue,
    TopMenuVue,
    CoverPageVue,
    KnowAboutUsVue,
    WhatWeOfferingVue,
  },
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

@font-face {
  font-family: "Barlow-ExtraBold";
  src: url(./fonts/Barlow-ExtraBold.ttf);
}

body {
  margin: 0;
  width: 100vw;
  overflow-x: hidden;
}
</style>

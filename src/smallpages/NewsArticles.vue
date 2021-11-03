<template>
  <div class="news-and-articles">
    <LittleTitleWithGreenLineVue text="Direct from the Blog" />
    <div class="big-title">News & Articles</div>
    <div class="three-cards">
      <NewsCardsVue v-for="item in cardsDetails" :cardsDetail="item" :key="item.text" />
    </div>
  </div>
</template>

<script>
import LittleTitleWithGreenLineVue from "../components/LittleTitleWithGreenLine.vue";
import NewsCardsVue from "../components/NewsCards.vue";

export default {
  name: "NewsArticles",
  inheritAttrs: false,
  components: {
    LittleTitleWithGreenLineVue,
    NewsCardsVue,
  },
  props: {},
  data() {
    return {
      cardsDetails: [
        {
          picture: require("../assets/news-one-img-1.jpg"),
          text: "What is Holding Back the IT Solution Industry?",
        },
        {
          picture: require("../assets/news-one-img-2.jpg"),
          text: "Leverage agile frameworks to provide a",
        },
        {
          picture: require("../assets/news-one-img-3.jpg"),
          text: "Bring to the table win-win survival strategies.",
        },
      ],
    };
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
.news-and-articles {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 100px;

  .big-title {
    font-family: "Barlow-ExtraBold";
    font-size: 50px;
  }

  .three-cards {
    display: flex;
    margin-top: 40px;
  }
}
</style>
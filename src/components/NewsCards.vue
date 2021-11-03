<template>
  <div class="news-card">
    <div class="image">
      <img :src="cardsDetail.picture" />
      <div class="date">20 Aug</div>
      <div class="plus">+</div>
    </div>
    <div class="texts">
      <div class="author-comment">
        <img src="../assets/svg/people.svg" />
        <span>by admin</span>
        <img src="../assets/svg/chat.svg" />
        <span>2 comments</span>
      </div>
      <div class="title">{{ cardsDetail.text }}</div>
      <div class="text">
        Lorem ipsum is simply free text used by copytyping refreshing.
      </div>
      <div class="read-more">Read More</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "NewsCards",
  inheritAttrs: false,
  components: {},
  props: {
    cardsDetail: Object,
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
.news-card {
  width: 360px;
  height: 540px;
  color: #1c1926;
  margin: 0 15px;
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0px 10px 60px 0px rgba(0, 0, 0, 5%);
  border-bottom: 3px solid;
  border-color: #ffffff;
  transition: all 0.5s;

  .image {
    position: relative;
    height: 270px;
    overflow: hidden;
    cursor: pointer;

    img {
      position: absolute;
      left: 50%;
      top: 50%;
      width: 100%;
      transform: translate(-50%, -50%);
      transition: all 0.5s;
    }

    .date {
      font-family: "Barlow-ExtraBold";
      position: absolute;
      z-index: 1;
      background: #fdfdfd;
      bottom: 0;
      left: 0;
      border-radius: 0 10px 0 0;
      width: 70px;
      height: 70px;
      box-sizing: border-box;
      text-align: center;
      padding: 20px;
      font-size: 14px;
    }

    .plus {
      position: absolute;
      width: 100%;
      height: 100%;
      text-align: center;
      line-height: 270px;
      box-sizing: border-box;
      top: 20%;
      left: 50%;
      transform: translate(-50%, -50%);
      color: #ffffff;
      opacity: 0;
      transition: all 0.5s;
      font-size: 40px;
      user-select: none;
    }
  }

  .texts {
    padding: 38px;

    .author-comment {
      display: flex;
      align-items: center;
      color: #7b7981;
      font-family: "Barlow-Medium";
      font-size: 14px;

      img {
        width: 16px;
      }

      span {
        margin: 0 20px 0 10px;
        cursor: pointer;
        transition: all 0.5s;

        &:hover {
          color: #57dfc6;
        }
      }
    }

    .title {
      margin-top: 10px;
      font-family: "Barlow-SemiBold";
      font-size: 24px;
      color: #1c1926;
      transition: all 0.5s;
    }

    .text {
      margin-top: 20px;
      color: #7b7981;
      font-family: "Barlow-Medium";
      line-height: 30px;
    }

    .read-more {
      display: inline-block;
      font-family: "Barlow-SemiBold";
      cursor: pointer;
      margin-top: 10px;
      color: #1c1926;
      transition: all 0.5s;

      &:hover {
        color: #57dfc6;
      }
    }
  }

  &:hover {
    border-color: #57dfc6;
    .image {
      img {
        width: 110%;
      }

      .plus {
        top: 50%;
        color: #1989fb;
        opacity: 1;
        background: rgba(0, 0, 0, 0.3);
      }
    }
    .title {
      color: #1989fb;
    }
  }
}
</style>
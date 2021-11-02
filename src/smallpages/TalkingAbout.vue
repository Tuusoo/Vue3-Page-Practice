<template>
  <div class="talking-about">
    <div class="text-area">
      <LittleTitleWithGreenLineVue text="Customers Feedbacks" />
      <div class="big-title">
        What They’re <br />
        Talking About <br />
        Company
      </div>
      <div class="switch-buttons">
        <img src="../assets/svg/arrow-left.svg" @click="moveAhead" />
        <img src="../assets/svg/arrow-right.svg" @click="moveToNext" />
      </div>
    </div>
    <div class="banner-area">
      <div class="banner-body" :style="bannerBodyStyle" ref="bannerBody">
        <TalkingAboutCardVue
          v-for="item in bannerArray"
          :key="item.person"
          :item-data="item"
        />
      </div>
    </div>
  </div>
</template>

<script>
import LittleTitleWithGreenLineVue from "../components/LittleTitleWithGreenLine.vue";
import TalkingAboutCardVue from "../components/TalkingAboutCard.vue";

export default {
  name: "TalkingAbout",
  inheritAttrs: false,
  components: {
    LittleTitleWithGreenLineVue,
    TalkingAboutCardVue,
  },
  props: {},
  data() {
    return {
      bannerArray: [
        {
          picture: require("../assets/testimonial-one-img-1.png"),
          person: "Kevin Martin",
        },
        {
          picture: require("../assets/testimonial-one-img-2.png"),
          person: "Christine Eve",
        },
        {
          picture: require("../assets/testimonial-one-img-3.png"),
          person: "Joe Smith",
        },
        {
          picture: require("../assets/testimonial-one-img-1.png"),
          person: "Kevin Martin",
        },
      ],
      rotateIndex: 0,
      rotateTimer: null,
    };
  },
  computed: {
    bannerBodyStyle() {
      if(this.rotateIndex > 2){
        return `transform: translate(-${this.rotateIndex * 490}px,0);`;
      }else{
        return `transform: translate(-${this.rotateIndex * 490}px,0);transition: all 0.5s;`;
      }
    },
  },
  watch: {
    rotateIndex(newVal) {
      console.log(this.$refs.bannerBody.style)
      if (newVal > 2) {
        this.rotateIndex = 0;
      } else if(newVal < 0) {
        this.rotateIndex = 2;
      }
    },
  },
  created() {
    this.rotateTimer = setInterval(() => {
      this.rotateIndex++;
    }, 3000);
  },
  mounted() {},
  beforeUnmount() {
    clearInterval(this.rotateTimer);
  },
  unmounted() {},
  methods: {
    moveToNext() {
      clearInterval(this.rotateTimer);
      this.rotateIndex++;
      this.rotateTimer = setInterval(() => {
        this.rotateIndex++;
      }, 3000);
    },
    moveAhead() {
      clearInterval(this.rotateTimer);
      this.rotateIndex--;
      this.rotateTimer = setInterval(() => {
        this.rotateIndex++;
      }, 3000);
    },
  },
};
</script> 

<style scoped lang="less">
.talking-about {
  display: flex;
  box-sizing: border-box;
  padding: 100px calc((100vw - 1150px) / 2);
  background: #eef3f7;

  .text-area {
    width: 35%;
    flex-shrink: 0;
    .big-title {
      font-family: "Barlow-ExtraBold";
      font-size: 50px;
      margin-top: 10px;
    }

    .switch-buttons {
      margin-top: 20px;

      img {
        width: 80px;
        margin-right: 20px;
        cursor: pointer;
      }
    }
  }

  .banner-area {
    flex-shrink: 0;
    overflow: hidden;
  }
}
</style>
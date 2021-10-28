<template>
  <div class="top-header">
    <div class="left-area">
      <div class="location">
        <img src="../assets/svg/location.svg" class="little-icon" />
        <span>66 Road Broklyn Golden Street. New York</span>
      </div>
      <div class="location">
        <img src="../assets/svg/mail.svg" class="little-icon" />
        <span>needhelp@company.com</span>
      </div>
    </div>
    <div class="right-area">
      <div class="text">
        <span>Now Hiring:</span> Are you a driven and motivated 1st Line IT
        Support Engineer?
      </div>
      <div class="icons">
        <img src="../assets/svg/twitter.svg" />
        <img src="../assets/svg/facebook.svg" />
        <img src="../assets/svg/pinterest.svg" />
        <img src="../assets/svg/instagram.svg" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TopHeader",
  inheritAttrs: false,
};
</script> 

<style scoped lang="less">
.top-header {
  box-sizing: border-box;
  padding: 0 calc((100vw - 1300px) / 2);
  background: #1b1825;
  width: 100vw;
  display: flex;
  justify-content: space-between;
  font-family: "Barlow-Medium", sans-serif;
  font-weight: 500;

  .left-area {
    display: flex;

    .location {
      display: flex;
      align-items: center;
      margin-right: 30px;
      img {
        width: 15px;
        margin-right: 10px;
      }
      span {
        line-height: 38px;
        font-size: 12px;
        color: #ada8ba;
      }
    }
  }

  .right-area {
    display: flex;

    .text {
      line-height: 38px;
      font-size: 12px;
      color: #ada8ba;

      span {
        color: #42d99c;
      }
    }

    .icons {
      display: flex;

      img {
        width: 17px;
        margin-left: 20px;
      }
    }
  }
}
</style>
<template>
    <div class="footer-container">
      <div class="footer-container__navigation">
        <span>@ BroadCastLib By Egor Borovlev</span>
      </div>
      <div class="header-container__OtherComponents">
        
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {

      };
    },
  };
  </script>
  
  <style lang="scss" scoped>
  .footer-container {
    width: 100%;
    display: flex;
    justify-content: space-around;
    align-items: center;
    background: #2779a7;
    height: fit-content;
    &__navigation {
      display: flex;
      align-items: center;
      height: 35px;
      width: 98%;
      color: #ffff;
    }
    &__navBar {
      display: flex;
      align-items: center;
      justify-content: space-around;
      width: 30%;
    }
  }
  </style>
  
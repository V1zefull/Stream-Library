<script setup lang="ts">
import headerComp from "./components/headerCompinent/header.vue";
import footerComp from "./components/footerComponent/footer.vue";
import mainComp from "./page/mainPage/main.vue";
</script>

<template>
  <div class="container">
    <header class="container__header">
      <headerComp />
    </header>
    <body class="container__main">
      <mainComp/>
    </body>
    <footer class="container__footer">
      <footerComp />
    </footer>
    <router-view />
  </div>
</template>

<style scoped lang="scss">
.container {
  position: relative;
  width: 100%;
  &__header {
    display: flex;
    justify-content: center;
    align-items: center;
    height: fit-content;
    background: #2779a7;
    width: 100%;
  }
  &__main{
    height: fit-content;
    background: #ffffff;
    width: 100%;
  }
  &__footer {
    position: absolute;
    bottom: 0;
    display: flex;
    align-items: center;
    height: fit-content;
    background: #2779a7;
    width: 100%;
  }
}
</style>

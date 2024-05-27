<template>
  <div class="header-container">
    <div class="header-container__navigation">
      <h1>BroadCastLib</h1>
      <div class="header-container__navBar">
        <div class="header-container__btn" v-for="item in navBar">
          {{ item.name }}
        </div>
      </div>
    </div>
    <div class="header-container__theme">
      <div class="header-container__btn">Светлая тема</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      navBar: [
        {
          name: "Главная страница",
        },
        {
          name: "Демонстрация отдельных компонентов",
        },
        {
          name: "Документация",
        },
        {
          name: "Поддержка",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.header-container {
  width: 100%;
  display: flex;
  justify-content: space-around;
  align-items: center;
  background: #2779a7;
  height: fit-content;
  &__navigation {
    display: flex;
    width: 90%;
    color: #ffff;
  }
  &__navBar {
    display: flex;
    align-items: center;
    justify-content: space-around;
    width: fit-content;
  }
  &__btn {
    color: #ffff;
    background: #2779a7;
    padding: 15px;
    &:hover {
      background: #4789af;
    }
  }
}
</style>

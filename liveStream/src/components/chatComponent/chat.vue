<template>
  <div class="chat">
    <div class="chat__header">
      <div>&#10006</div>
      Super Chat
    </div>
    <div class="chat__body">
      <div class="chat__message" v-for="item in message">
        <label>{{ item.name }}</label>
        <textarea
          :placeholder="item.name"
          ref="textarea"
          readonlys
          :value="item.value"
          @change="resize()"
          disabled
        ></textarea>
      </div>
    </div>
    <div class="chat__footer">
      <input type="text" placeholder="Введите сообщение" />
      <div>⮚</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: [
        {
          name: "Егор Боровлев",
          value: ":(",
        },
        {
          name: "Николач",
          value: "Увековечено в камне",
        },
        {
          name: "Кирито 1000-7",
          value: "Как же хорошо ты делаешь, продолжай!",
        },
        {
          name: "Вадимка299",
          value: "Не пошла игра анлаки?",
        },
      
        {
          name: "Ясечка",
          value: "Вы раки не ХОЧУ с вами играть в пати!!!",
        },
        {
          name: "Паника",
          value: "А я лучше в доту играю :)?",
        },
      ],
    };
  },
  methods: {},
};
</script>

<style lang="scss" scoped>

.chat {
  position: relative;
  background: #2779a7;
  border-radius: 16px;
  width: fit-content;
  display: flex;
  justify-content: space-between;
  flex-direction: column;
  height: 47em;
  padding: 10px 15px 15px 15px;
  margin: 5px 20px 5px 5px;

  &__header {
    display: flex;
    justify-content: space-between;
    margin-bottom: 1em;
    width: 60%;
    color: white;
  }
  &__body{
    scrollbar-width: thin;
    scrollbar-color: gray rgb(196, 196, 196);
    overflow: auto;
    height: 37em;
  }
  

  &__message {
    display: flex;
    flex-direction: column;
    label {
      color: white;
    }
    textarea {
      width: 24em;
      border-radius: 16px;
      padding-top: 10px;
      height: 3em;
      color: white;
      padding-left: 10px;
      margin-bottom: 1em;
      font-size: 15px;
      resize: none;
      overflow: hidden;
    }
  }

  &__footer {
    position: relative;
    bottom: 0;
    display: flex;
    color: white;
    font-size: 23px;
    align-items: center;
    height: fit-content;
    input {
      width: 100%;
      border-radius: 8px;
      height: 2em;
      font-size: 16px;
      padding-left: 10px;
      margin-right: 10px;
      background: #6b99b2;
      border: none;
      color: white;
      &::placeholder{
        color: white;
      }
    }
    
  }

}
</style>

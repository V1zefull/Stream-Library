<template>
  <div class="chat">
    <div class="chat__header">
      <div class="chat__message-list" v-for="item in message">
        <div class="chat__message">
          <label>{{ item.name }}</label>
          <textarea
            :placeholder="item.name"
            @change="resize()"
            ref="textarea"
            readonlys
            disabled
            wrap="soft"
          >
                {{ item.value }}
            </textarea
          >
        </div>
      </div>
      <div class="chat__input-container">
        <input type="text" placeholder="Введите сообщение" />
      </div>
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
          value:
            "Классный стрим брстрим брострим брострим брострим брострим брострим брострим брострим брострим брострим брострим брострим брострим брострим брострим брострим брострим брострим брострим брострим брострим брострим брострим брострим брострим брострим брострим брострим брострим броо",
        },
      ],
    };
  },
  methods: {
    resize() {
      let element = this.$refs["textarea"];
      element.style.height = "18px";
      element.style.height = element.scrollHeight + "px";
    },
  },
};
</script>

<style lang="scss" scoped>
.chat {
  &__message {
    display: flex;
  }
  textarea {
    overflow: hidden;
    display: flex;
    flex-wrap: wrap;
    width: 100%;
    resize: none;
    width: 24em;
  }
}
</style>

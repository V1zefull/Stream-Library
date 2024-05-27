<script>
import chatComp from '../../components/chatComponent/chat.vue';
export default {
    components:{
        chatComp,
    },
    data() {
      return {

      };
    },
  };
</script>

<template>
    <div class="container">
        <div class="container__main">
            <chatComp/>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.container{
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    &__main{
        width: 90%;
    }
}

</style>
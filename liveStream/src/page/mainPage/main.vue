<script>
import chatComp from '../../components/chatComponent/chat.vue';
import Follower from '../../components/followerComponent/follower.vue';
export default {
    components:{
        chatComp,
        Follower,
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
            <div class="container__follower"><Follower/></div>
            
            <div class="container__chat"><chatComp/></div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.container{
    width: 100%;
    height: 100%;
    &__main{
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    &__follower{
        width: 20em;
        height: 100%;
    }
}

</style>
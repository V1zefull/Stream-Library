<script>
import chatComp from '../../components/chatComponent/chat.vue';
import Follower from '../../components/followerComponent/follower.vue';
import Player from '../../components/playerComponent/player.vue'
export default {
    components: {
        Player,
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
            <div class="container__follower">
                <Follower />
            </div>
            <div class="container_player">
                    <Player class="videoplayer" src="test.mp4" :muted="false" :autoplay="true" :controls="true"
                        :loop="false" poster="jpg_44-2.jpg"></Player>
            </div>
            <div class="container__chat">
                <chatComp />
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.container {
    width: 100%;
    height: 100%;

    &__main {
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    &__follower {
        width: 20em;
        height: 100%;
    }
}
</style>
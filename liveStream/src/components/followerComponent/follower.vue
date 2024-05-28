<template>
    <div class="follower">
        <div class="follower__container" >
            <div class="follower__header">Followers</div>
            <div class="follower__body" v-for="item in followerList" :key="item.id">
                <div>&#128535</div>
                {{ item.name }}
            </div>
            
        </div>
    </div>
</template>

<script>
    export default {
        data(){
            return{
                followerList:
                [
                    {
                        name: 'Егор Боровлев',
                        icon: '&#128535',
                        id: 1
                    },
                    {
                        name: 'Паника',
                        icon: '&#128535',
                        id: 2
                    },
                    {
                        name: 'Кирито 1000-7',
                        icon: '&#128535',
                        id: 3
                    },
                    {
                        name: 'Николаич',
                        icon: '&#128535',
                        id: 4
                    }
                ]
            }
        }

    }
</script>

<style lang="scss" scoped>
.follower{
    width: 100%;
    height: 100%;
    background: #2779a7;
    &__container{
        color: white;
    }
    &__header{
        font-size: 24px;
        padding: 10px 0 10px 0;
        display: flex;
        justify-content: center;
        align-items: center;
        border-bottom: 1px solid rgba(0, 0, 0, 0.336);
    }
    &__body{
        padding: 10px 0 10px 5px;
        border-bottom: 1px solid rgba(0, 0, 0, 0.336);
        font-size: 20px;
        display: flex;
        align-items: center;
    }
}
</style>
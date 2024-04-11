<script>
    export default{
        name: 'AppHeader',
        data (){
            return {
                links: [
                    {
                        title: 'CHARACTERS',
                        active: false
                    },
                    {
                        title: 'COMICS',
                        active: true
                    },
                    {
                        title: 'MOVIES',
                        active: false
                    },
                    {
                        title: 'TV',
                        active: false
                    },
                    {
                        title: 'GAMES',
                        active: false
                    },
                    {
                        title: 'COLLECTIBLES',
                        active: false
                    },
                    {
                        title: 'VIDEOS',
                        active: false
                    },
                    {
                        title: 'FANS',
                        active: false
                    },
                    {
                        title: 'NEWS',
                        active: false
                    },
                    {
                        title: 'SHOP',
                        active: false
                    },
                ]
            }
        },
        methods: {

        },
        mounted() {
        }
    }
   
</script>

<template>
   <header>
        <div class="container d-flex jst-btwn algn-cntr">
            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="logo">
            </div>
            <ul class="nav-bar d-flex algn-cntr">
                <li class="anchor" v-for="link, index in links">
                    <a class="d-flex algn-cntr" :class="{'active' : link.active}" href="#">{{ link.title }}</a>
                </li>
            </ul>
        </div>
   </header>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;
.container{
    min-height: 140px;
}
ul{
    li{
        margin-left: 20px;
        a{
            min-height: 140px;
            color: black;
            font-weight: bold;
            font-size: 20px;
            &.active::after{
                content: '';
                position: absolute;
                bottom: 0;
                left: 50%;
                transform: translateX(-50%);
                background-color: $primary-color;
                height: 5px;
                margin-top: 100px;
                width: 100%;
            }
            &.active{
                color: $primary-color;
            }
        }
    }
}
</style>
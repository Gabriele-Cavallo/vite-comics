<script>
    export default{
        name: 'AppFooter',
        data (){
            return {
                socials:[
                    {
                        social: 'Facebook',
                        icon: 'fa-brands fa-facebook-f d-flex jst-cntr algn-cntr'
                    },
                    {
                        social: 'Twitter',
                        icon: 'fa-brands fa-twitter d-flex jst-cntr algn-cntr'
                    },
                    {
                        social: 'Youtube',
                        icon: 'fa-brands fa-youtube d-flex jst-cntr algn-cntr'
                    },
                    {
                        social: 'Pinterest',
                        icon: 'fa-brands fa-pinterest-p d-flex jst-cntr algn-cntr'
                    },
                    {
                        social: 'Maps',
                        icon: 'fa-solid fa-location-dot d-flex jst-cntr algn-cntr'
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
    <footer class="d-flex algn-cntr">
        <div class="container d-flex algn-cntr jst-btwn">
            <button class="btn pointer">SIGN-UP NOW!</button>
            <div class="social-wrapper d-flex algn-cntr">
                <span>FOLLOW US</span>
                <!-- Single Social Template -->
                <a v-for="social in socials" href="#" class="single-social">
                    <i :class="social.icon"></i>
                </a>
                <!-- /Single Social Template -->
            </div>
        </div>
    </footer>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;
footer{
    background-color: #303030;
    height: 182px;
}
button{
    background: transparent;
    border: 2px solid $primary-color;
    padding: 20px;
    font-weight: bold;
    color: white;
    font-size: 16px;
}
.social-wrapper{
    gap: 20px;
    padding-right: 80px;
    span{
        color: $primary-color;
        font-weight: 900;
        font-size: 25px;
    }
    .single-social{
        color: #303030;
        i{
            height: 40px;
            width: 40px;
            background-color: grey;
            border-radius: 50%;
            font-size: 25px;
        }
    }
}
</style>
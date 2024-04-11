<script>
    export default{
        name: 'AppMainBottomSection',
        data (){
            return {
                section: [
                    {
                        title: 'DC COMICS',
                        links: ['Charcater', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News']
                    },
                    {
                        title: 'SHOP',
                        links: ['Shop DC', 'Shop DC Collectibles']
                    },
                    {
                        title: 'DC',
                        links: ['Terms of Use', 'Privacy Policy (New)', 'Ad Choices', 'Advertising', 'Jobs', 'Subscription', 'Talent Workshop', 'CPSC Certificates', 'Ratings', 'Shop Helpd', 'Contact Us']
                    },
                    {
                        title: 'Sites',
                        links: ['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa']
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
    <section class="d-flex algn-cntr">
        <div class="container d-flex algn-cntr jst-btwn">
            <div class="links-wrapper d-flex">
                <div class="d-flex flex-col d-wrap">
                    <ul v-for="singleSection in section">
                        <h4>{{singleSection.title}}</h4>
                        <li v-for="singleLink in singleSection.links">
                            <a href="#">
                                {{singleLink}}
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="logo">
                <img src="../assets/img/dc-logo-bg.png" alt="logo">
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
section{
    background-image: url('..//assets/img/footer-bg.jpg');
    min-height: 400px;
    background-size: cover;
    overflow-y: hidden;
}
img{
    transform: scale(1.5);
    margin-right: 350px;
}
.links-wrapper{
    color: white;
    min-width: 600px;
    max-height: 450px;
    ul{
        font-weight: bold;
        font-size: 20px;
        margin-bottom: 20px;
        margin-right: 40px;
        h4{
            margin-bottom: 20px;
            font-size: 30px;
        }
        li{
            margin-top: 10px;
            font-weight: 400;
            color: grey;
            font-size: 16px;
            a{
                color: grey;
            }
        }
    }
}

</style>
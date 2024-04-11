<script>
    export default{
        name: 'AppMainMiddleSection',
        data (){
            return {
                services: [
                    {
                        title: 'DIGITAL COMICS',
                        image: 'buy-comics-digital-comics.png'
                    },
                    {
                        title: 'DC MERCHANDISE',
                        image: 'buy-comics-merchandise.png'
                    },
                    {
                        title: 'SUBSCRIPTION',
                        image: 'buy-comics-subscriptions.png'
                    },
                    {
                        title: 'COMIC SHOP LOCATOR',
                        image: 'buy-comics-shop-locator.png'
                    },
                    {
                        title: 'DC POWER VISA',
                        image: 'buy-dc-power-visa.svg'
                    },
                    ]
                }
        },
        methods: {
            getImageUrl(name) {
                return new URL(`../assets/img/${name}`, import.meta.url).href;
            }
        },
        mounted() {
        }
    }
   
</script>

<template>
    <section class="d-flex algn-cntr">
        <div class="container d-flex algn-cntr jst-btwn">
            <div v-for="service in services" class="services-wrapper d-flex algn-cntr">
                <img :src="getImageUrl(service.image)" alt="Service">
                <span>{{ service.title }}</span>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;
section{
    background-color: $primary-color;
    min-height: 200px;
}
.container{
    padding: 80px;
}
img{
    max-height: 80px;
}
.services-wrapper{
    gap: 10px;
    color: white;
    min-width: 255px;
}

</style>
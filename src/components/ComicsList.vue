<script>
    export default{
        name: 'ComicsList',
        props: ['comics'],
    }
</script>

<template>
    <div class="container d-flex d-wrap jst-btwn">
        <div v-for="comic in comics" class="comic-wrapper pointer">
            <img :src="comic.thumb" alt="comics">
            <h2>{{comic.series}}</h2>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;

.comic-wrapper{
    text-align: center;
    display: flex;
    flex-wrap: wrap;
    margin: 0 6px 50px;
    width: calc((100% / 6) - 12px);
    img{
            max-height: 340px;
            width: 100%;
        }
    h2{
    color: white;
}
}
</style>
<script>
    import AppHeader from './components/AppHeader.vue';
    import AppMainTopSection from './components/AppMainTopSection.vue';
    import AppMainMiddleSection from './components/AppMainMiddleSection.vue';
    import AppFooterTopSection from './components/AppFooterTopSection.vue';
    import AppFooter from './components/AppFooter.vue';

    export default{
        components: {
            AppHeader,
            AppMainTopSection,
            AppMainMiddleSection,
            AppFooterTopSection,
            AppFooter
        }
    }
</script>

<template>
    <AppHeader></AppHeader>
    <main>
        <AppMainTopSection></AppMainTopSection>
        <AppMainMiddleSection></AppMainMiddleSection>
    </main>
    <footer>
        <AppFooterTopSection></AppFooterTopSection>
        <AppFooter></AppFooter>
    </footer>
</template>

<style lang="scss">
    @use './style/generic';
    a{
        text-decoration: none;
    }
    li{
        list-style-type: none;
    }
</style>
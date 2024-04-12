<script>
    import AppHeader from './components/AppHeader.vue';
    import AppMainTopSection from './components/AppMainTopSection.vue';
    import AppMainBottomSection from './components/AppMainBottomSection.vue';
    import AppFooterTopSection from './components/AppFooterTopSection.vue';
    import AppFooter from './components/AppFooter.vue';

    export default{
        components: {
            AppHeader,
            AppMainTopSection,
            AppMainBottomSection,
            AppFooterTopSection,
            AppFooter
        }
    }
</script>

<template>
    <AppHeader></AppHeader>
    <main>
        <AppMainTopSection></AppMainTopSection>
        <AppMainBottomSection></AppMainBottomSection>
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
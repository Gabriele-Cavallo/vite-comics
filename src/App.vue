<script>
    import AppHeader from './components/AppHeader.vue';
    import AppMainTopSection from './components/AppMainTopSection.vue';
    import AppMainMiddleSection from './components/AppMainMiddleSection.vue';
    import AppMainBottomSection from './components/AppMainBottomSection.vue';
    import AppFooter from './components/AppFooter.vue';

    export default{
        components: {
            AppHeader,
            AppMainTopSection,
            AppMainMiddleSection,
            AppMainBottomSection,
            AppFooter
        }
    }
</script>

<template>
    <AppHeader></AppHeader>
    <AppMainTopSection></AppMainTopSection>
    <AppMainMiddleSection></AppMainMiddleSection>
    <AppMainBottomSection></AppMainBottomSection>
    <AppFooter></AppFooter>
</template>

<style lang="scss">
    @use './style/generic';
</style>


<template>
    <div>
        <HeaderApp />
        <MainApp />
        <FooterApp />
    </div>
</template>

<script>
import HeaderApp from './components/HeaderApp.vue';
import MainApp from './components/MainApp.vue';
import FooterApp from './components/FooterApp.vue';

export default {

    data() {
        return {};
    },
    components: {
        HeaderApp,
        MainApp,
        FooterApp
    }
}
</script>

<style lang="scss" scoped></style>


<template >
    <div>
        <HeaderApp />
        <MainApp />
        <FasciaApp />
        <FooterApp />
    </div>
</template>

<script>
import HeaderApp from './components/HeaderApp.vue';
import MainApp from './components/MainApp.vue';
import FooterApp from './components/FooterApp.vue';
import FasciaApp from './components/FasciaApp.vue';



export default {

    data() {
        return {};
    },
    components: {
        HeaderApp,
        MainApp,
        FasciaApp,
        FooterApp,

    }
}
</script>

<style lang="scss" scoped></style>
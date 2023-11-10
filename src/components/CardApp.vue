<template>
    <div class="gap-2 d-flex flex-column justify-content-start myCard" @click="logItems(image)">
        <div class="image-conteiner">
            <img :src="image" alt="">
        </div>
        <div class="title">
            {{ title }}
        </div>
    </div>
</template>

<script>
export default {
    props: {
        image: String,
        cost: String,
        title: String,
        typology: String
    },
    data() {
        return {

        }
    },
    mounted() {
    },
    methods: {

    }
}
</script>

<style lang="scss" scoped>
.image-conteiner {
    width: 10vw;
    height: 10vw;
    overflow-y: hidden;
}

.myCard {
    padding: 10px;
    max-width: calc(100%/6);
    min-width: calc(100%/6);
}

img {
    width: 100%;
}

.title {
    color: white;
    max-width: 150px;
    padding-bottom: 20px;
}
</style>

<template>
    <div class="card gap-2 d-flex flex-column justify-content-start" @click="logItems(image)">
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
        this.logItems(this.image)
    },
    methods: {
        logItems(val) {
            console.log('image ' + val)
        }
    }
}
</script>

<style lang="scss" scoped></style>
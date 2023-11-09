<template>
    <div class="fascia">
        <div class="container d-flex flex-row justify-content-evenly align-items-center h-100 ">
            <div v-for="feature in features" class="img-container d-flex flex-row  align-items-center ">
                <img :src="feature.link" alt="ciao" srcset="">
                <div class=" ps-2 text-white">{{ feature.title }}</div>
            </div>
        </div>
    </div>
</template>

<script>

export default {
    name: 'FasciaApp',
    data() {
        return {
            features: [
                {
                    title: 'DIGITAL COMICS',
                    link: '/img/buy-comics-digital-comics.png'
                },
                {
                    title: 'DC MERCHANDISE',
                    link: '/img/buy-comics-merchandise.png'
                },
                {
                    title: 'SUBSCRIPTION',
                    link: '/img/buy-comics-subscriptions.png'
                },
                {
                    title: 'COMIC SHOP PORTAL',
                    link: '/img/buy-comics-shop-locator.png'
                },
                {
                    title: 'DC POWER VISA',
                    link: '/img/buy-dc-power-visa.svg'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
.fascia {
    background-color: #0282f9;
    width: 100%;
    height: 20vh;
}

.img-container {
    height: 30%;
}

img {
    max-height: 100%;
}
</style>
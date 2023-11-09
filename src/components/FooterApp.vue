<template>
    <div class="footer">
        <div class="footer-top d-flex flex-row justify-content-evenly py-5 ">
            <ul class="outer-ul  d-flex flex-column flex-wrap ">
                <li v-for="(category, index) in categories">
                    <h4 class="category">{{ category.title }}</h4>
                    <ul class="pl-0">
                        <li v-for="(link) in category.links" class="">
                            <a class="sublink" href="#">{{ link }}</a>
                        </li>
                    </ul>
                </li>
            </ul>
            <div class="img-container overflow-hidden d-flex flex-row justify-content-end ">
                <img src="../assets/img/dc-logo-bg.png" alt="">
            </div>
        </div>
        <div class="footer-bottom d-flex flex-row justify-content-evenly align-items-center py-3 ">
            <div>
                <div class="button">SIGN UP NOW</div>
            </div>
            <div class=" d-flex flex-row align-items-center ">
                <div>
                    FOLLOW US
                </div>

                <img v-for="i in 9" src="../assets/img/footer-facebook.png" alt="" class=" me-2 ">

            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'FooterApp',
    data() {
        return {
            categories: [
                {
                    title: "DC COMICS",
                    links: [
                        'Character',
                        'Comics',
                        'Movies',
                        'TV',
                        'Games',
                        'Videos',
                        'News',
                    ]
                },
                {
                    title: "SHOP",
                    links: [
                        'Shop DC',
                        'shop DC Collectibles',

                    ]
                },
                {
                    title: "DC",
                    links: [
                        'Character',
                        'Comics',
                        'Movies',
                        'TV',
                        'Games',
                        'Videos',
                        'News',

                    ]
                },
                {
                    title: "SITES",
                    links: [
                        'Character',
                        'Comics',
                        'Movies',
                        'TV',
                        'Games',
                        'Videos',
                        'News',

                    ]
                },
            ]



        }
    }
}
</script>

<style lang="scss" scoped>
.footer-top {
    background-image: url('../assets/img/footer-bg.jpg');
}

.sublink {
    color: gainsboro;
    text-decoration: none;
}

.category {
    color: white;
    font-weight: bolder;
}

.outer-ul {
    max-height: 50vh;
    width: 40vw;
}

.footer-top {
    max-height: 50vh;
}

img {
    max-height: 100%;
}

.button {
    background-color: #00000000;
    color: white;
    border: 1px solid blue;
    padding: 10px;
}
</style>
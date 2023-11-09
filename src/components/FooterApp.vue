<template>
    <div class="footer">
        <div id="footer-top">
            <div class="footer-description container d-flex flex-row justify-content-between ">
                <ul class="outer-ul  d-flex flex-column flex-wrap py-5">
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
        </div>
        <div style="background-color: #565656;">
            <div class="footer-bottom d-flex flex-row justify-content-between align-items-center py-3 container ">
                <div>
                    <div class="button">SIGN UP NOW</div>
                </div>
                <div class=" d-flex flex-row align-items-center ">
                    <div style="color: #0282f9; font-size: bolder;" class="me-2">
                        FOLLOW US
                    </div>
                    <img v-for="index in 5" :src="'/img/footer' + index + '.png'" alt="" class=" me-2 ">
                </div>
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
                    ],

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
            ],
            start: '../assets/img/footer',
            png: '.png'



        }
    }
}
</script>

<style lang="scss" scoped>
.footer {
    background-color: #565656;
}

#footer-top {
    background-image: url('../assets/img/footer-bg.jpg');
    max-height: 50vh;
}

.footer-description {
    max-height: 50vh;
    overflow-x: visible;
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

.img-container {
    max-height: 100%;
    overflow-x: visible;


}

img {
    height: 120%;
    transform: translate(5%, -10%);
    overflow-x: visible;
    z-index: 1000;
}

.button {
    background-color: #00000000;
    color: white;
    border: 3px solid #0282f9;
    padding: 10px;
}
</style>

<template>
    <div id="containerHeader">
        <div class=" d-flex flex-row justify-content-between container">
            <div class="subcontainer-header d-flex flex-row justify-content-start align-items-center w-25">
                <img src="../assets/img/dc-logo.png" class="" alt="">
            </div>

            <div v-for="(section, index) in categories" @click="selectTitle(index)"
                class="tilesTotali d-flex flex-column justify-content-between ">
                <div></div>
                <div>{{ section.title }}</div>
                <div class="bottom-color " style="height: 3px;" :class="{ active: (index === selected) }">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'HeaderApp',
    data() {
        return {
            categories: [
                {
                    id: 0,
                    title: 'CHARACTERS'
                },
                {
                    id: 1,
                    title: 'MOVIES'
                },
                {
                    id: 2,
                    title: 'TV'
                },
                {
                    id: 3,
                    title: 'GAMES'
                },
                {
                    id: 4,
                    title: 'COLLECTIBLES'
                },
                {
                    id: 5,
                    title: 'VIDEOS'
                },
                {
                    id: 6,
                    title: 'FANS'
                },
                {
                    id: 7,
                    title: 'NEWS'
                },
                {
                    id: 8,
                    title: 'SHOP'
                }
            ],
            selected: 1
        }
    },
    methods: {
        selectTitle(index) {
            this.selected = index;
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../node_modules/bootstrap/scss/bootstrap";

.tilesTotali {}

#containerHeader {
    background-color: white;
    margin: 20px auto;


}

.subcontainer-header {
    min-height: 100%;
}

img {
    height: 80%;
}

.active {
    background-color: #10508c;
}

li {
    list-style: none;
    margin-left: 20px;
    padding: 40px 0;
    align-content: stretch;
    line-height: 100%;
}
</style>
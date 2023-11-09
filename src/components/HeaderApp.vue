
<template>
    <div id="containerHeader" class=" d-flex flex-row justify-content-evenly ">

        <div class="subcontainer-header d-flex flex-row justify-content-center align-items-center ">

            <img src="../assets/img/favicon.ico" alt="">
        </div>

        <ul class=" subcontainer-header  d-flex flex-row justify-content-center align-items-center h-100">
            <li v-for="(section, index) in categories" @click="selectTitle(index)" class="h-100">
                {{ section.title }}
                <div class="bottom-color active" v-if="(index === selected)">

                </div>
            </li>
        </ul>
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

#containerHeader {
    background-color: white;
    margin: 20px auto;


}

.active {
    background-color: red;
    height: 3px;
}

li {
    list-style: none;
    margin-left: 20px;
    padding: 40px 0;
    align-content: stretch;
}
</style>
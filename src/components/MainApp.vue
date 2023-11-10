<template>
    <div class="myJumbotron ">
        <img src="../assets/img/jumbotron.jpg" alt="" srcset="" class="jumboimg">
    </div>
    <div class="container">
        <div class="button button-mine btn-primary text-white ">CURRENT SCENE</div>
    </div>
    <div class="container">

        <div class="d-flex flex-row justify-content-between container flex-wrap ">
            <CardApp v-for="(card, index) in importedFiles" :image="card.thumb" :cost="card.price" :title="card.series"
                :typology="card.type" />
        </div>

    </div>
    <div class="d-flex flex-row justify-content-center mb-3 ">
        <div class="button btn-primary">
            LOAD MORE
        </div>
    </div>
</template>

<script>
import axios from 'axios'
import CardApp from './CardApp.vue';
export default {
    name: 'MainApp',
    components: {
        CardApp
    },
    data() {
        return {
            importedFiles: undefined,
            selected: 1
        }
    },
    methods: {
        fetchData() {
            axios
                .get('../src/components/data/dc-comics.json')
                .then(response => {
                    this.importedFiles = response.data
                    console.log(this.importedFiles)
                })
        },
        changeSelected() {
            console.log('hello')
        }
    },
    mounted() {

        this.fetchData()


    }
}
</script>

<style lang="scss" scoped>
h1 {
    color: white;
    margin: 20px auto;
}

.myJumbotron {
    width: 100%;
    height: 200px;
    overflow-y: hidden;
}

.jumboimg {
    background-color: red;
    width: 100%;
    max-height: 480px;

}

.button {
    width: fit-content;
    padding: 10px;
}

.button-mine {
    transform: translate(0%, -50%);
}
</style>
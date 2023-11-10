<template>
    <div class="container">
        <h1>{{ content }}</h1>
        <CardApp v-for="card in importedFiles" :image="card.thumb" :cost="card.price" :title="card.series"
            :typology="card.type" />
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
            content: '-->Content goes here<--',
            importedFiles: undefined
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
        ParseData() {

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
</style>
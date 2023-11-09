<template>
    <div class="container">
        <h1>{{ content }}</h1>
    </div>
</template>

<script>
export default {
    name: 'MainApp',
    data() {


        return {
            content: '-->Content goes here<--'
        }
    }
}
</script>

<style lang="scss" scoped>
h1 {
    color: white;
    margin: 20px auto;
}
</style>
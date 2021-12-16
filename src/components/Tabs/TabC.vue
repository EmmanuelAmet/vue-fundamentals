<template>
    <div>
        Tab C Content
    </div>
    <keep-alive>
    <input type="text" v-model="name">
    </keep-alive>
</template>

<script>
    export default {
        name: 'TabC',
        data(){ 
            return {
                name: ''
            }
        }
    }
</script>

<style scoped>

</style>
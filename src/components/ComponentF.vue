<template>
    <div>
        <h2>Component F</h2>
        <h3>Username: {{username}}</h3>
    </div>
</template>

<script>
    export default {
        name: 'ComponentF',
        components:{

        },
        inject: ['username']
    }
</script>

<style scoped>

</style>
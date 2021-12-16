<template>
    <h3 v-for="name in names" :key="name.firstName">
        <slot :firstName="name.firstName" :lastName="name.lastName"></slot>
    </h3>
</template>

<script>
    export default {
        name: 'NameList',
        data() {
            return {
                names: [
                    {
                        firstName: 'Henry',
                        lastName: 'Dei'
                    },
                    {
                        firstName: 'Nathan',
                        lastName: 'Walls'
                    },
                    {
                        firstName: 'Bless',
                        lastName: 'Aleric'
                    }
                ]
            }
        }
    }
</script>

<style scoped>

</style>
<template>
    <h3 v-show="showElement">You are a VIP user</h3>
    <h2> {{ name }}</h2>
</template>

<script>
export default {
    name: 'AppFooter',
    props: {
        name: {
            type: String
        },
        vip: {
            type: String
        }
    },
    data() {
        return {
            showElement: true
        }
    }
    
}
</script>

<style scoped>

</style>

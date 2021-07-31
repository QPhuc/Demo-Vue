<template>
    <div>
        <h2>Hello {{ firstName }}  {{ lastName }}</h2>
    </div>
</template>

<script>
    export default {
        name: 'PersonGreeting',
        props: ['firstName', 'lastName'],
    }
</script>

<style scoped>

</style>
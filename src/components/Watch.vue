<template>
    <div>
        <input type="text" placeholder="Name" v-model="name">
    </div>
</template>

<script>
    export default {
        name: 'Watch',
        data() {
            return {
                name: '',
            }
        },
        watch: {
            name(newValue, oldValue) {
                console.log('Old value', oldValue);
                console.log('New value', newValue);
            }
        }
    }
</script>

<style scoped>

</style>
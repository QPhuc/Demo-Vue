<template>
    <div>
        <!-- Option API -->
        <input type="text" placeholder="First Name" v-model="fName">
        <input type="text" placeholder="Last     Name" v-model="lName">
    </div>
</template>

<script>
    export default {
        name: 'VModel',
        data() {
            return {
                fName: '',
                lName: '',
            }
        },
    }
</script>

<style scoped>

</style>
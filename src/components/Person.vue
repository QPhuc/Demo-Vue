<template>
    <div>
        <input type="text" placeholder="First Name" v-model="firstName">
        <input type="text" placeholder="Last Name" v-model="lastName">
    </div>
</template>

<script>
    import { ref } from 'vue'
    export default {
        name: 'Person',
        components: {

        },
        setup(props) {
            const firstName = ref('')
            const lastName = ref('')

            return {
                firstName,
                lastName
            }
        },
    }
</script>

<style scoped>

</style>
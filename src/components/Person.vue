<template>
    <div>
        <input type="text" placeholder="First Name" v-model="firstName">
        <input type="text" placeholder="Last Name" v-model="lastName">
    </div>
    <PersonGreeting :firstName="firstName" :lastName="lastName" />
</template>

<script>
    import { ref } from 'vue';
    import PersonGreeting from './PersonGreeting.vue'

    export default {
        name: 'Person',
        components: {
            PersonGreeting,
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
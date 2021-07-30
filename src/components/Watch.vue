<template>
    <div>
        <input type="text" placeholder="Name" v-model="name">


        <input type="text" placeholder="First Name" v-model="firstName">
        <input type="text" placeholder="Last Name" v-model="lastName">
    </div>
</template>

<script>
    import { ref, watch } from 'vue';
    export default {
        name: 'Watch',
        setup(props) {
            const firstName = ref('')
            const lastName = ref('Phuc')

            watch([firstName, lastName], (newValue, oldValue) => {
                console.log('firstName Old value', oldValue[0]);
                console.log('firstName New value', newValue[0]);
                console.log('lastName Old value', oldValue[1]);
                console.log('lastName New value', newValue[1]);
            })

            return {
                firstName,
                lastName
            }
        },
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
<template>
    <div>
        <!-- Option API -->
        <input type="text" placeholder="First Name" v-model="fName">
        <input type="text" placeholder="Last Name" v-model="lName">
        <h2>Option Fullname is {{ fullName }}</h2>
        
        <input type="text" placeholder="First Name" v-model="refFirstName">
        <input type="text" placeholder="Last Name" v-model="refLastName">
        <h2>Conposition Fullname is {{ refFullName }}</h2>
    </div>
</template>

<script>
    import {ref, computed} from 'vue'
    export default {
        name: 'Computed',
        setup(props) {
            const refFirstName = ref('');
            const refLastName = ref('');

            const refFullName = computed(function() {
                return `${refFirstName.value} ${refLastName.value}`
            })

            return {
                refFirstName,
                refLastName,
                refFullName
            }
        },
        data() {
            return {
                fName: '',
                lName: '',
            }
        },
        computed: {
            fullName() {
                return `${this.fName} ${this.lName}`
            }
        }
    }
</script>

<style scoped>

</style>
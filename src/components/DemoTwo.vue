<template>
    <div>
        <h2> {{ firstName }}  {{ lastName }} </h2>
        <h2> {{ fname }}  {{ lname }} </h2>
    </div>
</template>

<script>
    import { reactive, toRefs } from 'vue';
    export default {
        name: 'DemoTwo',
        setup(props) {
            const state = reactive({
                firstName: 'Tran',
                lastName: 'Phuc',
            })

            setTimeout(() => {
                state.firstName = 'PHUC';
                state.lastName = 'TRAN';
                console.log(state);
            }, 2000);

            return toRefs(state)
        },
        data() {
            return {
                fname: 'Tran',
                lname: 'Phuc',
            }
        },
    }
</script>

<style scoped>

</style>
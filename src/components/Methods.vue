<template>
    <div>
        <h2>{{ name }}</h2>
        <button @click="setName">Change Name</button>

        <h2> {{ count }} </h2>
        <button @click="incrementCount">Increment Count</button>

        <h2> {{ first }} {{ last }} </h2>
        <button @click="changeHero">Change Hero</button>
    </div>
</template>

<script>
    import { ref, reactive, toRefs } from 'vue'
    export default {
        name: 'Methods',
        setup(props) {
            const count = ref(0);
            const state = reactive({
                first: 'Tran',
                last: 'Phuc',
            })

            function incrementCount() {
                count.value++
            }

            function changeHero() {
                state.first = 'PHUC';
                state.last = 'TRAN';
            }

            return {
                count,
                incrementCount,
                ...toRefs(state),
                changeHero
            }
        },
        data() {
            return {
                name: 'QPhuc'
            }
        },
        methods: {
            setName() {
                this.name= 'TRAN QUANG PHUC'
            }
        },
    }
</script>

<style scoped>

</style>
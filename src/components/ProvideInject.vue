<template>
    <div>
        <h3>Parent component {{ name }} </h3>
        <h3>Parent component count  {{ count }} </h3>
        <h3>Parent component hero {{ firstName }}  {{lastName}} </h3>

        <button @click="incrementCount">Increment count</button>

        <ChildA />
    </div>
</template>

<script>
    import { provide, ref, reactive, toRefs } from 'vue'
    import ChildA from './ChildA.vue'
    export default {
        components: { ChildA },
        name: 'ProvideInject',
        setup(props) {
            provide('c_userName', 'TRAN QUANG PHUC')

            const count = ref(0)

            function incrementCount() {
                count.value++
            }

            const state = reactive({
                firstName: 'Tran',
                lastName: 'Phuc'
            })

            provide('c_count', count)
            provide('c_hero', state)
            provide('incrementCount', incrementCount)

            return {
                count,
                ...toRefs(state),
                incrementCount
            }
        },
        data() {
            return {
                name: 'QPhuc'
            }
        },
        provide() {
            return {
                userName: this.name
            }
        }
    }
</script>

<style scoped>

</style>
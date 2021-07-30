<template>
    <div>
        <h3>Parent component {{name}} </h3>
        <ChildA />
    </div>
</template>

<script>
    import ChildA from './ChildA.vue'
    export default {
        component: { ChildA },
        name: 'ProvideInject',
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
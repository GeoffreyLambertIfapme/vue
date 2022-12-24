<template>
    <button class="btn btn-primary" @click="onClick()">
        {{  label }} 
    </button>
</template>

<script>
export default {
    name: 'ActionComponent',
    props: {
        label: String
    },
    methods: {
        onClick(){
            this.$emit('action');
        }
    }
}
</script>

<style>
</style>
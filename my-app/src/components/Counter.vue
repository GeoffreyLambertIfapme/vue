<template>
    <span class="value">
        {{  value }}  
    </span>
</template>

<script>
export default {
    name: 'CounterValue',
    props: {
        value: Number
    }
}
</script>

<style>
.value {
    color: green;
}
</style>
<template>
    <button @click="onClick()" :style="{background: color}" class='btn'>{{ text }}</button>
</template>

<script>
    export default {
        name: 'AppButton',
        props: {
            text: String,
            color: String,
        },
        methods: {
            onClick() {
                this.$emit('show-add-a')
            }
        }
    }
</script>

<style>

</style>
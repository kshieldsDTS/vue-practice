<template>
    <header>
        <h1>{{ title }}</h1>
        <AppButton @toggle-add-task="$emit('toggle-add-task')" :text="showAddTask ? 'Close' : 'Add Task'" :color="showAddTask ? 'red' : 'green'"/>
    </header>
</template>

<script>
import AppButton from './AppButton'
    export default {
        name: 'PageHeader',
        props: {
            title: String,
            showAddTask: Boolean,
        },
        components: {
            AppButton
        }
    }
</script>

<style scoped>
    header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
    }
</style>
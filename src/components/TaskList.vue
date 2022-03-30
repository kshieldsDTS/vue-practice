<template>
    <div :key='task.id' v-for="task in tasks">
        <TaskView @delete-task="$emit('delete-task', task.id)" :task="task"/>
    </div>
</template>

<script>
import TaskView from "./TaskView.vue"

    export default {
        name: 'TaskList',
        props: {
            tasks: Array,
        },
        components: {
            TaskView
        },
        emits: ['delete-task'],
    }
</script>
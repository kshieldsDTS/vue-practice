<template>
    <div :key='task.id' v-for="task in tasks">
        <TaskView :task="task"/>
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
        }
    }
</script>
<template>
    <div class="taskContainer">
        <div v-bind:key="task.id" v-for="task in tasks">
            <Task @toggle-reminder="$emit('toggle-reminder', task.id)" v-on:delete-task="$emit('delete-task', task.id)" :task="task" />
        </div>
    </div>
</template>

<script>
import Task from "./Task.vue"

export default {
    name: "Tasks",
    props: {
        tasks: Array
    },
    components: {
        Task
    }
}
</script>
<template>
    <div v-for="(task, index) in tasks" :key="index">
        <AppTask @toggle-reminder="$emit('toggle-reminder', task.id)" @delete-task="$emit('delete-task',task.id)" :task="task"/>
    </div>
</template>

<script>
import AppTask from './AppTask.vue';
    export default{
    name: "AppTasks",
    props: ["tasks"],
    methods: {},
    emits: ['delete-task','toggle-reminder'],
    components: { AppTask }
}
</script>

<style scoped>

</style>
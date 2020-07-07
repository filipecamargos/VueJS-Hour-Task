<template>
    <div class="row">
        <app-task v-for="(task, index) in tasks" :key="task" @click.native="removeTask(index)"> {{ task }}</app-task>
    </div>
</template>

<script>
//Import the Task template and its values associated
import Task from './Task.vue';

export default {
    props: ['tasks'],
    components: {
        appTask: Task
    },
    methods: {
        removeTask(index) {
            this.$emit('removeTask', index);
        }
    },
    
}
</script>

<style scoped>

</style>
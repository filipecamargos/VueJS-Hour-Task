<template>
    <div class="container">
        <top-progress :taskCounts="taskDone" :setNumTasks="myTasks"></top-progress>
        <app-new-task @addTaskEvent="novaTask"></app-new-task>
        <app-task-view :tasks="tasks" @removeTask = "removeTask"></app-task-view>
        <div class="row">
            <div class="col-sm-12 text-center">
                <div class="alert alert-info">Info: Click on the Task to Remove it Once is Completed!</div>
            </div>
        </div>
    </div>
</template>

<script>
    import TaskView from "./components/TaskView.vue";
    import NewTask from "./components/NewTask.vue";
    import ProgressBar from "./components/ProgressBar.vue";

    export default {   
        data: function() {
            return {
                tasks: ["test","test", "hello"],
                myTasks: 10,
                taskDone: 0,
            }
        },
        methods: {
            novaTask(task) {
                if (this.tasks.length >= this.myTasks )
                {
                    return alert('Max number')
                }
                this.tasks.push(task);
            },
            removeTask(index) {
                this.tasks.splice(index, 1);
                this.taskDone ++;
            }
        },
        components: {
            appTaskView: TaskView,
            appNewTask: NewTask,
            topProgress: ProgressBar
        }
    }
</script>

<style>
</style>

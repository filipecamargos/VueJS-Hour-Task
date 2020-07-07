<template>
    <div class="row">
        <form>
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
                <label>Task</label>
                <textarea class="form-control" rows="3" v-model="task"></textarea>
            </div>
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
                <button class="btn btn-primary" @click.prevent="createNew">Add Task</button>
            </div>
        </form>
    </div>
</template>


<script>
export default {
    data: function () { 
        return {
            task: '',
        };
     },
     methods: {
         createNew() {
             if (this.task < 1) {
                 return
             }
             this.$emit('addTaskEvent', this.task);
             this.task = "";
         }
     },
}
</script>

<style scoped>

</style>
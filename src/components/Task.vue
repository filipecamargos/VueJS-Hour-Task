<template>
    <div class="col-sm-6 col-md-4 col-lg-3">
        <div class="panel panel-default">
            <div class="panel-body task">
                <slot></slot>
            </div>
        </div>
    </div>
</template>

<script>
</script>

<style scoped>
    .panel-body {
        background-color: aqua;
    }

    .task {
        cursor: pointer;
    }

    .task:hover {
        background-color: #ffe2e2;
    }

</style>
<template>
    <div class="row">
        <div class="col-sm-12">
            <h3> Title </h3>
            <div class="progress">
                <div class="progress">
                    <div class="progress-bar" role="progressbar" aria-valuenow="60" aria-valuemin="0" aria-valuemax="100"
                     :style="{width: (taskCounts / setNumTasks) * 100 + '%'} ">
                        {{ taskCounts }} | {{ setNumTasks }}
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: ['taskCounts', 'setNumTasks']
}
</script>

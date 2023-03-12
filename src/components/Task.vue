<template>
    <div :class="[task.reminder ? 'reminder' : '', 'task']">
        <h3>
            {{ task.text }}
            <i class="fas fa-solid fa-trash"></i>
        </h3>
        <p>
            {{ task.day }}
        </p>
    </div>
</template>

<script>
export default {
    name: 'Task',
    props: {
        task: {
            type: Object
        }
    }
}
</script>

<style>
.fas {
    color: red;
}

.task {
    background: #f4f4f4;
    margin: 5px;
    padding: 10px 20px;
    cursor: pointer;
}

.task.reminder {
    border-left: 5px solid green;
}

.task h3 {
    color: #333;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.task p {
    color: #666;
}
</style>

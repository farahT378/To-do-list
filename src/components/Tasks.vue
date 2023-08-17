<template>
    <Task  :key="task.id" v-for="task in tasks" :task="task" @toggle-reminder="$emit('toggle-reminder',task.id)" @delete-task="$emit('delete-task',task.id)" />
</template>

<script>
import Task from './Task.vue'
export default{
    name:'Tasks',
    props:{
       tasks:Array, 
    },
    components:{
        Task,
    },
    emits: ['delete-task' , 'toggle-reminder'],
}
</script>

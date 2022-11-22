<template>
  <div :key="task.id" v-for="task in tasks">
  <TaskTwo @delete-task="$emit('delete-task', task.id)" :task="task" />
  </div>
</template>

<script>
import TaskTwo from './TaskTwo.vue'

 export default {
  name: 'TaskMain',
  props: {
    tasks: Array
  },
  components: {
    TaskTwo,
  },
  emits: ['delete-task'],
 }
</script>
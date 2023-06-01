<template>
  <!-- loop through tasks array. v-bind:key === :key-->
  <div v-for="task in tasks" :key="task.id">
    <!-- handle the emit from Task component -->
    <Task @toggle-reminder="$emit('toggle-reminder', task.id)" @delete-task="$emit('delete-task', task.id)" :task="task" />
  </div>
</template>


<script>
import Task from './Task.vue';


export default {
  /* eslint-disable */
  name: "Tasks",
  props: {
    tasks: Array
  },
  components: {
    Task
  },
  emits: ['delete-task', 'toggle-reminder']
};
</script>
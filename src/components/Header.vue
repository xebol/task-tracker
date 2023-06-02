<template>
  <header>
    <h1>{{ title }}</h1>
    <Button @btn-click="$emit('toggle-add-task')" :text="showAddTask ? 'Close' : 'Add Task'" :color="showAddTask ? 'red' : 'green'"/>
  </header>
</template>


<script>
import Button from './Button';

export default {
  /* eslint-disable */
  name: "Header",
  props: {
    title: String,
    showAddTask: Boolean
  },
  components: {
    Button
  }
};
</script>


<!-- scoped means any styling is only applied to this particular component -->
<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>
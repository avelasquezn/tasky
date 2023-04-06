<template>
  <div>
      <h2>Tasky</h2>
      <h3>Task Management</h3>
      <ul>
          <li v-for="task in tasks" :key="task.id">
              <task-item v-bind:task="task" />
          </li>
      </ul>
  </div>
</template>

<script>
import TaskItem from "./task-item.vue";

export default {
    name: "task-list",
    components: {TaskItem},
    props: ["tasks"]
}
</script>

<style scoped>

</style>
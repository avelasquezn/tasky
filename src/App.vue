<script>

import TaskList from "./components/task-list.vue";
import AddTask from "./components/add-task.vue";

export default {
    name: 'App',
    components: { TaskList, AddTask },
    data() {
        return {
            tasks: [
                { id: 1, title: 'Prepare Final Project Status', completed: false},
                { id: 2, title: 'Study Web Apps', completed: false},
                { id: 3, title: 'Do laundry', completed: false},
                { id: 4, title: 'Cook breakfast', completed: false},
                { id: 5, title: 'Learn Vue', completed: false}
            ]
        }
    },
    methods: {
        addTask(newTask) {
            this.tasks.push(newTask);
        }
    }
}
</script>

<template>
  <div id="app">
      <task-list v-bind:tasks="tasks"/>
      <add-task v-on:add-task="addTask"/>
  </div>
</template>

<style scoped>

</style>

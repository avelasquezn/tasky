<template>
  <div><p>{{ task.title }}</p></div>
</template>

<script>
export default {
    name: "task-item",
    props: [
        "task"
    ]
}
</script>

<style scoped>

</style>
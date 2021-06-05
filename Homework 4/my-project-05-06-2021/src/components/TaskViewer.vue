<template>
  <div class="main-container">
    <div class="title">{{ title }}</div>
    <div class="tasks-container">
      <task-card
        v-for="task in tasksList"
        :key="task.id"
        :category="task.category"
        :title="task.title"
        :users="task.users"
      />
    </div>
    <div>
      <p class="add">Add a card...</p>
    </div>
  </div>
</template>

<script>
import TaskCard from "./TaskCard";
export default {
  name: "TaskViewer",
  components: { TaskCard },
  props: {
    title: {
      type: String,
      default: "Tasks list",
    },
    tasksList: {
      type: Array,
      default: () => [],
    },
  },
};
</script>

<style lang="css" scoped>
.main-container {
  width: 320px;
  padding: 10px;
  background-color: lightblue;
  border-radius: 10px;
}
.title {
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
  font-weight: bold;
}
.add {
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
  margin-left: 10px;
}
</style>
<template>
  <div :key="todo.id" v-for="todo in todos" class="todo">
    <TodoItem
      v-bind:todo_prop="todo"
      v-on:del-todo="$emit('del-todo', todo.id)"
    />
  </div>
</template>

<script>
import TodoItem from "./TodoItem";
export default {
  name: "Todos",
  props: ["todos"],
  components: {
    TodoItem,
  },
};
</script>

<style scoped>
  .todo {
    margin: 0 40px 0 40px;
    padding: 2px;
  }
</style>

<template>
  <ul>
    <todo-item v-for="todo in todos" :key="todo.id" :todo="todo" />
  </ul>
</template>

<script>
import { inject } from "@vue/runtime-core";
import TodoItem from "./TodoItem.vue";
export default {
  components: { TodoItem },

  setup() {
    const todos = inject("todos");

    return {
      todos,
    };
  },
};
</script>

<style></style>

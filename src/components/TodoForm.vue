<template>
  <form @submit.prevent="addTodo">
    <input v-model.trim="todoText" type="text" placeholder="Add to-do" />
  </form>
</template>

<script>
import { inject, ref } from "@vue/runtime-core";
export default {
  setup() {
    const todos = inject("todos");
    const todoText = ref("");
    console.log(todos.value);

    const addTodo = () => {
      if (!todoText.value.trim()) {
        console.log("Vacio");
        return;
      }
      const todo = {
        todo: todoText.value,
        state: false,
        id: Date.now(),
      };
      todos.value.push(todo);
      todoText.value = "";
    };

    return {
      addTodo,
      todoText,
    };
  },
};
</script>

<style></style>

<template>
  <div class="app-container">
    <todo-app />
  </div>
</template>

<script>
import TodoApp from "./components/TodoApp.vue";
export default {
  components: { TodoApp },
  name: "App",
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.app-container {
  width: 100%;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
}
</style>

<script setup>
import AppTitle from './components/AppTitle.vue';
import AddTodoInput from './components/AddTodoInput.vue';
import Filters from './components/Filters.vue';
import TodoList from './components/TodoList.vue';
</script>

<template>
  <AppTitle></AppTitle>
  <AddTodoInput></AddTodoInput>
  <Filters></Filters>
  <TodoList></TodoList>
</template>

<style>
body {
  display: flex;
  justify-content: center;
  padding: 40px 20px;
}

#app {
  max-width: 600px;
  width: 100%;
}
</style>

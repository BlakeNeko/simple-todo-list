<script setup>
import TodoItem from './TodoItem.vue';
import TodoStatusBar from './TodoStatusBar.vue';
</script>

<template>
  <div class="card">
    <TodoItem></TodoItem>
    <TodoItem></TodoItem>
    <TodoItem></TodoItem>
    <TodoStatusBar></TodoStatusBar>
  </div>
</template>

<style scoped>
.card {
  padding: 16px;
  background-color: #fafafa;
  border-radius: 4px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  margin-bottom: 16px;
}
</style>

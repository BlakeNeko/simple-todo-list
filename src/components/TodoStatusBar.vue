<script setup>
const props = defineProps(['allTodosLength', 'doneTodosLength']);
</script>

<template>
  <div class="status">
    <span>共 {{ allTodosLength }} 项，已完成 {{ doneTodosLength }} 项</span>
  </div>
</template>

<style scoped>
.status {
  display: flex;
  align-items: center;
  font-size: 14px;
  color: #666666;
  margin-top: 16px;
}
</style>

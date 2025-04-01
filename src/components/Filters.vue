<script setup></script>

<template>
  <div class="buttons">
    <div class="filters">
      <button class="active">全部</button>
      <button>待完成</button>
      <button>已完成</button>
    </div>
    <div class="clear-done">
      <button>清除已完成</button>
    </div>
  </div>
</template>

<style scoped>
.buttons {
  display: flex;
  justify-content: space-between;
  margin-bottom: 24px;
}

.filters {
  display: flex;
  gap: 12px;
}

.filters button {
  padding: 6px 12px;
  background: none;
  border: none;
  border-radius: 4px;
  font-size: 14px;
  color: #666666;
  cursor: pointer;
  transition: all 0.2s ease;
}

.filters button:hover,
.clear-done button:hover,
.filters button.active {
  background-color: #e8f5e9;
  color: #3cb371;
}

.filters button.active {
  font-weight: 500;
}

.clear-done button {
  background: none;
  border: none;
  color: #3cb371;
  font-size: 14px;
  cursor: pointer;
  padding: 6px 12px;
  border-radius: 4px;
  transition: all 0.2s ease;
}
</style>

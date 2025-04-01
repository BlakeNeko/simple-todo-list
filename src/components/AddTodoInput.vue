<script setup></script>

<template>
  <div class="card">
    <div class="input-group">
      <input type="text" placeholder="添加新的待办事项……" />
      <button>添加</button>
    </div>
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

.input-group {
  display: flex;
  gap: 8px;
}

.input-group input[type='text'] {
  flex: 1;
  padding: 10px 16px;
  border: 1px solid #e0e0e0;
  border-radius: 4px;
  font-size: 16px;
  transition: all 0.2s ease;
}

.input-group input[type='text']:focus {
  outline: none;
  border-color: #3cb371;
  box-shadow: 0 0 0 2px rgba(60, 179, 113, 0.2);
}

button {
  background-color: #3cb371;
  color: #ffffff;
  border: none;
  border-radius: 4px;
  padding: 10px 16px;
  font-size: 16px;
  font-weight: 500;
  cursor: pointer;
  transition: all 0.2s ease;
}

button:hover {
  background-color: #2e8b57;
}
</style>

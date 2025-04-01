<script setup></script>

<template>
  <div class="todo-item">
    <input type="checkbox" />
    <span>任务内容</span>
    <div class="actions">
      <button>编辑</button>
      <button>删除</button>
    </div>
  </div>
</template>

<style scoped>
.todo-item {
  display: flex;
  align-items: center;
  padding: 12px 0;
  border-bottom: 1px solid #e0e0e0;
}

input[type='checkbox'] {
  margin-right: 12px;
  appearance: none;
  width: 20px;
  height: 20px;
  border: 2px solid #e0e0e0;
  border-radius: 4px;
  cursor: pointer;
  position: relative;
  transition: all 0.2s ease;
}

input[type='checkbox']:checked {
  background-color: #3cb371;
  border-color: #3cb371;
}

input[type='checkbox']:checked::after {
  content: '✓';
  color: #ffffff;
  font-size: 14px;
  position: absolute;
  left: 3px;
}

span {
  flex: 1;
  font-size: 16px;
  color: #333333;
}

.actions {
  display: flex;
  gap: 4px;
}

.actions button {
  background: none;
  border: none;
  color: #666666;
  cursor: pointer;
  padding: 4px;
  border-radius: 4px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.actions button:hover {
  background-color: rgba(0, 0, 0, 0.05);
  color: #3cb371;
}
</style>

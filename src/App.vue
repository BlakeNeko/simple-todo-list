<script setup>
import AppTitle from './components/AppTitle.vue';
import AddTodoInput from './components/AddTodoInput.vue';
import Filters from './components/Filters.vue';
import TodoList from './components/TodoList.vue';

import { ref, computed } from 'vue';

const todos = ref([
  { id: 1, title: '学习Vue', isDone: false },
  { id: 2, title: '学习React', isDone: false },
  { id: 3, title: '学习JavaScript', isDone: true },
]);

const allTodosLength = computed(() => {
  return todos.value.length;
});
const doneTodosLength = computed(() => {
  return todos.value.filter((each) => each.isDone === true).length;
});

const allFilters = ref(['全部', '待完成', '已完成']);
const selectedFilter = ref(0);

function handleChangeFliter(index) {
  selectedFilter.value = index;
}
</script>

<template>
  <AppTitle></AppTitle>
  <AddTodoInput></AddTodoInput>
  <Filters
    :all-filters="allFilters"
    :selected-filter="selectedFilter"
    @change-fliter="handleChangeFliter"
  ></Filters>
  <TodoList
    :all-todos-length="allTodosLength"
    :done-todos-length="doneTodosLength"
  ></TodoList>
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

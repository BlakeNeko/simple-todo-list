<script setup>
import AppTitle from './components/AppTitle.vue';
import AddTodoInput from './components/AddTodoInput.vue';
import Filters from './components/Filters.vue';
import TodoList from './components/TodoList.vue';

import { ref } from 'vue';

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

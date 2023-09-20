<script setup>
import { ref } from 'vue'
import TodoItem from './TodoItem.vue'

const groceryList = ref([
  { id: 0, text: '야채' },
  { id: 1, text: '치즈' },
  { id: 2, text: '무엇이든 먹고 싶은 음식 재료' }
])
</script>

<template>
  <ol>
    <TodoItem
      v-for="item in groceryList"
      :todo="item"
      :key="item.id"
    ></TodoItem>
  </ol>
</template>
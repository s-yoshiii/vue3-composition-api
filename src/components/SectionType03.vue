<script setup>
import { ref } from "vue";
const newTodo = ref("");
const todos = ref([]);
const addTodo = () => {
  todos.value.push(newTodo.value);
  newTodo.value = "";
};
</script>
<template>
  <h2>繰り返し処理でリストを作ろうv-for</h2>
  <input type="text" size="30" v-model="newTodo" />
  <button type="button" @click="addTodo()">追加</button>
  <ul>
    <li v-for="(todo, i) in todos" :key="i">{{ i }}. {{ todo }}</li>
  </ul>
</template>

<script setup>
import { ref } from "vue";
import TodoList from "./TodoList.vue";
const newTodo = ref("");
const todos = ref([]);
const addTodo = () => {
  todos.value.push(newTodo.value);
  newTodo.value = "";
};
const removeTodo = (index) => {
  todos.value.splice(index, 1);
};
</script>
<template>
  <h2>
    繰り返し処理でリストを作ろう - v-for/Vue
    3で条件によって要素を表示・非表示しよう - v-if / v-else
  </h2>
  <input type="text" size="30" v-model="newTodo" />
  <button type="button" @click="addTodo()">追加</button>
  <TodoList :todos="todos" @removeTodo="removeTodo" />
</template>

<script setup>
import { ref } from "vue";
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
    繰り返し処理でリストを作ろう - v-for<br />
    条件によって要素を表示・非表示しよう - v-if / v-else
  </h2>
  <input type="text" size="30" v-model="newTodo" />
  <button type="button" @click="addTodo()">追加</button>
  <ul v-if="todos.length > 0">
    <li v-for="(todo, i) in todos" :key="i">
      {{ todo }}
      <button type="button" @click="removeTodo(i)" style="cursor: pointer">
        削除
      </button>
    </li>
  </ul>
  <p v-else>※ToDoを追加してください</p>
</template>

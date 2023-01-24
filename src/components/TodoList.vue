<script setup>
defineProps(["todos"]);
const emit = defineEmits(["removeTodo"]);
const clickRemove = (i) => {
  emit("removeTodo", i);
};
</script>
<template>
  <ul v-if="todos.length > 0">
    <li v-for="(todo, i) in todos" :key="i">
      {{ todo }}
      <button type="button" @click="clickRemove(i)" style="cursor: pointer">
        削除
      </button>
    </li>
  </ul>
  <p v-else>※ToDoを追加してください</p>
</template>

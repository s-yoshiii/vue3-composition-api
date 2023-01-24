<script setup>
import { ref } from "@vue/reactivity";

// Vue3でボタンのクリックに反応するイベント定義
const number = ref(0);
const add = () => {
  number.value++;
};
</script>
<template>
  <!-- Vue3でボタンのクリックに反応するイベント定義 -->
  <h2>Vue3でボタンのクリックに反応するイベント定義</h2>
  <input type="text" size="30" v-model="number" />
  <button @click="add()">+1</button>
</template>

<script setup>
import { ref } from "@vue/reactivity";
import { computed } from "@vue/runtime-core";
// Vueの新しい開発手法
const answer = computed(() => {
  return 1 + 1;
});
const message = computed(() => {
  if (name.value === "") {
    return "ようこそ<strong>ゲスト</strong>さん";
  }
  return `ようこそ<strong>${name.value}</strong>さん`;
});
const welcomeColor = "blue";
const name = ref("");

// Vue3でボタンのクリックに反応するイベント定義
const number = ref(0);
const add = () => {
  number.value++;
};
</script>
<template>
  <h1>Vue 3</h1>
  <!-- Vueの新しい開発手法 -->
  <h2>Vueの新しい開発手法</h2>
  <p>1 + 1 = {{ answer }}</p>
  <p>お名前は？：<input type="text" size="30" v-model="name" /></p>
  <p
    v-html="message"
    :style="{ backgroundColor: welcomeColor, color: 'white' }"
  ></p>
  <!-- Vue3でボタンのクリックに反応するイベント定義 -->
  <h2>Vue3でボタンのクリックに反応するイベント定義</h2>
  <input type="text" size="30" v-model="number" />
  <button @click="add()">+1</button>
</template>

<style></style>

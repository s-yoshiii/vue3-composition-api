<script setup>
import { computed, ref } from "@vue/runtime-core";

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
</script>
<template>
  <!-- Vueの新しい開発手法 -->
  <h2>Vueの新しい開発手法</h2>
  <p>1 + 1 = {{ answer }}</p>
  <p>お名前は？：<input type="text" size="30" v-model="name" /></p>
  <p
    v-html="message"
    :style="{ backgroundColor: welcomeColor, color: 'white' }"
  ></p>
</template>

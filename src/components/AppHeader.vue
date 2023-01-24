<script setup>
defineProps(["color"]);
</script>
<template>
  <header>
    <h1 :style="{ color: color }"><slot name="title">No Title</slot></h1>
    <slot name="caption"><span>学習用です。</span></slot>
  </header>
</template>

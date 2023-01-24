<script setup>
import AppHeader from "@/components/AppHeader.vue";
import SectionType01 from "@/components/SectionType01.vue";
import SectionType02 from "@/components/SectionType02.vue";
import SectionType03 from "@/components/SectionType03.vue";
</script>
<template>
  <AppHeader color="blue">
    <template v-slot:title> Vue 3 Composition API </template>
    <template v-slot:caption>
      <span
        :style="{
          'font-size': '12px',
        }"
        >v-slot name学習用です</span
      >
    </template>
  </AppHeader>
  <SectionType01 />
  <SectionType02 />
  <SectionType03 />
</template>

<style></style>

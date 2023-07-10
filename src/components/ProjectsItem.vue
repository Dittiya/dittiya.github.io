<script setup>
import { reactive, ref } from 'vue';

const items = ref([{ name: "test1" }, { name: "test2" }])
</script>

<template>
  <div class="carousel-item bg-body text-center" v-for="(item, index) in items" :class="{ 'active': index === 0 }">
    <h1>{{ item.name }}</h1>
  </div>
</template>

<style>

</style>

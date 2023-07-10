<script setup>
import { ref } from 'vue';

const items = ref([])

async function getConfig() {
  const response = await fetch("https://raw.githubusercontent.com/Dittiya/dittiya.github.io/master/public/config.json")
  const json = response.json()
  return json
}

async function getItems(fetchConfig) {
  const config = await fetchConfig()
  items.value = config.projects
}

getItems(getConfig)
</script>

<template>
  <div class="carousel-item bg-body text-center" v-for="(item, index) in items" :class="{ 'active': index === 0 }">
    <h1>{{ item.name }}</h1>
  </div>
</template>

<style></style>

<script setup>
import { RouterView } from 'vue-router'
import FooterComponent from './components/FooterComponent.vue'
import NavigationBar from './components/NavigationBar.vue'
</script>

<template>
	<NavigationBar />
	<RouterView />
	<FooterComponent />
</template>

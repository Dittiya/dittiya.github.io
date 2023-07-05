<script setup>
import { RouterLink, RouterView } from 'vue-router'
import FooterComponent from './components/FooterComponent.vue';
import NavigationBar from './components/NavigationBar.vue'
</script>

<template>
	<header class="fixed-top">
		<NavigationBar />
	</header>

	<RouterView />

	<footer class="fixed-bottom">
		<FooterComponent />
	</footer>
</template>

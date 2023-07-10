<script setup>
import { RouterView } from 'vue-router'
import FooterComponent from './components/FooterComponent.vue'
import NavigationBar from './components/NavigationBar.vue'
import LoadingState from './components/LoadingState.vue'
import { ref } from 'vue';

/* TODO
 * Add loading while fetching config
 */
const loading = ref(true)
</script>

<template>
	<template v-if="loading">
		<LoadingState />
	</template>
	<template v-else>
		<NavigationBar />
		<RouterView />
		<FooterComponent />
	</template>
</template>
